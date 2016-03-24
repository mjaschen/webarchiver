# webarchiver

The goal is to find a way to download a webpage with the following 
conditions:

1. secure, i. e. it **must** be ensured, that a downloaded webpage which is
   served by a webserver is not able to trigger parsing and executing 
   code on the server. E. g., think of a downloaded page or asset which 
   has a file extension like `.php` and contains actual PHP code. One
   solution is to disable any processing of code for the given folder,
   but this is not realizable for many users which have no access to 
   the webserver configuration (shared hosting, etc.)
2. download the complete page, including all assets that are needed for display

My current approach is using *wget* which provides the necessary features for
mirroring a webpage and its assets (images, stylesheets, etc.)
