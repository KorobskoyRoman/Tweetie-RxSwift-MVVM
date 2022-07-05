use_frameworks!
source 'https://cdn.cocoapods.org'
inhibit_all_warnings!

abstract_target 'TweetieAbstract' do
    pod 'Alamofire'

    pod 'RxSwift'
    pod 'RxCocoa'
    pod 'RealmSwift'
    pod 'RxRealm'
    pod 'Unbox'
    pod 'Then'
    pod 'Reachability'
    pod 'RxRealmDataSources'

    target 'Tweetie' do
        platform :ios, '13.0'
        pod 'RxDataSources'
    end
    
    target 'MacTweetie' do
        platform :osx, '10.14'
    end
    
    target 'TweetieTests' do
        platform :ios, '13.0'
        pod 'RxTest'
        pod 'RxBlocking'
    end
end

post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '13.0'
    end
  end
end
