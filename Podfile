# Uncomment the next line to define a global platform for your project
 platform :ios, '16.0'

target 'GithubActionTest' do
  # Comment the next line if you don't want to use dynamic frameworks
  use_frameworks!

  pod 'Masonry'
  pod 'SnapKit'

end

post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings["IPHONEOS_DEPLOYMENT_TARGET"] = "14.0"

    if target.respond_to?(:product_type) and target.product_type == "com.apple.product-type.bundle"
        config.build_settings['CODE_SIGNING_ALLOWED'] = 'NO'
      end
    end

  end
end
