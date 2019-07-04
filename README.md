# ChromeOS Security Notes

## Account Security Checkup

https://myaccount.google.com/data-and-personalization

Ensure all activity controls are paused

![](https://github.com/rootsecdev/ChromeOS/blob/master/Screenshots/Screenshot%202019-06-29%20at%207.37.29%20AM.png)

## Activities to perform on a Chrome OS device

1. Under settings > People > Sync

Turn sync off everything except for extensions and bookmarks. I find these two settings the least privacy intrusive to get up and running if you log into a chrome browser on another device.

Under encryption options ensure you are encrypting your data with a sync passphrase created by you and not your google chrome password. 

![](https://github.com/rootsecdev/ChromeOS/blob/master/Screenshots/Screenshot%202019-06-29%20at%207.46.47%20AM.png)

## Extensions for security

1. HTTPS Everywhere

https://www.eff.org/https-everywhere

2. Privacy Badger

https://www.eff.org/privacybadger

3. Password Checkup

https://chrome.google.com/webstore/detail/password-checkup/pncabnpcffmalkkjpajodfhijclecjno

Some may wonder about this setting suggestion. For more technical details on how this operates go here >> https://security.googleblog.com/2019/02/protect-your-accounts-from-data.html

4. No Script (Caution may break websites)

https://chrome.google.com/webstore/detail/noscript/doojmbjmlfjjnbmnoijecmcbfeoakpjm

More about how this was finally ported over here >> https://www.zdnet.com/article/noscript-extension-officially-released-for-google-chrome/



### Important Flags for security

```
chrome://flags/#enable-usbguard
```
Prevents newly connected USB devices from operating at the lock screen until Chrome OS is unlocked to protect against malicious USB devices. Already connected USB devices will continue to function. – Chrome OS

## (Optional) Enable Linux Beta

This is just a running list on enabling Linux Beta if your chrome os device supports it and what I do with it. It's awesomeness!

1. Enable the Linux beta by going to settings and midway through you will find a section for Linux (beta)

  ![](https://github.com/rootsecdev/ChromeOS/blob/master/Screenshots/Screenshot%202019-07-03%20at%207.30.41%20PM.png)
  
Enabling will take you through a wizard and it will download about 300mb worth of data. It can take 5 to 10 mins to set up. 

2. One you are finished open up your terminal icon. Update your linux terminal with the following commands:

```
sudo apt-get update
```

  ![](https://github.com/rootsecdev/ChromeOS/blob/master/Screenshots/Screenshot%202019-07-01%20at%204.17.40%20PM.png)
