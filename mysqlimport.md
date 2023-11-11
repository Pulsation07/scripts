# MySQL import strings for Wordpress.
Go to phpmyadmin and login.

Select which database you want to change the URLs in.

Go to execute command

```
UPDATE wp_options SET option_value = replace(option_value, 'Old URL', 'New URL') WHERE option_name = 'home' OR option_name = 'siteurl';
UPDATE wp_posts SET guid = replace(guid, 'Old URL','New URL');
UPDATE wp_posts SET post_content = replace(post_content, 'Old URL', 'New URL');
UPDATE wp_postmeta SET meta_value = replace(meta_value,'Old URL','New URL');
```
