# steamfriends.info
Track your Steam friends and check who is added, deleted or renamed from your friend list.
You can host your own version for free at https://www.planethoster.com/en/World-Lite

# Installation

Replace $apikey in file crontab/GetFriendList.php line 29 with your steam api key
Replace $apikey in file include/steamauth.php line 6 with your steam api key

To get an apikey go to https://steamcommunity.com/dev/apikey

You can add multiple api keys to prevent limitation e.g. $apikey = array('1','2','3');

Replace $db = new mysqli('localhost', 'user', 'password', 'database'); in file crontab/GetFriendList.php line 14 and 31 with your database credential
Replace $db = new mysqli('localhost', 'user', 'password', 'database'); in file include/config.php line 6 with your database credential

Make sure that you also have imported the install.sql file to your database

Replace $admins = array('765XXXXXXXXXXXXX'); in file include/config.php line 29 with your steamid64 you can also add mutliple admins e.g. $admins = array('1','2','3');
They will have access to the members section

Remove the index.html, to connect to your site type example.com/login in the adress bar

You can loop trough all the members by executing php crontab/GetFriendList.php without parameter (don't use it in a cronjob except if it's for a single account or two, otherwise a while loop would be better)

# Credits

All credit goes to [Xyleme](https://steamcommunity.com/profiles/76561197960288870) for making the code and [Rysanlos](https://steamcommunity.com/profiles/76561198026039547) for maintaining it during 7 years
