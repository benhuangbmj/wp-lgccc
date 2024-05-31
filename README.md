**List of Plugins:**

-   Easy Google Fonts
-   Quick Featured Images
-   Members

add_action('publish_post', function($post_id) {
	$my_post = array(
		'ID' => $post_id,
		'post_content' => 'Hello world!',
	);	
	wp_update_post($my_post);
});
