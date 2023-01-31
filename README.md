Flutter Case 


# Command For Run FLutter IOS
1. cd ios
2. Pod init 
3. Pod install
4. flutter build ipa -v 
    noted:
        a. -v for see log when run

# Setup target iphone via pod file

post_install do |installer| \
&nbsp;installer.pods_project.targets.each do |target| \
    &nbsp;&nbsp;flutter_additional_ios_build_settings(target) \
    &nbsp;target.build_configurations.each do |config| \
      &nbsp;config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '(input your target ex: 13,0)' \
        end \
     end \
  end

# Command For build project flutter 
1. Build for Android 
    flutter build apk --release

2. Build For IOS
    flutter build ios --release
    
# case error   --no-tree-shake-icons for build IOS
 Case above because method not excute / use in method main. Flutter use metode tree shake.For solution case  add command 
 "--no-tree-shake-icons" 
 when build flutter  
 
 # case xcode version not found
    Error "cannnot find "xcodebuild""
   xcode must set version can used 
   go to Xcode->preferences->locations-> set value for command Line tools


