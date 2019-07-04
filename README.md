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

3. Download the signal desktop debian package

   https://signal.org/download/
   
   Here is the code to install in terminal as of 7/4:
   
```
   curl -s https://updates.signal.org/desktop/apt/keys.asc | sudo apt-key add -
echo "deb [arch=amd64] https://updates.signal.org/desktop/apt xenial main" | sudo tee -a /etc/apt/sources.list.d/signal-xenial.list
sudo apt update && sudo apt install signal-desktop
```
  Shown below is executing each line in terminal

  ![](https://github.com/rootsecdev/ChromeOS/blob/master/Screenshots/Screenshot%202019-07-04%20at%208.36.34%20AM.png)

  Select Y to download 

  ![](https://github.com/rootsecdev/ChromeOS/blob/master/Screenshots/Screenshot%202019-07-04%20at%208.38.28%20AM.png)

  When finished you should see the application in your Linux application section in Chrome OS

  ![](https://github.com/rootsecdev/ChromeOS/blob/master/Screenshots/Screenshot%202019-07-04%20at%209.00.34%20AM.png)

4. Install keepassx next. Keepass is a passowrd manager that is compatible with Windows, Mac OS, and Linux. It's my password manager of choice. I keep my encrypted database stored on Microsoft Onedrive. To get started type in the following code:

  ```
  sudo apt install keepassx
  ```
  
  ![](https://github.com/rootsecdev/ChromeOS/blob/master/Screenshots/Screenshot%202019-07-04%20at%209.03.15%20AM.png)
  
  I normally just download my keepass from OneDrive and run locally on Chrome OS. If I do make changes I just re-upload the   newer file back to OneDrive manually. I try and not do this often unless absolutely needed. 
  
5. Install a secure password generator in terminal if you don't want to use the keepass password generator. I user pwgen to generate secure random passwords.

  ```
  sudo apt install pwgen
  ```
  
  How to use pwgen:
  
  ```
  pwgen -help
  
  sage: pwgen [ OPTIONS ] [ pw_length ] [ num_pw ]

Options supported by pwgen:
  -c or --capitalize
        Include at least one capital letter in the password
  -A or --no-capitalize
        Don't include capital letters in the password
  -n or --numerals
        Include at least one number in the password
  -0 or --no-numerals
        Don't include numbers in the password
  -y or --symbols
        Include at least one special symbol in the password
  -s or --secure
        Generate completely random passwords
  -B or --ambiguous
        Don't include ambiguous characters in the password
  -h or --help
        Print a help message
  -H or --sha1=path/to/file[#seed]
        Use sha1 hash of given file as a (not so) random generator
  -C
        Print the generated passwords in columns
  -1
        Don't print the generated passwords in columns
  -v or --no-vowels
        Do not use any vowels so as to avoid accidental nasty words
  ```
