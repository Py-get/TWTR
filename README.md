# TWTR
A clientside clone of heroku_ebooks with some options tweaked

# How to Use
Clone this repo

Create the twitter account you want your bot to use

Visit [https://dev.twitter.com/apps](https://dev.twitter.com/apps) with the same login and create an application. Make sure that your application has read and write permissions to make POST requests.

Take the consumer key (and secret) and access token (and secret) from your Twiter application and paste them into the appropriate spots in local_settings.py.

In local_settings.py, be sure to add the handle of the Twitter user you want your _ebooks account to be based on. To make your tweets go live, change the DEBUG variable to False.

Edit lines 141 and 142 of ebooks.py to a directory where you save images you want the bot to post. By default it has a 1/10 chance to post images. This can be changed by editting ODDS2 in local_settings.py

Consider changing line 92 of ebooks.py to end in a 1 not a 2. This was changed from heroku_ebooks to allow for smaller accounts but I can't speak for how reliable it is anymore.

Install [python-twitter](https://github.com/bear/python-twitter)

Run automate.py. Every 15 minutes there is a 1/3 chance (give or take) the bot will post, and a 1/10 chance it will post with an image.
