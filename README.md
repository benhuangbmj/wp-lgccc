**List of Plugins:**

-   Easy Google Fonts
-   Quick Featured Images
-   Members

add_filter("category_save_pre", function($category) {
	$id = get_the_ID();
	$status = get_post_status($id);
	if ($status == "private") {
		return array(8);
	} else {
		return $category;
	}
});
