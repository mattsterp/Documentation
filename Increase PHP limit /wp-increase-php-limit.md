Increase PHP Memory limit – The default memory limit for WordPress is 32MB. It is very common to get Memory Size Exhausted Error with certain plugins or themes.

The fatal error message looks like:
Fatal Error: Allowed Memory size of xxxxxxxx bytes exhausted….

This type of error arises because your Host’s PHP Memory limit is quite less than what satisfies the requirements of sophisticated Wordpress  solutions and web applications.

The solution is to increase the PHP memory limit. You can follow any of these 3 tips to increase the PHP Memory limit:

CHANGE MEMORY LIMIT IN PHP.INI FILE
Editing php.ini file is the most common and easiest way to increase memory limit if you have direct access to the PHP.ini file. Many Shared hosting providers don't give you direct access to the PHP.ini file. In that case, you have to create you own PHP.ini file in the directory where your WordPress site is installed. Or you might need to contact me at your support dashboard for assistance.

Add the following line of code within your php.ini file
memory_limit = 64M 
This would increase the memory limit to 64 MB.

CHANGE MEMORY LIMIT IN WP-CONFIG.PHP FILE
This option is best for you if you don’t have direct access to php.ini file. and there is no need to create any extra file in your directory.

To increase memory limit via your websites wp-config.php file, simply access your server in your preferred method SFTP SSH etc., )(aside: a;ways makes a backup of you wp-config file always before making changes.  do not store this backup in a public accessible  location.  The recommended method is a private repository on GitHub).  add the following line of code directly above the line that says
/* That's all, stop editing! Happy blogging. */
Near the bottom of the  wp-config.php file and enter:

/* Increase PHP Limit */
define('WP_MEMORY_LIMIT', '256M');

This would increase PHP memory limit to 64MB., if you receive any error message contact me through your support dashboard. And I will increase the limit for you.  

EDIT YOUR .HTACCESS FILE

A .htaccess file is a way to configure the details of your website without the need to alter the server config files.

The period that starts the file name keeps the file hidden within the folder.  So if not visible, you will need to make sure "Show Hidden Files" is set in your IDE or hosting panel settings, but in most hosts, this is a default setting.

If you already have a .htaccess file then simply add the following code to your .htaccess file:

php_value memory_limit 64M

Some hosts don't create the .htaccess file automatically.  In such situations, you have to create it yourself to increase the PHP memory limit.  

In some cases to view these type of files, you will need to make sure "Show Hidden Files" is set in your IDE or hosting panel settings.

The location  of the .htaccess file is important. The configurations in that file will affect everything in its directory and the directories under it.

You can create the .htaccess file in a text editor (make sure to name it only .htaccess without any other extension or name) and then upload it to your site through an FTP client.  (show example)

Once you have the file uploaded and in the proper directory and the following line.

php_value memory_limit 64M
