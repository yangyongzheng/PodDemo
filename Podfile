platform :ios, '15.0'
inhibit_all_warnings!

target 'AppMain' do
  # Comment the next line if you don't want to use dynamic frameworks
  use_frameworks!
  # ObjC Pods
  pod 'FMDB'
  pod 'SVProgressHUD'
  pod 'MJRefresh'
  # Swift Pods
  pod 'lottie-ios'
  pod 'SnapKit'
  pod 'Moya'
  # 第三方SDK
end

post_install do |installer|
  installer.generated_projects.each do |project|
    project.build_configurations.each do |config|
      if config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'].to_f < 15.0
        config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '15.0'
      end
    end
    project.targets.each do |target|
      target.build_configurations.each do |config|
        if config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'].to_f < 15.0
          config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '15.0'
        end
      end
    end
  end
end
