# PHP
Loop Through Multi dimensional array and change value

$result =
array
  (
		array
			(
				array
					(
						'menu_cats' => 1,                 
						'item' => 'Introduction',
						'link' => 'needs'
					),
		
				array
					(
						'menu_cats' => 1,
						'item' => 'Needs Assessment',
						'link' => 'needs/needs.php'
					)
		
			),
		
		array
			(
				array
					(
						'menu_cats' => 2,          
						'item' => 'Introduction',
						'link' => 'knowledge'
					),
		
				array
					(
						'menu_cats' => 2,
						'item' => 'Administer Knowledge Pre-Test',
						'link' => 'knowledge/pre_test.php'
					)
			)

);

foreach($result as $key => $subarray) {
   foreach($subarray as $subkey => $subsubarray) {
      $result[$key][$subkey]['menu_cats'] = 'your string here';
   }
}
echo '<pre>'.print_r($result).'</pre>';
