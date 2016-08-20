#Breeze

Breeze is a customisable theme, based on the theme of the same name, built to enhance the experience of browsing web directories. It uses the `mod_autoindex` Apache module—and some CSS—to override the default style of a directory listing.

##Features

Breeze may be basic, but it gives you a great deal of creative freedom when styling your directory.

* Style your directory listing with CSS.
* Make it pop with Javascript or jQuery.
* Add welcome messages, download instructions or copyright notices.
* Add custom mime type icons (requires editing the `.htaccess` file)

_Sadly, visual style is all you can work with. It's not possible to alter the generated table structure of the listing directory with Breeze._

##Installation

Breeze requires an Apache(2.2.11+) enabled HTTP server.

Let's assume you have a folder named `share` in your server root directory (the path thus being `http://mywebsite.com/share`) that you'd like to use as your listing directory:

* [Download](https://github.com/gustawho/breeze-apache-dirs/archive/master.zip) and unzip Breeze
* Copy and paste the contents of the `/breeze-apache-dirs` folder to your `/share` folder.
* Edit `htaccess.txt` (now in the `/share` folder) and update all instances of paths marked with *{FOLDERNAME}* to point to your site root.

So...

    AddIcon /{FOLDERNAME}/theme/icons/gif.png .gif

Should be changed to...

    AddIcon /share/theme/icons/gif.png .gif

* Once done, rename `htaccess.txt` to `.htaccess` in both the `/share` and `/share/theme` folders.

##Breeze themes

If you'd like to alter the default Breeze theme, look in the `/theme` folder and you'll find the following files:

* `header.html`
* `footer.html`
* `style.css`

Edit these as you would any other HTML or CSS file.

Adding your own icons is a little more involved. You'll need to edit the main Breeze `.htaccess` file. Look for the following as an example:

    AddIcon /{FOLDERNAME}/theme/icons/gif.png .gif

The above rule will assign an icon named `gif.png` from the directory `/{FOLDERNAME}/theme/icons/` to any file with the `.gif` extension.

This URL path is relative to your site's root.

##Mime Types

The default Breeze theme has icons in place for the following mime types:

    .aif .aif .asf .asx .avi .bin .c .css .csv .dmg .doc .docm .docx .dot .dotm .eps .flv .gif 
    .htm .html .ico .iff .jar .jpeg .jpg .js .json .log .m3u .m4a .md .mid .mov .mp3 .mp4 .mpa 
    .mpg .msg .mwa .odt .pages .pdf .pkg .png .ps .psd .ra .rar .rb .rm .rss .rtf .shtml 
    .sql .srt .swf .tex .tiff .txt .vob .wav .wmv .wpd .wps .xhtml .xlam .xlr .xls .xlsm .xlsx 
    .xltm .xltx .xml .zip


##Credits

Breeze owes it's existence to the amazing Apaxy by [Lars Jung](https://twitter.com/lrsjng). Had I not seen this, I would never have looked into making my own (probably way less useful) version.

[Breeze Icons](http://tiheum.deviantart.com/art/Faenza-Icons-173323228) are used in the `breeze` theme.
