# odoo8-DailyDatabaseCopy
Copy Script Odoo v8 database for Ubuntu 14.04 Trusty Tahr

# Installation:

Preinstalled requisites: Odoo, pg_dump, 7z

Make it executable with:
chmod 755 DailyCopy.sh

Copy DailyCopy.sh to your desired path and change the "copy_path" variable with the path of your desired path

Make sure you have created "destination" folder and odoo user has permissions

Edit crontab of odoo user with "crontab -e" and add the line 
 "0 0 * * * /path/DailyCopy.sh ddbb destination odoo_user password" 

To make a daily copy of your database at 00:00, the first number are minutes (from 0 to 60) and the second numbers are hour (from 0 to 23)

If you have more than one database, add a crontab line to each database

