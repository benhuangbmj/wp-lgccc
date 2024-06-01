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

function wporg_filter_content( $content ) {
	$ID = get_the_ID();
	$post = get_post($ID);
	return $post->post_status;
}
add_filter( 'the_content', 'wporg_filter_content' );
