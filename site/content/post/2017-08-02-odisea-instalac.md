---
author: ""
date: "2017-08-02T18:54:24+02:00"
draft: false
title: "Computer install ordeal teaches lessons on error avoidance"
tags: ["geekness","FLOSS","personal"]
image: "https://farm5.staticflickr.com/4326/35919108670_f5e1f6b067_z.jpg"
comments: true     # set false to hide Disqus comments
share: true        # set false to share buttons
thumbnailImagePosition: left
thumbnailImage: //farm5.staticflickr.com/4326/35919108670_f5e1f6b067_z.jpg
coverImage: //farm5.staticflickr.com/4326/35919108670_f5e1f6b067_z.jpg
metaAlignment: center
coverMeta: out
---

Let's install a new GNU/Linux operating system in two old computers to give them a new life. After all, what could go wrong?...

<!--more-->

In my company we're always using different computers, devices, and operating systems to test scenarios, UX, and alternatives. So when one of the developers said "I need a machine with Ubuntu Server LTS to test a new feature", I said, "why not using this old MacPro 1,1 that we have sitting around collecting dust?".

Everybody seemed OK with the idea, and since I suggested it and everybody knows I like to 'tinker' with machines... I was tasked with the responsibility.

"Since I'm doing this, I might as well update the old iMac we also have sitting around", I thought. After all, I have installed GNU/Linux systems a ton of times, and since in the past it used to be a challenge, in recent years it has become easier and easier to the point of being a boring pleasure.

But I had NO IDEA of what I was getting myself into.

First I tried the iMac. I will try to make a very long story short, by listing the insane steps, errors, and lessons learned:

1. USB key with installer not recognized. Could it be the key? Let's make another one.
2. USB key not bootable. Oops, my mistake, let's make another one.
3. USB key not recognized... hmmm, this is strange. Maybe it is the USB port, let's check it.
4. Installer not recognized. What now? Oh, I see in the logs that the iMac's old bootloader will not boot from USB for a non-OSX installer. Well, I wish I knew that before. Let's try with a CD.
5. CD not readable. Well, that's normal, we all know optic media fails. Let's try another one.
6. OS needs to be 32 bits. Ooops, I forgot to check, after all this messing with peripherals and units. Let's burn another one.
7. CD not bootable. What? OK, I'm going to check my collection of "official CDs", that I've used in the past and know they work:
	a. Fedora
	b. Debian
	c. Red Hat
	d. Solaris
	e. Sabanyon
	f. Even Yellow Dog!
	h. Here it is: Ubuntu... 7.0.4. Oh, well, I can always update later
8. Finally the installer CD loads... only to display a garbled error message in multi-techno-color. But I've been there before: it's the graphics card. So let's repeat, in compatibility (extra slow) mode.
9. Error: 7vmlinuz not found. I check the CD contents. The file is there, but it has a .efi at the end. Online forums suggest to use USB and delete the file appendix. But that's not an option for me. So I have to mess with the ISO content, and brun another CD. Oh, joy.
10. Tada! It worked. Now we can update. Next one available: 7.10. OK, no problem, even if it takes 10 updates, I will get it to the current version eventually...
11. What? Error? But...? Let's research online: I see, the only unresolved issue with old Ubuntu updaters is: 7.0.4 to 7.10 in iMacs. You have to be kidding me!
12. Wait, now that we have the GNU/Linux bootloader, maybe I can skip ahead to a new version by installing anew on top of it, right? Bring in the Linux Mint 17 CD!
13. Success! After only countless hours of bashing my head against newbie forums and esoteric expert techno-blogs, I got where I wanted. 

It was totally worth it. The feeling of taming the beast, of overcoming challenges. I love it!

Now, the MacPro. I'm sure it can't be worse, right?

1. USB key with installer not recognized. Could it be the key? Let's make another one.
2. USB key not recognized... hmmm, this is strange. Maybe it is the USB port, let's check it. It is. Crap. Oh, well, I can always use the CD.
3. CD not readable. Well, that's normal, we all know optic media fails. Let's try another one.
4. Again.
5. Again. This is not normal.
6. I read online that the MacPro bootloader won't allow me to do what I want. So I install rEFInd.
7. New bootloader works, but will not boot my USBs (at all) or CDs (it recognizes them, but will not load them).
8. I research some more: that particular MacPro is 64bit, BUT the bootloader is 32bit. So, what I wanted to do was never going to work!
9. As I reasearch options (some very wacky and complex ones, believe me), my colleagues mention they do not need that after all.

I could have gotten frustrated, or angry, or stubbornly tried to make it happen regardless... but I'm too busy, and my pride is not confused by my ego any more (or so I believe), so I decide to move on to other projects, and learn the many lessons. The main one? **Triple check your assumptions**.

<div id="flickrembed"></div><div style="position:absolute; top:-70px; display:block; text-align:center; z-index:-1;">></div><script src='https://flickrembed.com/embed_v2.js.php?source=flickr&layout=responsive&input=www.flickr.com/photos/jcortell/sets/72157687091650855&sort=5&by=album&theme=default&scale=fill&limit=5&skin=default&autoplay=true'></script>