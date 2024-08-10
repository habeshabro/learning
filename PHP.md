```php
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <?php
	    $charName = "John";
	    $charAge = 35;
	    $friends = array("a", "b", "c");
	    echo $friends[0];
	    $associativeArray = array("Jim"=>"A", "Pam"=>"B")
	    //$associativeArray["Jim"] = "A"
	    echo "<h1>Hello $charName</h1>";
	    strtoupper();
	    strtolower();
	    strlen();
	    str_replace(x, y, $hhh)  // replace x with y in $hhh 
	    substr($hhh, 2, 4) // grab 4 starting from 2
    ?>
</body>
	<form action="this.php" method="get">
		<input type="text" name="userName">
		<input type="checkbox" name="fruits[]" value="apple">
		<input type="checkbox" name="fruits[]" value="orange">
		<input type="submit">
	</form>
	<?php
		$_GET["userName"]
		$_POST["password"] // use post instead of get in form method
		$fruits = $_POST["fruits"]
		function func($varA){
			echo "hello $varA";
		}
		func("Dude");
		if ($isMale) {
			echo "You are male";
		} //elseif else && ||
		switch($var){
			case "A":
				echo "cc";
				break;
			default:
				echo "jdkfjdkjf";
		}
		$index=0;
		while($index<5){
			echo $index;
			$index++;
		}
		for($i=0; $i < count($smArray); $i++){
			echo "$smArray[$i] <br>";
		}
		class Book = {
			public $pages;
			private $author;
			function __construct($aAuthor, $aPages){
				$this->author = $aAuthor;
				$this->pages = $aPages;
			}
			function isLong(){
				if($pages >= 500){
					return "very";
				}
				else {
					return "not";
				}
			}
		}
		class GoodBook extends Book {
		} 
		$book1 = new Book("a", 20);
		$book1->author = "J.K Rowling"
		echo "$book->title is $book->isLong() long"
	?>	
	<?php include="footer.php" ?>
</html>
```

```sh
	php -s localhost:5000
```