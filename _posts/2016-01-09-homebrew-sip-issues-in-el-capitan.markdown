---
published: true
title: Homebrew SIP Issues In El Capitan
layout: post
---
After upgrading to El Capitan, I ran into an issue with Homebrew while I was trying to update it. The specific error message that I kept seeing was:

                  /usr/local/bin is not writable....blah

Naturally, I went on Google and expected to fix it in couple of minutes just like any other problems. But, after looking at various suggestions and trying all the fixes & solutions that I could find, I still was not successful at solving the problem. 

The fixes that I tried were such as:

* Fixing the permissions by running:

       sudo chflags norestricted /usr/local && sudo chown $(whoami):admin /usr/local && sudo chown -R $(whoami):admin /usr/local


* Rebooting into recovery mode and then disabling SIP

* Running _brew doctor_ and running the fix suggestions

* Banging my table and shouting at my computer

* Praying and being nice to my computer

After all my efforts were to no avail, I was like, "screw it" and I uninstalled brew and reinstalled it again, while having SIP disabled. Guess what? It finally worked, but I had to reinstall all my previous brews.

I'm not saying that this is what you have to do if you are facing similar problems after upgrading to El Capitan, but if all the solutions that you try do not work, do try to uninstall and reinstall brew again. ;)