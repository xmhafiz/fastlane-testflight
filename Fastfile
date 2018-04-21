# This file contains the fastlane.tools configuration
# You can find the documentation at https://docs.fastlane.tools
#
# For a list of all available actions, check out
#
#     https://docs.fastlane.tools/actions
#

# Uncomment the line if you want fastlane to automatically update itself
# update_fastlane

default_platform(:ios)

platform :ios do
  desc "Submit a new Beta Build to Apple TestFlight"
  lane :beta do
    # match(type: "appstore") # more information: https://codesigning.guide

    increment_build_number(
      # increment build and update version accrodingly
      build_number: latest_testflight_build_number(version: "1.0") + 1,
      xcodeproj: "AwesomeProject.xcodeproj"
    )

    get_certificates           # invokes cert
    get_provisioning_profile   # invokes sigh

    # scheme and workspace file
    build_app(workspace: "AwesomeProject.xcworkspace", scheme: "AwesomeProject")
    upload_to_testflight(skip_waiting_for_build_processing: true)
 
    # sh "your_script.sh"
  end
end