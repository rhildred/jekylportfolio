#Light-weight, multi-platform, free and open-source software PHP development environment

Just start coding and testing on your local machine. Well ... after these simple steps. 

##Portable


##Windows

###Git

The first thing that you will need will be the git software configuration management system. Git keeps your local machine testing environment consistent with your cloud based deployment environment. Git can be downloaded [from here](https://git-scm.com/downloads). You can install Git by accepting the defaults except for these two screens.

![Use Git from Bash Only](https://res.cloudinary.com/salesucation-com-inc/image/upload/v1474945470/GitBashOnly_zcktvu.png)

![Leave line endings as is](https://res.cloudinary.com/salesucation-com-inc/image/upload/v1474945465/GitLeaveLineEndings_nqkkec.png)

###Adobe Brackets

You will use Adobe Brackets as your integrated development environment (IDE) just as you would use Visual Studio for .net development. You can download brackets [from here](http://brackets.io/). There is no need to change any of the defaults.

####Brackets Extensions

To finish up the installation you will need to launch brackets as administrator. Go to the start menu, and right mouse click over the Brackets menu item. Select the option to `Run as Administrator` (there might be a choice to access `more` options which you need to click first).

![Run Brackets as Administrator](https://res.cloudinary.com/salesucation-com-inc/image/upload/v1474985041/RunAsAdministrator_bvdvj5.png)

Extensions are added to Brackets by going to the `File/Extension Manager ...` menu item. You will need to search for the following extensions:

1. Brackets Git

![change the custom terminal command](https://res.cloudinary.com/salesucation-com-inc/image/upload/v1474985381/GitSettings_auyrjz.png)
1. Indentator
1. PHP Debugger
1. PHP Smarthints

When the extensions are all added, you will need to install our last piece! 

###PHP

You can download php [from here](http://php.net/downloads.php). I went to Windows downloads and got this one:

![PHP x64 threadsafe](https://res.cloudinary.com/salesucation-com-inc/image/upload/v1474985916/PHPx64threadsafe_eo1jcy.png)

I extracted all:

![extract all](https://res.cloudinary.com/salesucation-com-inc/image/upload/v1474986223/ExtractAll_dzjufu.png)

To this folder:

![enter image description here](https://res.cloudinary.com/salesucation-com-inc/image/upload/v1474986223/ToThisFolder_uk9pg0.png)

Once php is unzipped it needs to be linked to our environment.

####Link to Environment

There are 2 files that must be edited, as administrator, to link php to our environment.
1. Add `export PATH=/php:$PATH` to the end of the `c:/Program Files/Git/etc/profile`
![File open (not folder)](https://res.cloudinary.com/salesucation-com-inc/image/upload/v1474987045/FileOpen_yc0p1n.png)
![profile](http://res.cloudinary.com/salesucation-com-inc/image/upload/v1474987045/Profile_becfsa.png)
1. The extensions that we need must be turned on by un-commenting them in `c:\Program Files\Git\php\php.ini`
	2. Start by opening  `c:\Program Files\Git\php\php.ini-development` in the same way that you opened the `c:/Program Files/Git/etc/profile`
	3. Then do File/Save As to rename the file to php.ini.
	4. Then remove the semi colon on the lines: `; extension_dir = "ext"` (line 734), `;extension=php_curl.dll` (line 877) and `;extension=php_pdo_sqlite.dll` (line 897)


OSX(Mac)
-----


In the case of a **usb-drive environment** you will make a `brackets+git` folder that will serve as the root folder of your environment. You will install git in `bracket+git/git`. If you get portable 7zip first you can get the portable `PortableGit-1.9.5-preview20150319.7z` version and extract it to the `bracket+git/git` folder.

![brackets+git](https://rhildred.github.io/articles/phplite/bracketsgit.svg "brackets+git")

In windows git provides a `Git Bash.vbs` that we will use to run php command line tools from.

Brackets
-------

The next thing that you will need to install is adobe brackets. You [can get it here](http://brackets.io/). I picked the one without extract.

If you are running from a usb stick you will need portable brackets, which you [can get here](https://github.com/sagiegurari/brackets-portable/releases)

Brackets has quite a number of extensions built for it. There are 4 that I use for PHP:

1. Brackets Git
1. Indentator
1. PHP Debugger
1. PHP Smarthints

You can install them by searching for them in file/extension manager.

PHP
----

With PHP things get a little more complicated. If you are on windows you can get a [zip of php here](http://windows.php.net/download/) . You want the 64 bit threadsafe one.

If you are on windows you will unzip that file into the folder that git is in ... in the example `bracket+git/git/php`:

![brackets+git+php](https://rhildred.github.io/articles/phplite/bracketsgitphp.svg "brackets+git+php")

If you are on OSX you can install php with `curl -s http://php-osx.liip.ch/install.sh | bash -s 5.6`. You will need to change your path by editing `~/.bash_profile` in your home folder and adding the following line at the end `export PATH=/usr/local/php5/bin:$PATH`.

Likewise in windows you will also need to put php in your path. You can do this, using brackets, by adding to `brackets+git/git/etc/profile` the line:
`export PATH=/php:$PATH`

Now if all is well on windows or OSX you can click the git icon on the right hand edge of your brackets, click the > sign in the black rectangle, type `php --version` in the resulting shell window and see these results:

```

PHP 5.6.11 (cli) (built: Jul 10 2015 21:46:48) 
Copyright (c) 1997-2015 The PHP Group
Zend Engine v2.6.0, Copyright (c) 1998-2015 Zend Technologies
    with Zend OPcache v7.0.6-dev, Copyright (c) 1999-2015, by Zend Technologies
    with Xdebug v2.2.5, Copyright (c) 2002-2014, by Derick Rethans

```

You can give php some code to execute by starting a new file in brackets called index.php.

```
<?php
phpinfo()
?>
```
If you type in `php -S localhost:8000` you will be running a web server listening on localhost port 8000. Surfing to http://localhost:8000 in your favourite browser should yield an informational screen, similar to the above but with more detail.

###Testing

1. If you have not done so already, log in to github and navigate to `https://github.com/rhildred/wordpress-heroku`, click on the `fork` icon and get a copy of the project in your own account.
2. In your own account get the clone url:
![Get the Git Clone Url](https://res.cloudinary.com/salesucation-com-inc/image/upload/v1474989197/CloneWordpress-Heroku_xyfqxp.png)
3. Back in brackets you will create a folder and subfolder for your sandbox
4. Click clone, and paste the url. You should see code coming on to your machine.
4. When the code is there, click the black square with the `>` sign.
5. Type in `php -S localhost:8000`
6. Follow [this link](http://localhost:8000) to land on the language selection of the wordpress installation screen.


Conclusion
====
If you were able to get all of this working you have a good solid sandbox for full stack web development with php. Your web development stack is .5 gb in size, and possibly on your usb stick. Hopefully it will open up a whole new world to you.














































































































































































































4













4

4

4

4





4





4





4

4















4

4

4













4

4





4

4

4

4



4

4

4














































1

1

1



1

1
1
5













































































5









































































































































































































































































5























































































































































































































































































































































































































































































































































































































































































































3





















































































































































































 