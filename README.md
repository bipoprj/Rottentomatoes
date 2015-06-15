# Rottentomatoes
# codepath tutorial
https://github.com/codepath/ios_guides/wiki/RottenTomatoes-Tutorial

#api key
http://api.rottentomatoes.com/api/public/v1.0/lists/movies/box_office.json?apikey=p8s4mk5kjeasmu9c6qxm5wcb

#fix code signing issue
https://github.com/CocoaPods/CocoaPods/issues/3156
adding into Podfile
```
post_install do |installer_representation|
    installer_representation.project.targets.each do |target|
        if target.to_s.include? 'Pods'
            target.build_configurations.each do |config|
                if !config.to_s.include? 'Debug'
                    config.build_settings['CODE_SIGN_IDENTITY[sdk=iphoneos*]'] = 'iPhone Distribution'
                end
            end
        end
    end
end
```

#pod install
gem install cocoapods --user-install
gem which cocoapods
#yosemite
sudo gem install cocoapods -V
sudo gem update --system 
