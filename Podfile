# Uncomment the next line to define a global platform for your project
platform :ios, '12.0'
workspace 'CleanArchitectureSample'
#inhibit_all_warnings!

def rx_swift
    pod 'RxSwift', '~> 5.1'
end

def remote
    pod 'Alamofire'
    pod 'AlamofireImage'
    pod 'AlamofireNetworkActivityIndicator'
    pod 'RxAlamofire'
    pod 'ModelMapper'
end

target 'App' do
  project 'App/App.xcodeproj'
  use_frameworks!
  
  # Pods for App
  rx_swift
  remote
  pod 'Swinject'
  pod 'MBProgressHUD'
  pod "TTGSnackbar"

  target 'AppTests' do
    inherit! :search_paths
    # Pods for testing
  end

  target 'AppUITests' do
    # Pods for testing
  end

end

target 'Domain' do
  project 'Domain/Domain.xcodeproj'
  use_frameworks!

  # Pods for App
  rx_swift

  target 'DomainTests' do
    inherit! :search_paths
    #test_pods
  end
end

target 'Data' do
  project 'Data/Data.xcodeproj'
  use_frameworks!

  # Pods for Data
  rx_swift
  remote

  target 'DataTests' do
    inherit! :search_paths
    #test_pods
  end
end
