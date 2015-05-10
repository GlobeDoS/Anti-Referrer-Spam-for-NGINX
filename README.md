# Anti Referrer Spam for NGINX
##### by http://globe.eu/

### What does anti-referrer-spam.conf do?
> **tl;dr** It displays a 403 error (forbidden) message to every visitor/bot that comes from one of the defined urls to your page.

### Why is **referrer spam** a problem?
If you are serious about your page and your visitors intrests, at some point you probably want to use some kind of page analytics (for example http://www.google.com/analytics/ or http://piwik.org/ ). There you can see where your visitors are comming from. Recently, spammers started to use this to their advantage. They send thousend bot visitors to your page from a special page so that you will see their pae as origin. If you are curious about this huge amount of visitors, there is a chance that you type in that url and visit the spammer site. There, they advertise SEO services (*Warning: Dont buy anything there!*)
Thease so called referrer spam attacks falsifies your pages statistics - so the best solution is, instead to filter them out manually in your analytics, to block them in the first place.

### What does this snipped do and how to install it?
1. Create an folder named for example *global* inside your /nginx/ folder
   * It should look somehow like ***/etc/nginx/global/***
2. Create a file named *anti-referrer-spam.conf* inside your just created folder and paste the content as shown below
* It should look somehow like ***/etc/nginx/global/anti-referrer-spam.conf***
3. Edit your configuration file for your website located inside */sites-available/* as shown below. You have to add *`include global/anti-referrer-spam.conf;`* inside of your *`server { ... }`*

### We'd love to hear your feedback!
Please feel free to suggest improvements to the code & other spammy domains we may block. Or just leave a few kind words below :-)
