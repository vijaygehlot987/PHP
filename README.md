# PHPThe php code can be embedded into html code just as an example given below -
basic.php

<html>
<head>
<title> Basic Example </title>
</head>
<body>
<?php
echo "This is php code embedded into html";
?>
</body>
</html>

similarly html code can be embedded in php code as follows -

example.php
<?php

echo "<b>"."using html in php"."</b>";

?>

2. Multiline comments program

<?php
/* This is a comment with multiline
Purpose: Multiline Comments Demo
Subject: PHP
*/
echo “An example with multi line comments”;
?>

3. To specify a boolean literal, use the keywords TRUE or FALSE. Both are case-insensitive.

<?php
$foo=True; //assign the value TRUE to $foo variable
?>

4. String 

<?php
$variable = “name”;
$literally = ‘My $variable will not print!\\n’;
print($literally);
$literally = “My $variable will print!\\n”;
print($literally);
?>

This will produce following result:

My name will not print!
My name will print

5 . Add to numbers program in php 

<?php
 $a=10; 
 $b=20; 
 $c=$a+$b; 
 echo "Sum: ",$c; 
 ?>

Output : sum: 30

6. Swap two number using third variable program in PHP

<?php
$a=10; 
$b=20; 
echo "Value of a: $a</br>";
echo "Value of b: $b</br>";        $temp=$a; 
$a=$b; 
$b=$temp; 
echo "Value of a: $a</br>"; 
echo "Value of b: $b</br>"; 
?>

Output:
Value of a: 10 
Value of b: 20 
Value of a: 20 
Value of b: 10

7. Even Odd number program in PHP

<?php
 $num=10;
 if($num%2==0)
 {
 echo "Even number"; 
 } 
else 
 {
 echo "Odd number";
  } 
 ?>
Output:
Even number

8. Here is the Program to list the first 15 prime numbers.

<?php  
$count = 0;  
$num = 2;  

while ($count < 15 )  

{  

$div_count=0;  

for ( $i=1; $i<=$num; $i++)  

{  

if (($num%$i)==0)  

{  

$div_count++;  

}  

}  

if ($div_count<3)  

{  

echo $num." , ";  

$count=$count+1;  

}  

$num=$num+1; 

}  
?>  

9. Factorial of a number in Php 

<?php 
$num = 4; 
$factorial = 1; 
for($x=$num; $x>=1; $x--)
 {
 $factorial = $factorial * $x;
 } 
echo "Factorial of $num is  $factorial";
?>

Output: Factorial of 4 is 24

10.  Armstrong number Program in PHP


<?php
 $num=153; 
$sum=0; 
$temp=$num; 
while($temp!=0) 
{ 
$rem=$temp%10;
$sum=$sum +$rem*$rem*$rem; $temp=$temp/10; 
}
 if($num==$sum)
{ 
 echo "Armstrong number";
 }
 else
{ 
echo "not an armstrong number"; 
} 
?>

11. Palindrome number Program in PHP


<?php 
$num = 121; 
$p=$num; 
$revnum = 0; 
while ($num != 0)
 { 
$revnum = $revnum * 10 + $num % 10;  
$num = (int)($num / 10); 
} 
if($revnum==$p) 
{ 
echo $p," is Palindrome number"; 
} 
else 
{ 
echo $p." is not Palindrome number";
} 
?>

12. Write a PHP program to get the size of a file.

<?php
$myfile = fopen("/home/students/ppp.txt", "w") or die("Unable to open file!"); 
$txt = "PHP Exercises\n"; fwrite($myfile, $txt);
$txt = "from\n"; fwrite($myfile,$txt); 
$txt = "hello World\n"; fwrite($myfile, $txt); fclose($myfile);
echo "Size of the file".filesize("/home/students/ppp.txt")."\n"; 
?>

13.Write a PHP program to remove duplicates from a sorted list.

<?php 
function remove_duplicates_list($list1){ 
$nums_unique array_values(array_unique($list1));
 return $nums_unique ;
 }
$nums = array(1,1,2,2,3,4,5,5); print_r(remove_duplicates_list($nums)); 
?>

14.Swap two number using third variable program in PHP

<?php 

$a=10; 
$b=20; 

echo "Value of a: $a</br>";
echo "Value of b: $b</br>";

$temp=$a; 
$a=$b; $b=$temp;

echo "Value of a: $a</br>";
echo "Value of b: $b</br>"; 

?>

15 . Program to simple calculator

<?php

 if(isset($_POST['sub']))
 {
  
$txt1=$_POST['n1'];                       $txt2=$_POST['n2'];     $oprnd=$_POST['sub'];

 if($oprnd=="+")  
$res=$txt1+$txt2;
else if($oprnd=="-")              $res=$txt1-$txt2;

else if($oprnd=="x")        $res=$txt1*$txt2;
else if($oprnd=="/")    $res=$txt1/$txt2;
 } 
?>

<form method="post" action=""> 
Calculator 
<br>

No1:<input name="n1" value="<?php echo $txt1; ?>"> <br>

No2:<input name="n2" value="<?php echo $txt2; ?>"> <br>

Res:<input name="res" value="<?php echo $res; ?>">
<br>

<input type="submit" name="sub" value="+">

<input type="submit" name="sub" value="-">

<input type="submit" name="sub" value="x">

<input type="submit" name="sub" value="/">

 </form>

16.  Program to find the sum of elements in an array.

<?php
 
      $arr = array(10,20,30,'a'); 
       echo array_sum($arr); 

 ?>

17. Program to split a string into an array elements based on delimiter
.
<?php 

$str = "Welcome";
$arr = explode('c',$str);          print_r($arr); 

?>

18.Program to find the product of elements in an array.

<?php

  $arr = array(10,20,30);
  echo array_product($arr); 

?>

19. Program to combine the array elements into a string with given delimiter.
<?php  

       $arr = array(9,1,2013);
       $str = implode('/',$arr);  
       echo $str;  

 ?>

20. Separate odd and even elements from array without using loop



<?php

$input = array(4, 3, 6, 5, 8, 7, 2);

function oddCmp($input)

{

    return ($input & 1);

}


function evenCmp($input)

{

    return !($input & 1);

}

$odd = array_filter($input, "oddCmp");

$even = array_filter($input, "evenCmp");

$odd = array_values(array_filter($odd));

$even = array_values(array_filter($even));

print"Odd array :\n";

print_r($odd);

print"\nEven array :\n";

print_r($even);

 
?>

21. Program to create simple Login and Logout example using sessions.

✡️login.php

 <html> 
 <head>
 <title>Login Form</title> 
 </head> 
 <body>
 <h2>Login Form</h2>
 <form method="post"   action="checklogin.php"> 
User Id: <input type="text" name="uid">
<br> 
Password: <input type="password" name="pw">
<br> 
<input type="submit" value="Login"> 
</form> 
</body> 
</html>

✡️ checklogin.php
 <?php 
 $uid = $_POST['uid'];
 $pw = $_POST['pw']; 

if($uid == 'arun' and $pw == 'arun123') 
{  
session_start(); 
$_SESSION['sid']=session_id();              header("location:securepage.php");
 } 

?> 

✡️securepage.php

 <?php 
session_start(); 

 if($_SESSION['sid']==session_id())  
{   
       echo "Welcome to you<br>";  
     echo "<a href='logout.php'>Logout
       <a>"; 
}  
else 
{   
header("location:login.php"); 
} 
?> 

✡️logout.php

<?php  
echo "Logged out scuccessfully"; session_start();  
session_destroy();  setcookie(PHPSESSID,session_id(),time()-1); 
?>

22. Program to Upload a file to the Server.

✡️ form1.php

 <html>
 <head>
 </head> 
 <body> 
<form method="post"   action="upload.php" enctype="multipart/     form-data">
 Resume : <input type="file" name="f1"> <br>
<input type="submit" value="Upload">
</form> 
</body> 
</html>

✡️ Upload.php

<?php 

if(is_uploaded_file($_FILES['f1']['tmp_name'])) 

{  
$fname = $_FILES['f1']['name'];            if(move_uploaded_file($_FILES['f1']['tmp_name'],"uploads/$fname"))

 {   
echo "Uploaded successfully";
 } 
else
 {  
echo "Not uploaded";
 }
 } 
?>

23. Program to create a New Database using PHP and Mysql

<?php
 if(! mysql_connect('servername','username','password'))
 { 
    die('Connection failed!'.mysql_error()); 
 }
$sql = "create database newdb"; if(mysql_query($sql))

{ 
 echo "Database created"; 
}
else
{ 
  echo mysql_error(); 
} 
?> 

------------------------------------------------------------- Note: When we are using XAMPP or WAMP, servername = localhost, username = root, password is empty.

24. Program to connect to the server and selecting database

<?php 
if(!mysql_connect('servername','username','password'))
 {
     die('Connection failed!'.mysql_error());
 }
      if(!mysql_select_db("dbname"))
 {  
die('Database unavailable'.mysql_error()); 
 }
 ?> 
------------------------------------------------------------- Note: When we are using XAMPP or WAMP, servername = localhost, username = root, password is empty

25. Program to Insert records into the table in Database.

<?php

 $conn =mysqli_connect('servername','username','password','databasename');

 if(!$conn) 
{
 die('Connection failed!'.mysqli_error($conn));
 } 
$sql = "INSERT INTO tablename('sno','name','pwd') VALUES('101','Surya','surya123')";
  
 if(mysqli_query($conn,$sql)) 
{  
echo "Record Inserted"; 
 } 
else 
{  
echo mysql_error();
} 
?> 
------------------------------------------------------------- Note: When we using XAMPP or WAMP, servername = localhost, username = root, password is empty.

26.Program to fetch records from the table in Database.


<?php 

$conn = mysqli_connect('servername','username','password','databasename');
 
if(!$conn) 
{  
die('Connection failed!'.mysqli_error($conn)); 
} 
$sql = "SELECT * FROM tablename";   $data = mysqli_query($conn,$sql);   while($rec = mysqli_fetch_row($data)) 
{ 
echo "$rec[0]<br>"; 
echo "$rec[1]<br>";
echo "$rec[2]<br>"; 
}
?>
 ------------------------------------------------------------- Note: When we are using XAMPP or WAMP, servername = localhost, username = root, password is empty.

27. Program to Store a image in Database

 <?php

  if(isset($_POST['sub'])) 
   
{   
 $cont =   file_get_contents($_FILES['f1']['tmp_name']);  
$type = $_FILES['f1']['type'];         $cont=addslashes($cont);  
    mysql_connect("servername","username","password"); 
mysql_select_db("dbname");   $sql="insert into tablename values ('','$cont','$type')";  
 
if(mysql_query($sql))   
echo "Inserted";   
else  
echo mysql_error();   
}
?>

 <form method="post" action="" enctype="multipart/form-data">

 <input type="file" name="f1">

Image : <input type="submit" value="Upload" name="sub"> 

</form> -------------------------------------------------------------------- Note: When we using XAMPP or WAMP, servername = localhost, username = root, password is empty.

Kishan Rami:
28. Program to Read image from Database.

 <?php

header("content-type:image/jpeg");     mysql_connect("servername","username","password"); 

mysql_select_db("databasename");  
$sql = "select * from tablename";
$data = mysql_query($sql); 
    while($rec=mysql_fetch_row($data))
   { 
     echo "$rec[1]<br>";
   }

 ?>

 ------------------------------------------------------------- Note: When we using XAMPP or WAMP, servername = localhost, username = root, password is empty.

29. Contact form using Php 

contactform.php

<html> 
<head>
</head> 
<body>
<h4>Contact Form</h4>
<form method="post "action="sendmail
.php">
 Name : <input type="text"name="uname"><br> 
Mobile No. : <input type="text" name="mobile"><br> 
Email id : <input type="text" name="email"><br> 
Message : <textarea name="message">
</textarea><br> 
<input type="submit" value="Submit">
</form> 
</body> 
</html> 

sendmail.php

<?php 
$uname = $_POST['uname']; 
$mobile = $_POST['mobile'];
$email = $_POST['email']; 
$message = $_POST['message'];

$to = "phpkish@gmail.com"; 
$subject = "Contact"; 
$message = $message."\n Name: ".$uname."\n Mobile: ".$mobile."\n Email: $email;
if(mail($to,$subject,$message))
 { 
       echo "Thank you for contacting us";
 } 
else
 {
         echo "Try again"; 
} 
?>

30. Write a PHP script which will display the colors in the following way 

<?php
$color = array('white', 'green', 'red');
foreach ($color as $c)
{
echo "$c, ";
}
sort($color);
echo "<ul>";
foreach ($color as $y)
{
echo "<li>$y</li>";
}
echo "</ul>";
?>

31. Write a PHP script to calculate and display average temperature, five lowest and highest temperatures.

<?php
$month_temp = "78, 60, 62, 68, 71, 68, 73, 85, 66, 64, 76, 63, 81, 76, 73,
68, 72, 73, 75, 65, 74, 63, 67, 65, 64, 68, 73, 75, 79, 73";
$temp_array = explode(',', $month_temp);
$tot_temp = 0;
$temp_array_length = count($temp_array);
foreach($temp_array as $temp)
{
 $tot_temp += $temp;
}
 $avg_high_temp = $tot_temp/$temp_array_length;
 echo "Average Temperature is : ".$avg_high_temp.";
sort($temp_array);
echo " List of five lowest temperatures :";
for ($i=0; $i< 5; $i++)
{ 
echo $temp_array[$i].", ";
}
echo "List of five highest temperatures :";
for ($i=($temp_array_length-5); $i< ($temp_array_length); $i++)
{
echo $temp_array[$i].", ";
}
?>

32. Write a PHP function to change the following array's all values to upper or lower case.

<?php
function array_change_value_case($input, $ucase)
{
$case = $ucase;
$narray = array();
if (!is_array($input))
{
return $narray;
}
foreach ($input as $key => $value)
{
if (is_array($value))
{
$narray[$key] = array_change_value_case($value, $case);
 continue;
}
$narray[$key] = ($case == CASE_UPPER ? strtoupper($value) : strtolower($value));
}
return $narray;
}
$Color = array('A' => 'Blue', 'B' => 'Green', 'c' => 'Red');
echo 'Actual array ';
print_r($Color);
echo 'Values are in lower case.';
$myColor = array_change_value_case($Color,CASE_LOWER);
print_r($myColor);
echo 'Values are in upper case.';
$myColor = array_change_value_case($Color,CASE_UPPER);
print_r($myColor);
?>

33. Write a PHP script which displays all the numbers between 200 and 250 that are divisible by 4.

<?php
 echo implode(",",range(200,250,4))."\n";
?>

34. Write a PHP script to get the shortest/longest string length from an array.

<?php

$my_array = array("abcd","abc","de","hjjj","g","wer");
$new_array = array_map('strlen', $my_array);

// Show maximum and minimum string length using max() function and min() function 

echo "The shortest array length is " . min($new_array) .
". The longest array length is " . max($new_array).'.';

?>

35. Write a PHP script to get the largest key in an array.


<?php

$ceu = array( "Italy"=>"Rome", "Luxembourg"=>"Luxembourg", "Belgium"=> "Brussels",
"Denmark"=>"Copenhagen", "Finland"=>"Helsinki", "France" => "Paris", "Slovakia"=>"Bratislava",
"Slovenia"=>"Ljubljana", "Germany" => "Berlin", "Greece" => "Athens", "Ireland"=>"Dublin",
"Netherlands"=>"Amsterdam", "Portugal"=>"Lisbon", "Spain"=>"Madrid", "Sweden"=>"Stockholm",
"United Kingdom"=>"London", "Cyprus"=>"Nicosia", "Lithuania"=>"Vilnius", "Czech Republic"=>"Prague", "Estonia"=>"Tallin", "Hungary"=>"Budapest", "Latvia"=>"Riga", "Malta"=> "Valetta","Austria" => "Vienna", "Poland"=>"Warsaw") ;

$max_key = max( array_keys( $ceu) ); 
echo $max_key."\n";

?>

36. Write a PHP function to floor decimal numbers with precision.

<?php
function floorDec($number, $precision, $separator)

{
$number_part=explode($separator, $number);
$number_part[1]=substr_replace($number_part[1],$separator,$precision,0);

if($number_part[0]>=0)
{
$number_part[1]=floor($number_part[1]);}
else
{
$number_part[1]=ceil($number_part[1]);
}

$ceil_number= array($number_part[0],$number_part[1]);
return implode($separator,$ceil_number);
}
print_r(floorDec(1.155, 2, ".")."\n");
print_r(floorDec(100.25781, 4, ".")."\n");
print_r(floorDec(-2.9636, 3, ".")."\n");
?>

37. Write a PHP script to sort the following array by the day (page_id) and username.

<?php
$arra[0]["transaction_id"] = "2025731470"; 
$arra[1]["transaction_id"] = "2025731450"; 
$arra[2]["transaction_id"] = "1025731456"; 
$arra[3]["transaction_id"] = "1025731460"; 

$arra[0]["user_name"] = "Sana"; 
$arra[1]["user_name"] = "Illiya"; 
$arra[2]["user_name"] = "Robin"; 
$arra[3]["user_name"] = "Samantha"; 

//convert timestamp to date 
function convert_timestamp($timestamp){ 
    $limit=date("U"); 
    $limiting=$timestamp-$limit; 
    return date ("Ymd", mktime (0,0,$limiting)); 
} 

//comparison function 
function cmp ($a, $b) { 
    $l=convert_timestamp($a["transaction_id"]); 
    $k=convert_timestamp($b["transaction_id"]); 

    if($k==$l){ 
        return strcmp($a["user_name"], $b["user_name"]); 
    }
else{ 
        return strcmp($k, $l); 
    } 
} 

//sort array 
usort($arra, "cmp"); 

//print sorted info 
while (list ($key, $value) = each ($arra)) 
{ 
    echo "\$arra[$key]: "; 
    echo $value["transaction_id"]; 
    echo " user_name: "; 
    echo $value["user_name"]; 
    echo "\n"; 
} 
?>

39. Write a PHP script to count the total number of times a specific value appears in an array.

<?php
function count_array_values($my_array, $match) 
{ 
    $count = 0; 
    
    foreach ($my_array as $key => $value) 
    { 
        if ($value == $match) 
        { 
            $count++; 
        } 
    } 
    
    return $count; 
} 

$colors = array("c1"=>"Red", "c2"=>"Green", "c3"=>"Yellow", "c4"=>"Red");

echo "\n"."Red color appears ".count_array_values($colors, "Red"). " time(s)."."\n"; 
?>

40. Write a PHP a function to remove a specified duplicate entry from an array.


<?php
function array_uniq($my_array, $value) 
{ 
    $count = 0; 
    
    foreach($my_array as $array_key => $array_value) 
    { 
        if ( ($count > 0) && ($array_value == $value) ) 
        { 
            unset($my_array[$array_key]); 
        } 
        
        if ($array_value == $value) $count++; 
    } 
    
    return array_filter($my_array); 
} 
$numbers = array(4, 5, 6, 7, 4, 7, 8);

print_r(array_uniq($numbers, 7));
?>

41.Write a PHP script to count the total number of times a specific value appears in an array.

<?php
function count_array_values($my_array, $match) 
{ 
    $count = 0; 
    
    foreach ($my_array as $key => $value) 
    { 
        if ($value == $match) 
        { 
            $count++; 
        } 
    } 
    
    return $count; 
} 

$colors = array("c1"=>"Red", "c2"=>"Green", "c3"=>"Yellow", "c4"=>"Red");

echo "\n"."Red color appears ".count_array_values($colors, "Red"). " time(s)."."\n"; 
?>

42. Write a PHP script to trim all the elements in an array using array_walk function.

<?php
$colors = array( "Red ", " Green", "Black ", " White "); 
print_r($colors);
array_walk($colors, create_function('&$val', '$val = trim($val);')); 
print_r($colors);
?>

43. Write a PHP script to delete a specific value from an array using array_filter() function.


<?php

 $colors = array('key1' => 'Red', 'key2' => 'Green', 'key3' => 'Black');
$given_value = 'Black';
print_r($colors);

$new_filtered_array = array_filter($colors, function ($element) use ($given_value)
 { 
     return ($element != $given_value);
}
      print_r($filtered_array);
      print_r($new_filtered_array);
?>

44. Write a PHP a function to remove a specified duplicate entry from an array.

<?php
function array_uniq($my_array, $value) 
{ 
    $count = 0; 
    
    foreach($my_array as $array_key => $array_value) 
    { 
        if ( ($count > 0) && ($array_value == $value) ) 
        { 
            unset($my_array[$array_key]); 
        } 
        
        if ($array_value == $value) $count++; 
    } 
    
    return array_filter($my_array); 
} 
$numbers = array(4, 5, 6, 7, 4, 7, 8);

print_r(array_uniq($numbers, 7));
?>

45. Write a PHP program to generate an array with a range taken from a string.

<?php
function string_range($str1) 
{
  preg_match_all("/([0-9]{1,2})-?([0-9]{0,2}) ?,?;?/", $str1, $a);
  $x = array ();
  foreach ($a[1] as $k => $v) 
  {
    $x  = array_merge ($x, range ($v, (empty($a[2][$k])?$v:$a[2][$k])));
  }
  return ($x);
}
$test_string = '1-2 18-20 9-11';
print_r(string_range($test_string));
?>
@php_program

46. Write a PHP program to convert word to digit.

<?php
function word_digit($word) {
    $warr = explode(';',$word);
    $result = '';
    foreach($warr as $value){
        switch(trim($value)){
            case 'zero':
                $result .= '0';
                break;
            case 'one':
                $result .= '1';
                break;
            case 'two':
                $result .= '2';
                break;
            case 'three':
                $result .= '3';
                break;
            case 'four':
                $result .= '4';
                break;
            case 'five':
                $result .= '5';
                break;
            case 'six':
                $result .= '6';
                break;
            case 'seven':
                $result .= '7';
                break;
            case 'eight':
                $result .= '8';
                break;
            case 'nine':
                $result .= '9';
                break;    
        }
    }
    return $result;
}

echo word_digit("zero;three;five;six;eight;one")."\n";
echo word_digit("seven;zero;one")."\n";
?>

34. Write a PHP program to check if the bits of the two given positions of a number are same or not.

<?php
function test_bit_position($num, $pos1, $pos2) {
   $pos1--;
   $pos2--;
   $bin_num = strrev(decbin($num));
   if ($bin_num[$pos1] == $bin_num[$pos2]) {
     return "true";
   } else {
     return "false";
   }
}
echo test_bit_position(112,5,6)."\n";
?>

35. Write a PHP program to print out the multiplication table upto 6*6.

<?php
for ($i = 1; $i < 7; $i++) {
  for ($j = 1; $j < 7; $j++) {
     if ($j == 1) {
       echo str_pad($i*$j, 2, " ", STR_PAD_LEFT);
     } else {
       echo str_pad($i*$j, 4, " ", STR_PAD_LEFT);
     }
  }
  echo "\n";
}
?>

36. Write a PHP program that multiplies corresponding elements of two given lists.

<?php

function multiply_two_lists($x, $y)
 {
    $a = explode(' ',trim($x));
    $b = explode(' ',trim($y));
    foreach($a as $key=>$value) 
 {
        $output[$key] = $a[$key]*$b[$key];
  }
    return implode(' ',$output);
 }
echo multiply_two_lists(("10 12 3"), ("1 3 3"))."\n";
?>
