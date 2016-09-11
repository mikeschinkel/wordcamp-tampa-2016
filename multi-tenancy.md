#No More Cowboy Coding!

**_AKA Easy Local WordPress Development_**

_Presented by Mike Schinkel_

#Multi-Tenancy
*IMPORTANT: This is not complete yet.*

1. Create `example.box` and `wordcamp-tampa.dev` folders in `www`
2. Copy `content` into `example.box`
3. Move `content` into `wordcamp-tampa.dev`
4. `WP_CONTENT_*`

	FROM:


		define( 'WP_CONTENT_DIR', __DIR__ .'/content' );
		define( 'WP_CONTENT_URL', 'http://' . APP_DOMAIN . '/content' );

	TO:

		define( 'WP_CONTENT_DIR', __DIR__ . '/' . APP_DOMAIN . '/content' );
		define( 'WP_CONTENT_URL', 'http://' . APP_DOMAIN . '/' . APP_DOMAIN . '/content' );

5. Table Prefix

		if ( ! isset( $table_prefix ) ) {
		    if ( ! file_get_contents(  __DIR__ .'/' . APP_DOMAIN . '/TABLE_PREFIX' ) ) {
			    $table_prefix = 'wp_';
		    } else {
			    $table_prefix = file_get_contents(  __DIR__ .'/' . APP_DOMAIN . '/TABLE_PREFIX' );
		    }
	    }
	
6. `Vagrantfile`

	FROM:
	    
		config.hostsupdater.aliases = [
            "adminer.example.box",
            "mailhog.example.box"
        ]
    
	TO:
	
		config.hostsupdater.aliases = [
            "adminer.example.box",
            "mailhog.example.box",
     	    "wordcamp-tampa.dev",
            "adminer.wordcamp-tampa.dev",
            "mailhog.wordcamp-tampa.dev"
        ]

7. Uploads Directory

8. Database
