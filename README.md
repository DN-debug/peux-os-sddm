# Peux OS Clairvoyance

A version of sddm-clairvoyance theme modified for 
Peux OS, comes with auto-background 
change implemented along with Full/Partial Blur. 
With every login-session, a new background image 
will be shown. 

![](https://github.com/DN-debug/peux-os-sddm/blob/master/sddm-peux.png)
## Features

Things that make this version different from the original theme are auto-background changer/blur/date&time. Two of these are editable from
within the 'theme.conf' file:

1. <b>blur</b>: 
    I have implemented GaussianBlur with ShaderEffects into this theme.
    You just have to use 'true' / 'false' to enable it. 
    There is 'BlurRadius' whose value is between 0-100.

2. <b>Date and Time</b>: 
    Date and Time is visible in the mid-bottom position by default.
    To change the position, manipulate the 'relativePositionX' and 'relativePositionY'
    values in the 'theme.conf'.

#### Background Changer

The background image of the login-screen would change automatically, with a random image everytime the sddm session
is restarted. That means, if you login and then logout, you'd likely to see a different background.

## Issues and Contribution

This is not really an issue, rather an implementation constraint created by ME, that is, the pictures' path is hardcoded. I could have dynamically pulled the images from a 
folder or url but it simply is not my aim to do so as of now. <br><br>
If anyone wants, they can modify it as per their choice by either forking or cloning this repo. You could also fetch 
XML data from Bing/Yahoo/Flicker and many other sites in your implementation. <br><br> 

If you would like to contribute to this repo please do so by creating a PR. I am open to suggestions.

## Dependencies

To run this, you must have the below QT5 dependencies:

`qt5-graphicaleffects`
`qt5-quickcontrols`
`qt5-quickcontrols2`

## Procedure to Test

Follow the below steps to test it:

    1. You'd require to have "login" backgrounds directory
       inside of your '/usr/share/backgrounds/' directory.

       You may use the one that is already included in this repo:

```bash
        git clone https://github.com/DN-debug/peux-os-sddm.git
        cd peux-os-sddm
        sudo cp -r login/ /usr/share/backgrounds/
```

    2. Now, assuming that you are inside of the parent directory of the repo,
       that is 'peux-os-sddm/', you may test it from here using the below command:

```bash
        sddm-greeter --test-mode --theme sddm-peux-os-clairvoyance/
```
    
## Credits

This is the modified version of [Eayu's sddm-theme-clairvoyance](https://github.com/eayus/sddm-theme-clairvoyance) for Peux OS

