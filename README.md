# Wordpress from [LocalWP](https://localwp.com/) to Docker


Export your localwp project and mount usign docker-compose file.


## Steps
1- Export your localwp project, and unzip it on this project folder.
```
    wordpress-project
    |__ app (*)
    |   |_ public   
    |   |_ sql      
    |__ .gitignore
    |__ docker-compose.yml
    |__ uploads.ini
    |__ README.md
```

2- Edit `app/public/wp-config.php` file with your docker-compose credentials.
```php
// ** Database settings - You can get this info from your web host ** //
/** The name of the database for WordPress */
define( 'DB_NAME', 'wordpress' );

/** Database username */
define( 'DB_USER', 'wordpress' );

/** Database password */
define( 'DB_PASSWORD', 'wordpress' );

/** Database hostname */
define( 'DB_HOST', 'mariadb' );

/** Database charset to use in creating database tables. */
define( 'DB_CHARSET', 'utf8' );

/** The database collate type. Don't change this if in doubt. */
define( 'DB_COLLATE', '' );        
```

3- Go to `app/sql/local.sql` and find&replace your old url with your new url. (e.g. _localhost:8000_ for this docker-compose)


## License

MIT

**Free Software, Hell Yeah!**