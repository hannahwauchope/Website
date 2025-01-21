## Hello
This is the github repo for the website of me and my research group.

The website is built from the Beautiful Jekyll github Website template, an incredible resource created by by [Dean Attali](https://deanattali.com), see more at the [Demo Website](https://beautifuljekyll.com/).

See the ReadMe at the Beautiful Jekyll repo (which this one is forked from) for full details.

The main modification I've made, other than specifying things within _config.yml, has been to add circles on the 'people' page. The code for this was adapted from the R Epidemics Consortium Website, [github repo here](https://github.com/reconhub/reconhub.github.io/tree/master). This involved adding the "Lists of Circles" section to the end of beautifuljekyll.css, adding list-circles.html to the _includes folder (and modifying it by splicing with code from social-networks-links.html to get all the buttons for various social links), adding People.YAML to the _data folder, and calling these from people.md.

I've also added my own domain name. I purchased it through NameCheap, then on the NameCheap website under *Manage*:
  - Under *Domain* --> *NameServers*, ensured it was set to "Namecheap BasicDNS"
  - Under *Advanced DNS* --> *Host Records*, added four A records, where 'Host' is '@', and value is: 185.199.108.153 ; 185.199.109.153 ; 185.199.110.153 ; 185.199.111.153. TTL can be 60 minutes
  - In the same place, added a final record, but this time a CNAME record. 'Host' is 'www', 'Target' is 'hannahwauchope.github.io.' (note full stop at end), TTL is 60mins
  
Then, on this github repo, under *Settings* --> *Pages*, in custom domain I added the domain www.hannahwauchope.com ('www' seems to be important), and ticked "Enforce HTTPS". This prompted github to set up a file called CNAME in the repo that just contains the text 'www.hannahwauchope.com'. It took about 24hrs for things to take effect and to stop getting error messages after the little "DNS Check in Progress" alert pops up. It also seems to take a bit after each time I update the website.
