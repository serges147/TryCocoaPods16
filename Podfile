platform :osx, '10.10'
use_frameworks!

workspace 'TryCocoaPods16'

def podAlamofire
  pod 'Alamofire'
end

target 'TryCocoaPods16' do

  project 'TryCocoaPods16.xcodeproj'
  pod 'Alamofire'

end

target 'MyFramework' do

  project 'MyFramework/MyFramework.xcodeproj'
  pod 'Alamofire'

end

def patch_xcconfig_file(config)

  puts config.base_configuration_reference.real_path

end

post_install do |installer_representation|

  installer_representation.pods_project.targets.each do |target|

    target.build_configurations.each do |config|

      patch_xcconfig_file(config)

    end

  end

end
