#51-android

##Introduction
If you're developing on Ubuntu Linux, you need to add a udev rules file that contains a USB configuration for each type of device you want to use for development. In the rules file, each device manufacturer is identified by a unique vendor ID, as specified by the ATTR{idVendor} property. 
  
For more infomation,please visit<BR />     [http://developer.android.com/tools/device.html](http://developer.android.com/tools/device.html).

##System requirements
Ubuntu,Fedora or other linux systems.

##Install  
1.Copy the file "51-android.rules" to "**/etc/udev/rules.d/51-android.rules**".To Achieve it，You should be sure that you have the **root** permission.

2.Now open the console,and execute:
```bash
sudo chmod a+r /etc/udev/rules.d/51-android.rules
```
3.Then execute：
```bash
sudo service udev restart
```

4.When plugged in over USB, can verify that your device is connected by executing `adb devices` from your SDK platform-tools/ directory. If connected, you'll see the device name listed as a "device."

##License
```
Copyright (C) 2013 Snowdream Mobile <yanghui1986527@gmail.com>

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```


[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/snowdream/51-android/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

