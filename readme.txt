=== Flickr field for Advanced Custom Fields (ACF) ===

== Description ==

The Flickr Field will grant you the ability to include photos, sets and galleries from your Flickr account. After selecting which image formats you wish to use the plugin will generate the flickr image urls. This plugin is an add-on for the Advanced Custom Fields WordPress plugin.

See the installation tab for more info.

== Installation ==

1. Make sure you have Advanced Custom Fields **v4** or **v5** installed. Get it at http://www.advancedcustomfields.com/. 
2. Upload the `flickr field` directory to the `/wp-content/plugins/` directory
3. Activate the plugin through the 'Plugins' menu in WordPress

Usage Example (in PHP):

**Getting the contents of a photostream and looping through the results**

	$flickr_photostream = get_field(FIELD_NAME);

	if (isset($flickr_photostream['items'])) {
		foreach ($flickr_photostream['items'] as $id => $photo) {
			echo '<a href="' . $photo['large'] . '" title="' . $photo['title'] . '"><img src="' . $photo['thumb'] . '" /></a>';
		}
	}

**Getting the contents of a set and looping through the results**

	$flickr_set = get_field(FIELD_NAME);

	if (isset($flickr_set['items'])) {
		foreach ($flickr_set['items'] as $id => $photos) {
			foreach ($photos as $photo) {
				echo '<a href="' . $photo['large'] . '" title="' . $photo['title'] . '"><img src="' . $photo['thumb'] . '" /></a>';
			}
		}
	}

== Screenshots ==

1. Setting up the field
2. Selecting a photo set
3. Selecting individual photos from your photostream

