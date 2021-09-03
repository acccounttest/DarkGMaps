# DarkGMaps
Google maps compatible with others dark theme program, yes yet the case.
--------------
_________________


# Gmaps updates

_________________

This project is one of the continuity of a similar project named DarkChromePastelFluo but for Gmaps services only, eventually later others.
The only aim is to show maps of the current tab in a more convenient contrast acceptation, without losing the recognition of all elements possible.


# DarkChrome userscript affected

_________________

Below lines are only for new arrivals who do not know or ever used or heard about stylish/stylus(new) extension.
The extension helps to inject CSS code, the language for stylizing only, on certain parts or whole parts keeping in mind the older scripts but trying to keep the least of them possible.
The extension adds functionality that could not be permitted or allowed, style frame by accessing their content, functionality is not new and is the only way to modify a site included in others within an iframe, or script window.
The content of the script is very limited since we use a first to any destination, at the beginning we didn't need another script for all the services possible, progressively the number of incompatibilities were too high, the idea to separate the works into different scripts was necessary or there could be broken functionalities.
Most of the work about gmaps and other google domains has been updated more in this project than current, or you can ignore these updates and paste the same code parts into the gmaps script(s) only.

There is a gmap CSS file content for each domain or URL scheme composition that varies, the different themes are all made in different compatibility ways, it could be because:
1. - The country is not the same and requires other values.
1. - The URL scheme is inappropriate, even for the same countries.
1. - The implemented frame is not actually viewable with the same script or not, with the same it is overwritten(one example below)
1. - The URL service default values are not supported by this main global color conversion and/or the domain is not recognized...
1. - ...


# Codesandbox and Gmaps in it

_________________

The problem of the frame is here, it is really better viewable map using the second script, the problem is with this URL:

    https://codesandbox.io/embed/github/googlemaps/js-samples/tree/sample-style-array

The map is in a frame inherited by a different domain, not Gmaps exactly itself but the gmaps script is not triggered, usually yes, probably more the fact it's nother domain in another frame with another implementation of maps by Google, it can conduct to the original gmaps localisation.
Just the first script adds a dark transparent layer like it should on videos, the problem was the HTML tag, with the background, you can't delete the upper layer in this example with others script, example delete element with the mandatory folder of DarkChrome project.

```
Another solution is on zzz main script:
    iframe[src="https://0l6dh.sse.codesandbox.io"],html[stylus-iframe="https://codesandbox.io"],html[stylus-iframe="https://codesandbox.io"] body{
    color:inherit !important;
    background:inherit !important;
    background-color:inherit !important;
        
}
    /*the Iframe was unecessary there and empty*/
    html[stylus-iframe="https://codesandbox.io"] body iframe,html[stylus-iframe="https://codesandbox.io"] body iframe > * {
        display:  none !important;
        visibility: hidden !important;
        background:inherit !important;
    background-color:inherit !important;
    }
```


Click open and fork or embed then see if it changes, normally not.

    https://codesandbox.io/s/github/googlemaps/js-samples/tree/sample-style-array/?from-embed
    https://codesandbox.io/embed/github/googlemaps/js-samples/tree/sample-style-array
    https://0l6dh.sse.codesandbox.io/

But sometimes it's not necessary an empty iframe between other tag or the simplicity of the URL scheme, rarely like here,and the problem is not the simplicity but more the not matching shorten URL already used in blacklist and whitelist, considering the real blacklist can exist in regex only manually not in both interface access, the plugin icon menu and the script config.


The only problem with Gmaps URL is the scheme they used specifically, hopefully the rules are very simple and pretty common to all tags, the only fail in this is the mains imbricated tags, usually with all gmap script the main script can be active it's not a problem, but with a certain implementation, example in frames, the layers become too much numerous and the interaction become transparent, inative, or unrecognizable with a very low contrast difference, example with this, it is included gmap but it can conduct you to original localisation in Gservices.
So visiting this site without a zzz script is fine, but there is no other script matching its URL, so options are:
1. - Deactive zzz script temporarily, unwanted.
1. - Add another script for this domain, but the problem was not this domain, it should not need any script to be in dark mode, and it's frames too.
1. - Add CSS code in Gmaps scripts, but the main domain is not one of the Gmaps scripts, and the scripts are not detected for the frames, we could add domains for the Gmaps scripts.
1. - Blacklist the simple domain values though the menu is not appropriated and the URL is too shortened.
1. - Ideally we could add blacklist in the header part of zzz script but it's a website much embedded and reused, more its a thematic itself. 
1. - I retained the solution of the code above, paste it in a main script you use, anyway deactivating zzz is a shortcut.
Now the map is draggable and zoom is working, if you want a more visible area, just fake a movement though left and right to come to your destination, at second click let it be pressed down, try to not use zoom after this but before, else focus can be lost.

Feel free to edit any domain changes, this is the only domain and frame functionality to the rescue of the last white areas that can be found.


# GMAPS

_________________

Important to exclude some gmaps urls from zzz script for the first time, add:

`|.*google.*/maps/d/u.*` in the header part, not in Gmaps script.



