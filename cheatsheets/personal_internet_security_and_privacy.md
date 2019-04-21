# Personal Internet Security and Privacy Cheatsheet

Personal security and privacy on the Internet is increasingly complicated to navigate. Threats to both are rampant and growing and even the well informed can fall prey to bad actors. In order to help myself do the best I can to protect my family's assets, I decided to jot down a few basic principles with links to relevant resources. By publishing this publicly, hopefully I can help others in some small way as well. 

Full disclosure obliges, of course. I am not in the least an expert in security and privacy matters. I am, however, someone who has been working on networked systems for over two decades and have over that time had the pleasure to work with folks who are. This has allowed me to gleen enough wisdom to build this cheatsheet.

## tl;dr

* Keep all software up to date by using its auto-update functionality, **especially** your Web Browser
* Install the bare minimum amount of software/apps on your devices
* Never plug an unknown USB device into your computer or phone
* Consider the Apple ecosystem for your devices.  They receive frequent updates and Apple appears to be genuinely engaged on privacy and security issues.
* Encrypt all of your device's hard drives (iPhones and many Android phones are by default)
* Buy your own wireless router, keep it updated, and deactivate the WIFI on the one provided to you by your ISP
* Know that all popular home storage devices (aka NASes) are extremely insecure
* Use randomly generated, long passwords with high entropy, one for each site.  No need to change them frequently. Consider a password manager or a [yubikey](https://www.yubico.com/).
* Use two factor authentication (2FA) wherever it is offered
* Use a privacy focused browser like Firefox or Safari
* Avoid dodgy websites
* Never click on links in email (some nuance on this below)
* Use a webcam cover/slider.  Know that there is no equivalent for microphones.
* Turn off bluetooth (sorry, that means wired headphones)
* Don't buy a home listening device (e.g. Alexa, Google Assistant)
* Don't buy anything "smart" if you can avoid it
* Assume all electronically transmitted information is insecure, even over encrypted channels
* Private VPNs are ok, but you are still in the hands of a 3rd-party
* Know that your wireless carrier is tracking you and selling your location data (and VPNs won't help)
* Know that many/most apps on Android and iPhones are selling your location and demographic data
* Anonymized data can be deanonymized easily

Phew!  That's a long "too long; didn't read!"  Indeed it is a lot to take in and the fact is that it's probably incomplete (recall, I am no expert).  To depress you even further, black-hat hackers probably have the same/similar tools as the US Government, that not all vulnerabilities are known to software/device makers and finally that many of our devices never receive security updates. 

Also, it's a lot to do.  I don't do all of it myself.  I should.

# Basic Hygiene

The single most important thing to do is to ensure all of your network connected devices are up to date with the latest security patches. This historically useful advice should be extended to include not just devices and their Operating Systems, but to all of the applications they run.

## Differences between Operating Systems

Go back to the early 2000's and everyone "knew" that Windows was a playground for black-hat hackers. Windows viruses and self-propagating worms were an every day fact of life back then, so much so that Bill Gates himself famously responded with his [Trustworthy Computing](../resources/bill_gates_trustworthy_computing.txt) internal memo at Microsoft.  For the security conscious amongst us it was easy enough to switch to a Macintosh, or for the more adventerous Linux or one of the [BSDs](https://openbsd.org), to remove this class of exploits entirely, but this is no longer (and never really was) sufficient.

Probably the biggest single entry point into a computer is one's Web Browser.  What once were simple tools for displaying text and graphics are now full-fledged [Operating Systems](https://en.wikipedia.org/wiki/Chrome_OS).  With [zero-day exploits](https://en.wikipedia.org/wiki/Zero-day_(computing)) targeting all browsers it is incredibly important to keep them up to date.
