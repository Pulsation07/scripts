# MySQL import strings for Wordpress.
Go to phpmyadmin and login.

Select which database you want to change the URLs in.

Go to execute command

```
UPDATE wp_options SET option_value = REPLACE(option_value, 'https://umwa.org', 'http://localhost:8000') WHERE option_name = 'home' OR option_name = 'siteurl';
UPDATE wp_posts SET post_content = REPLACE (post_content, 'https://umwa.org', 'http://localhost:8000');
UPDATE wp_posts SET post_excerpt = REPLACE (post_excerpt, 'https://umwa.org', 'http://localhost:8000');
UPDATE wp_postmeta SET meta_value = REPLACE (meta_value, 'https://umwa.org', 'http://localhost:8000');
UPDATE wp_termmeta SET meta_value = REPLACE (meta_value, 'https://umwa.org', 'http://localhost:8000');
UPDATE wp_comments SET comment_content = REPLACE (comment_content, 'https://umwa.org', 'http://localhost:8000');
UPDATE wp_comments SET comment_author_url = REPLACE (comment_author_url, 'https://umwa.org', 'http://localhost:8000');
UPDATE wp_posts SET guid = REPLACE (guid, 'https://umwa.org', 'http://localhost:8000') WHERE post_type = 'attachment';
```
