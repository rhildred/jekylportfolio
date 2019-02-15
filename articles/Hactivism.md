Hacktivism
==========

> working toward social change by combining programming skills with critical thinking
> [Wikipedia](http://en.wikipedia.org/wiki/Hacktivism)

If you send an email to the [email address](mailto://onwardwillow@netscape.net) at the bottom of Lorri Sauve's web page it will bounce! Yet the program she directs ... Better Beginnings, Better Futures, Guelph is still going strong. Lorri has a pain that she is trying to cure. She needs to be able to have a website that accurately reflects the vibrant nature of her program that she and her team can update.

![Happy Kids](http://bbbf.ca/Portals/_default/Skins/Nukeville.Morpheus/nv_ipi/r2/1.png "image from front page of bbbf.ca")

The current website, like those of many volunteer organizations was made by a volunteer. It was updated by an admin assistant. Both of these people are no longer available to the organization and now Better Beginnings are stuck with outdated information on their site. I have been thinking (I hope critically) about this problem and my approach to web development as an instructor at Conestoga College, whom Lorri approached to solve her problem.

I love my trade. I love that it is a learning trade, and I love to learn and work with new things. I don't want the new website to be the same old, hard to update, story though. So how can the Conestoga team make sure? Is there still a role for my students and I to apply what we are learning to a site that can be maintained by someone without the same background? There is. Our role as hactivists is to apply the best of our abilities in making the site look exactly the way that Lorri and her team want it to. To apply our skills to making the site responsive and accessible. Yet to deploy the site using common denominator technology.

Common denominator is [Wordpress](https://wordpress.com/). According to Wordpress they power 23% of the internet. Even after we are long done getting Lorri's site working she should be easily able to find people that know Wordpress. Better yet, there may be someone that is already involved with the program with an apptitude for doing this kind of work. So let's just set the site up as https://bbbfGuelph.wordpress.com and be done with it. Not so fast. Lorri already has a domain name, email addresses .... The free https://bbbfGuelph.wordpress.com doesn't quite meet her needs. We could pay for a wordpress.com site with a custom domain address, or there is another way that should be as maintainable, but provides lots more control.

The other way that I am describing is http://pagodabox.com. Pagodabox is a cloud provider that specializes in PHP, the language that Wordpress is written in. It probably isn't an issue for Better Beginnings, Better Futures Guelph, but there is [an article on their homepage](https://pagodabox.com/case-studies/scale-wordpress-case-study) about them scaling to 500,000 page views a day. They are a serious cloud provider that has been around for a while and at .1% of the volume of requests host for free. As well as scaling they provide sftp access to the code, which is helpful for portability or debugging. Combining pagodabox hosting with Cloudflare content delivery network gives a performance boost and also free ssl.

SSL is important, because currently Google is page ranking SSL pages higher than insecure pages. This will have immediate impact on the people that need the services of Better Beginnings, Better Futures being able to find them. A free secure website that can be easily changed, easily found and is free at these service levels is a way to get the word out about the real social change agent, Better Beginnings, Better Futures and their 2.5 to 1 payback. By giving them a new website like this, we are just moving technology out of the way of the social change that they provide.