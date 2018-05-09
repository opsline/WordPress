# Environment Variables

The following environment variables are also honored for configuring your WordPress instance:

- `WORDPRESS_DB_HOST` (defaults to the IP and port of the linked `mysql` container)
- `WORDPRESS_DB_USER` (defaults to "root")
- `WORDPRESS_DB_PASSWORD` (defaults to the value of the `MYSQL_ROOT_PASSWORD` environment variable from the linked `mysql` container)


Optional configs:

- `WORDPRESS_DB_NAME` (defaults to "wordpress")
- `WORDPRESS_TABLE_PREFIX` (defaults to "", only set this when you need to override the default table prefix in wp-config.php)
- `WORDPRESS_AUTH_KEY`, `WORDPRESS_SECURE_AUTH_KEY`, `WORDPRESS_LOGGED_IN_KEY`, `WORDPRESS_NONCE_KEY`, `WORDPRESS_AUTH_SALT`, `WORDPRESS_SECURE_AUTH_SALT`, `WORDPRESS_LOGGED_IN_SALT`, `WORDPRESS_NONCE_SALT` (default to unique random SHA1s)

If the `WORDPRESS_DB_NAME` specified does not already exist on the given MySQL server, it will be created automatically upon startup of the `wordpress` container, provided that the `WORDPRESS_DB_USER` specified has the necessary permissions to create it.
