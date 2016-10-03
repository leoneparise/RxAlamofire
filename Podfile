# Uncomment this line to define a global platform for your project
platform :ios, '8.0'

use_frameworks!

def common 
	pod 'Alamofire', '~> 3.4'
	pod 'RxSwift', '~> 2.4'
	pod 'RxCocoa', '~> 2.4'
end 

target 'RxAlamofireExample' do
	common
end

target 'RxAlamofireTests' do
	common
	pod 'OHHTTPStubs'
    pod 'OHHTTPStubs/Swift'
    pod 'RxBlocking'
end

post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['SWIFT_VERSION'] = '2.3'
    end
  end
end
