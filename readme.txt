//remove body class

add_filter('body_class', function (array $classes) {
    if (in_array('class_name', $classes)) {
      unset( $classes[array_search('class_name', $classes)] );
    }
  return $classes;
});

// Add specific CSS class by body.
 add_filter( 'body_class', function( $classes ) {
    return array_merge( $classes, array( 'class-name' ) );
} );

Source: https://stackoverflow.com/questions/7799089/remove-wordpress-body-classes
