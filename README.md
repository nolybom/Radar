# [Radar](https://github.com/SaifurRahmanMohsin/Radar) #
GeoLocation component for determining closest path to user location for OctoberCMS

# What is it #
A growing organization will have more than one branch to serve it's customers. This component makes it easy for customers to locate the nearest branch of your organization. It uses Google's distance matrix API to determine the closest of several branches to the customer's location and direct the user to find the right way to the nearest branch.

## Installation ##
Until this plugin is added to the market place, you will have to use the following method to install it:
```
cd /your/october/project/plugins/folder
mkdir -p mohsin
cd $_
wget https://github.com/SaifurRahmanMohsin/Radar/archive/master.zip
unzip master
rm $_
mv Radar-master radar
```
Logout from your backend and login again. This will create the necessary tables for the plugin to work. You have now installed Radar!


## Quick Start ##
* Goto [Google Developer Console](http://console.developers.google.com/), create or select your project. Select the APIs tab and enable the **Distance Matrix API**. Now, select the Credentials tab and generate a browser key. Add your domain in the allowed referers.

* Add the API Key in Radar settings. Now click on Radar and add the addresses of your organization's destinations.

* Add the component to your project (best to use in the contact / locate us page). Enjoy!

# Where can RADAR be used? #
* Brand websites so that users can find the closest branch / outlet to their preferred brand.

* Emergency services web app such as hospital, police station so that user can find the one nearest to them.

## Future Enhancements ##
* Toggle switch to use HTML5 Geolocation API rather than getting user address as input.

* Group ID component dropdown attribute to support multiple organizations.

## Limitations ##
* In case the data matrix API quota limit hits, or some other error occurs it pushes the user to the first address in the destinations list. This is a fallback to make sure the user doesn't feel that the web app is broken. The same behavior may be experienced if the data matrix API key is not set correctly in the Radar settings page.

* The maps in the backend and the search field use Google Maps APIs Geocoders. These are [not as effective as google maps](https://developers.google.com/maps/faq#geocoder_differences) and certain places might not show up on search. You may manually add the Formatted Address field with the place name after locating the place in [Google Maps](http://maps.google.com) . This data will appear in your browser's address bar in the format `https://maps.google.com/maps/place/FORMATTED_ADDRESS/@LATITUDE,LONGITUDE`. The place name and address can be found in the description box of the map place marker. The component relies mainly on FORMATTED_ADDRESS only, other fields may be ignored.

## Credits ##

#### The developers of October CMS ####
[Alexey Bobkov and Samuel Georges](http://octobercms.com) for OctoberCMS and the [Geolocation Widget](https://github.com/responsiv/geolocation-plugin) whose code has been ported into this plugin.
