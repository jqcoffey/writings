# Personal Internet Security and Privacy

Personal security and privacy on the Internet is increasingly complicated to navigate. Threats to both are rampant and growing and even the well informed can fall prey to bad actors. In order to help myself do the best I can to protect my family's assets, I decided to jot down a few basic principles with links to relevant resources. By publishing this publicly, hopefully I can help others in some small way as well. 

Full disclosure obliges, of course. I am not in the least an expert in security and privacy matters. I am, however, someone who has been working on networked systems for over two decades and have over that time had the pleasure to work with folks who are. This has allowed me to glean enough wisdom to write this guide.

## tl;dr

* Keep all software up to date by using its auto-update functionality, **especially** your web browser
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

The single most important thing to do is to ensure all of your network connected devices are up to date with the latest security patches. This historically useful advice should be extended to include not just devices and their Operating Systems, but to all of the applications these things run.

## Password Policy

The next most important thing is to apply good password practices.  There is some debate as to what a "secure" password looks like, but it really all boils down to how long it will take someone to decrypt it vs how likely it is that you'll leave it lying around for someone to find (e.g. because it's too hard to remember).

My policy is pretty simple:
* One password for each account
* Passwords should be 16 characters or more, include mixed case, numbers and symbols
* Use some sort of password manager (I use [pass](https://www.passwordstore.org/))

The above provides the principal protections you need.  First it ensures you have passwords that will [take millions of years to crack](../resources/password_entropy.png), even by state actors.  It also means that even if [some unscrupulous service provider doesn't store passwords in an encrypted format](https://krebsonsecurity.com/2019/03/facebook-stored-hundreds-of-millions-of-user-passwords-in-plain-text-for-years/), your data breach is isolated to that provider.

If all of this sounds like too much of a headache, then at the very least have unique and different passwords for your critical accounts, in particular your email account(s), which are generally used for password recovery and two factor authentication (2FA).

### Two Factor Authentication (2FA)

Many service proivders will provide two factor authentication or 2FA, which is a way to "double check" that the account holder is really the person attempting to authenticate.  This can be done via email, SMS or dedicate "one time password" (OTP) applications, frequently installed on your cellphone.

This is an additional protection and you should use it for every service that offers it.  Of course, since most of these mechanisms work via your cellphone (and you may have your password manager on it as well), it will now become your online security's weakest link.

## Operating Systems and Applications

Go back to the early 2000's and everyone "knew" that Windows was a playground for black-hat hackers. Windows viruses and self-propagating worms were an every day fact of life back then, so much so that Bill Gates himself famously responded with his [Trustworthy Computing](../resources/bill_gates_trustworthy_computing.txt) internal memo at Microsoft.  For the security conscious amongst us it was easy enough to switch to a Macintosh--or for the more adventerous Linux or one of the [BSDs](https://openbsd.org)--to remove this class of exploits entirely, but this is no longer (and never really was) sufficient.

Probably the biggest single entry point into a computer is your web browser.  What once were simple tools for displaying text and graphics are now advanced application deployment platforms for 3rd-party developers (including the bad folks).  With [zero-day exploits](https://en.wikipedia.org/wiki/Zero-day_(computing)) targeting web browsers that run on many different OSes your choice of OS is less important than you might have thought.

So just like your OS, it is incredibly important to keep your browser up to date. If you use your OS's browser (e.g. Safari for macOS or Edge for Windows) then the system updates will take care of this for you.  Recent versions of Firefox have auto-updates on by default, but for other browsers I'm not sure and in any case it's worth a double check.

As implied above, applications as attack vectors is not anything new.  Before web browsers, attackers targeted MS Office applications like Outlook, Word and Excel to great effect.  Make sure they're up to date as well.

In fact, make sure all of your software is up to date at all times.

## Your Local Network

The first thing you should do is go out and buy a wireless router to replace the one your ISP provided you.  Without exception they are all [incredibly insecure and hackable](https://routersecurity.org/ISProuters.php).  Linksys routers are solid bets.  Buy one, change the wifi and admin passwords to something secure (see passwords, later), update it to the latest firmware (turning on auto-updates if it has them) and deactivate the wifi on your ISP provided router.

### Network Attached Storage (NAS)

Many folks like to augment their local network with a shared hard drive.  Some of these provide useful functionality such as sharing photos, music, videos as well as offering a local backup target for your computers.  The problem is (wait for it), they're all incredibly insecure, with all major vendors affected ([WD](https://nakedsecurity.sophos.com/2018/09/20/western-digital-goes-quiet-on-unpatched-mycloud-flaw/), [Synology](https://www.theregister.co.uk/2014/08/05/synologys_synolocker_crisis_its_as_bad_as_you_think/), [QNAP](https://blog.f-secure.com/new-nas-vulnerabilities-are-pretty-much-as-bad-as-they-get/)).

If you're not technically capable of putting together your own from-scratch NAS based on Linux, FreeBSD or OpenBSD (preferrably), then I recommend you use a cloud provider's storage instead.

### Smart Devices

So-called smart devices are also a major source of vulnerabilities.  After all, they're running some coder's bug-ridden software on top of some version of some OS, all of which you have no direct access to.  These are also probably connected to your local network, making them available as targets should someone hack your wifi.  While you might not care if someone sees what temperature it is inside your house, you probably would care if they connected to, say, a smart camera.

Also, that smart TV of yours?  Consumer reports has [something to say about them](https://www.npr.org/sections/thetwo-way/2018/02/07/584018673/consumer-reports-says-roku-samsung-smart-tvs-have-security-vulnerabilities?t=1555848887051).

The basic recommendation here is to--while you still can--buy "dumb" devices.  Not only will they be more reliable, but they won't let hackers into your life.  They also won't spy on you.

If you must use a smart device, you may be able to do so without it always connected to your network.

### Home Listening Devices (aka Smart Speakers)

Virtual assistants provide a wealth of hands-free functionality.  Of course, they do so by listening to everything going on in your home.  The [privacy concerns](https://en.wikipedia.org/wiki/Smart_speaker#Privacy_concerns) are obvious, though there is nothing concrete suggesting that Amazon or Google are doing anything nefarious with what it hears.  Apple, for their part appear to have the best policy of the bunch.  For a reasonable summary of policies, have a read [here](https://protonvpn.com/blog/amazon-echo-google-home-facebook-portal-apple-homepod-privacy/).

Of course, your cellphone has a microphone and a virtual assistant on it as well.

## Minimizing Your Attack Surface

A classic security technique is to minimize the number of ways someone might be able to gain access to your system.  The real-world analogy is that a building with tons of doors and windows is going to be much easier to get into than a concrete bunker with no windows and a single, steel reinforced door. With [software eating the world](https://a16z.com/2011/08/20/why-software-is-eating-the-world/) and the explosion of functionality that's come with it, this is more relevant than ever.  This is because coders are human and humans make mistakes and the more code humans write, the more mistakes there will be.  The more mistakes there are, the more bugs there are and security holes are a just another (unfortunate) class of bugs.

So, what to do?  Simply do not install any software unless you really need it and be ruthless about uninstalling applications.  Most of your data is sync'ed to someone's cloud somewhere making this less risky than you might think since you can usually get back to where you were in an app with a simple re-install.  Ymmv for more classic desktop apps of course.

## Minimize Your Data Exhaust

Much ink has been spilled on the subject of data privacy, but it all boils down to one thing: our consumer-driven economy needs you to buy things and the best way to get you to do so is by using your own data against you.

What this translates into is that pretty much every application and device you've bought--no matter how expensive--is accumulating a data profile on you and sending it back to a remote server, [occasionally in China](https://www.nytimes.com/2016/11/16/us/politics/china-phones-software-security.html)). A nasty side effect of massive amounts of data from multiple sources is that even when it's "anonymized," [it actually isn't](https://www.nytimes.com/interactive/2018/12/10/business/location-data-privacy-apps.html).

Unless you find that you really need your [fridge to tell you when you're out of milk](https://www.makeuseof.com/tag/microsoft-cortana-fridge-out-of-milk/), I suggest you avoid these things wherever possible.

The good news is that by following the advice of reducing your applications and smart devices to the bare minimum you are also reducing your data exhaust.

### Keeping a Lower Profile on the Internet

If you really want to minimize the amount of data you're giving up to large corporations/governments, you'll need to alter your usage of the Internet.  This more or less boils down to:

* Quit social media
* Use Google Alternatives ([Firefox](https://mozilla.org), [DuckDuckGo](https://duckduckgo.com), [ProtonMail](https://protonmail.com), [Here Maps](https://wego.here.com/))
* Change your [DNS configuration](https://securitytrails.com/blog/firefox-dns-over-ssl-cloudflare-resolvers)
* Consider a VPN

On the VPN topic, while it sounds seductive to have all your traffic encrypted and safe from prying eyes, you are actually giving 100% of your traffic logs to a potentially unsavory third party.  I would only suggest this if you have the technical ability to operate your own VPN.

### On Encrypted Communications

There are a bunch of platforms that provide encrypted communications, but keep in mind, encryption is a very hard topic to get right and is dependent on two parties sharing some bit of information (so-called "keys").  If any third party gets these keys, then they have access to all of your information.  To make life easy on everyone popular end-to-end encrypted chat programs handle the key generation and storage for you, but crucially this also means that they have access to your keys.  So as with VPN providers, you should trust that your communications remain encrypted only as much as you trust that 3rd party provider.

Additionally, once a message arrives at its destination it is decrypted so that the recipient may read it.  From here it can be propagated via unencrypted channels.  Thus not only must you trust the 3rd party provider but you must also trust your recipient.


## Apple Products Are Pretty Good For Most People

On both the privacy and security fronts, Apple products should be seen as the go-to choice for most consumers.  While macOS and iOS are not inherently more secure than alternatives, macOS remains less of a target than Windows (due to its miniscule market share) and iOS devices receive updates on average much faster than most Android devices and for a longer period of time.

Regarding privacy, Apple has made a big public push advocating more privacy controls and while there are still problems with what they're doing, for the time being they are primarily a hardware vendor whereas both Microsoft and Goolge have large advertising revenue streams that benefit greatly from your data.

### For the True Fanatics

If you really want to go off the grid, you should consider an old-school feature phone and running [OpenBSD](https://openbsd.org).  You'll still be tracked, your data will still be [sold by your wireless carrier](https://techcrunch.com/2019/01/09/us-cell-carriers-still-selling-your-location-data/) and you'll need to be quite technical to get OpenBSD working on your laptop, but it's about as far as you can reasonably go these days.

Oh, and be sure to quit using Google services, setup your own email, DNS, VPN, etc. servers.
