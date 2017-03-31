source 'https://github.com/CocoaPods/Specs.git'
platform :ios, '9.0'
inhibit_all_warnings!

target 'BaseAppV2' do
    use_frameworks!
    
    pod 'AlamofireActivityLogger', '~> 2.3'
    pod 'AlamofireNetworkActivityIndicator', '~> 2.0'
    pod 'Branch'
    pod 'CCBottomRefreshControl'
    pod 'Crashlytics', '~> 3.8'
    pod 'Dodo', '~> 7.0'
    pod 'ImagePicker', :git => 'https://github.com/hyperoslo/ImagePicker'
    pod 'IQKeyboardManager'
    pod 'Kingfisher', '~> 3.0'
    pod 'KYNavigationProgress'
    pod 'Raccoon'
    pod 'SCLAlertView', :git => 'https://github.com/vikmeup/SCLAlertView-Swift'
    pod 'SVProgressHUD'
    pod 'SwiftyBeaver'
    pod 'UITextField+Shake', '~> 1.1'
    
    target 'BaseAppV2Tests' do
        inherit! :search_paths
        pod 'OHHTTPStubs'
        pod 'OHHTTPStubs/Swift'
    end
    
    target 'BaseAppV2UITests' do
        inherit! :search_paths
        pod 'OHHTTPStubs'
        pod 'OHHTTPStubs/Swift'
    end
    
end

post_install do |installer|
    installer.pods_project.targets.each do |target|
        target.build_configurations.each do |config|
            config.build_settings['ENABLE_STRICT_OBJC_MSGSEND'] = "NO"
            config.build_settings['SWIFT_VERSION'] = '3.0'
        end
    end
end
