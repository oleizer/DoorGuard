platform :ios, '11.0'

def unit_test_libs
    pod 'Quick'
    pod 'QuickSwiftCheck'
    pod 'Nimble'
end

def analytics
  pod 'Crashlytics'
  pod 'Fabric'
end

def networking
  pod 'Moya'
  pod 'PromiseKit'
end

def common_pods
  pod 'SnapKit'
  networking
end

target 'DoorGuard' do
  use_frameworks!
  common_pods
  analytics
  target 'DoorGuardTests' do
    inherit! :search_paths
    unit_test_libs
  end
end

post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
    end
  end
end