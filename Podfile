source 'https://github.com/CocoaPods/Specs.git'
use_frameworks!

def import_pods
    pod 'XCGLogger', '~> 3.3'
end

target 'lf iOS'  do
    platform :ios, '8.0'
    import_pods
end

target 'lf OSX' do
    platform :osx, '10.11'
    import_pods
end

target 'Example iOS'  do
    platform :ios, '8.0'
    import_pods
end

target 'Example OSX' do
    platform :osx, '10.11'
    import_pods
end

target 'Tests' do
    platform :osx, '10.11'
    import_pods
end

post_install do |installer|
    installer.pods_project.targets.each do |target|
        target.build_configurations.each do |config|
            config.build_settings['SWIFT_VERSION'] = '2.3'
            config.build_settings['MACOSX_DEPLOYMENT_TARGET'] = '10.10'
        end
    end
end

