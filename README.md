1.﻿CREATE A FORM WITH THE ELEMENTS OF TEXTBOXES, RADIO BUTTONS, CHECKBOXES, AND SO ON. WRITE JAVASCRIPT CODE TO VALIDATE THE FORMATE IN EMAIL AND MOBILE NUMBER IN 10 CHARACTERS, IF A TEXTBOX HAS BEEN LEFT EMPTY, POPUP AN ALERT INDICATING WHEN EMAIL, MOBILE NUMBER AND TEXTBOX HAS  BEEN LEFT EMPTY.
<html>
<head>
<title>Form validation</title>
<script>
function validateForm()
{
var email=document.forms["myForm"]["email"].value;
var mobile=document.forms["myForm"]["mobile"].value;
var name=document.forms["myForm"]["name"].value;
var emailRegex=/^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,4}$/;
var mobileRegex=/^[0-9]{10}$/;
if(name==" ")
{
alert("Name must be filled out");
return false;
}
if(!emailRegex.test(email))
{
alert("Invalid email format")
return false;
}
}
</script>
</head>
<body>
<form name="myForm" onsubmit="return validateForm()"method="Post">
Name:<input type="text" name="name"><br><br>
Email:<input type="text" name="email"><br><br>
Mobile:<input type="text" name="mobile"><br><br>
Gender:
<input type="Radio" name="gender" value="Male">Male
<input type="Radio" name="gender" value="Female">Female<br><br>
Hobbies:
<input type="Checkbox" name="Hobby1" value="Reading">Reading
<input type="Checkbox" name="Hobby2" value="Traveling">Traveling<br><br>
<input type="Submit" value="Submit">
</form>
</body>
</html>
﻿
OUTPUT:

﻿
2.﻿DEVELOP AN HTML FORM, WHICH ACCEPTS ANY MATHEMATICAL EXPRESSION. WRITE JAVASCRIPT CODE TO EVALUATE THE EXPRESSION AND DISPLAY THE RESULT.
<html>
<head>
<title>Math Expression Evalutor</title>
</head>
<body>
<form id="mathForm">
<label for="expression">Enter Mathematical Expression:</label>
<input type="text" id="expression" name="expression">
<input type="button" value="Evaluate" onclick="evaluateExpression()">
</form>
<div id="result"></div>
<script>
function evaluateExpression()
{
try
{
var expression=document.getElementById('expression').value;
var result=eval(expression);
document.getElementById('result').innerText='Result:'+result;
}
catch(error)
{
document.getElementById('result').innerText='Invalid expression';
}
}
</script>
</body>
</html>
﻿
﻿
﻿
﻿
OUTPUT:

﻿
3. CREATE A PAGE WITH DYNAMIC EFFECTS WRITE THE CODE TO INCLUDE LAYERS AND BASIC ANIMATIONS.
<html>
<head>
<title>Basic Animation</title>
<style>
#layer1{Position:absolute;top:50px;left:50px;}
#layer2{Position:absolute;top:50px;left:400px;}
#layer3{Position:absolute;top:50px;left:800px;}
</style>
<script type="text/javascript">
function moveimage(layer)
{
var top=window.prompt("Enter top value");
var left=window.prompt("Enter left value");
document.getElementById(layer).style.top= top+'px';
document.getElementById(layer).style.left= left+'px';
}
</script>
</head>
<body>
<div id="layer1"> <img﻿src="ball.jpg" onclick="moveimage('layer1')" alt="MyImage"/></div>
<div id="layer2"> <img﻿src="ball.jpg" onclick="moveimage('layer2')" alt="MyImage"/></div>
<div id="layer3"> <img﻿src="ball.jpg" onclick="moveimage('layer3')" alt="MyImage"/></div>
</body>
</html>
﻿
OUTPUT:

﻿

﻿
﻿
﻿
﻿
﻿

﻿

﻿
﻿
﻿
﻿
﻿
﻿
﻿
﻿
4. WRITE THE JAVASCRIPT CODE TO FIND THE SUM OF N NATURAL NUMBERS. (USERDEFINED FUNCTION).
<html>
<head>
<title>Sum of n numbers</title>
<script type="text/javascript">
function Sum()
{
var n=prompt("Enter a number",0);
var num=parseInt(n);
var sum=0;
for(i=1; i<=num; i++)
{
sum=sum+i;
}
document.writeln("Sum of " + num +" natural numbers: " + sum);
}
</script>
</head>
<body>
<center><h1>Finding sum of natural numbers using javascript</h1>
<input type="button" onclick="Sum()" value ="Sum"/>
</center>
</body>
</html>
﻿
OUTPUT:



﻿

﻿
﻿
﻿
﻿

﻿
5. CREATE A JAVASCRIPT CODE BLOCK USING ARRAYS AND GENERATE THE CURRENT DATE IN WORDS, THIS SHOULD INCLUDE THE DAY, MONTH AND YEAR.
<html>
<title>Current Date in Words</title>
<head>
</head>
<body>
<h2>Current Date in Words</h2>
<p id="dateInWords"></p><script>
const﻿daysOfWeek = [ "Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday" ];
const﻿monthsOfYear = [ "January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"];
const﻿currentDate = new Date();
const day=daysOfWeek [currentDate.getDay()]; const month = monthsOfYear [currentDate.getMonth()];
const year = currentDate.getFullYear();
const﻿currentDateInWords = ${day},  ${month}  ${currentDate.getDate()},  ${year};
document.getElementById('dateInWords').textContent = "Current date in words: " + currentDateInWords;
</script>
</body>
</html>
﻿
OUTPUT:

6. CREATE A FORM FOR STUDENT INFORMATION. WRITE A JAVASCRIPT CODE TO FIND TOTAL, AVERAGE, RESULT AND GRADE.
<html>
<head>
<title>Student Information Form</title>
<script>
function calculateResult()
{
var math=parseFloat(document.getElementById('math').value);
var science=parseFloat(document.getElementById('science').value); 
var english=parseFloat(document.getElementById('english').value);
var totalMarks=math+science+english;
var average=totalMarks/3;
var result=(math>=35 && science>=35 && english>=35)?"Pass":"Fail";
var grade;
if(average>=90)
{
grade='A+';
}
else if(average>=80)
{
grade='A';
}
else if(average>=70)
{
grade='B';
}
else if(average>=60)
{
grade='C';
}
else if(average>=50)
{
grade='D';
}
else
{
grade='F';
}
document.getElementById('totalMarks').value=totalMarks.toFixed(2);
document.getElementById('average').value=average.toFixed(2);
document.getElementById('result').value=result; 
document.getElementById('grade').value=grade;
}
</script>
</head>
<body>
<h2>Student Information</h2>
<form>
Math: <input type="number" id="math"><br><br>
Science: <input type="number" id="science"><br><br>
English: <input type="number" id="english"><br><br>
<input type="button" value="Calculate" onclick="calculateResult()">
</form>
<br>
<h2>Result Details</h2>
Total Marks: <input type="text" id="totalMarks" readonly><br><br>
Average: <input type="text" id="average" readonly><br><br>
Result: <input type="text" id="result" readonly><br><br>
Grade: <input type="text" id="grade" readonly>
</body>
</html>
﻿
OUTPUT:


﻿
7. CREATE A FORM FOR EMPLOYEE INFORMATION. WRITE JAVASCRIPT CODE TO FIND DA, HRA, PF, TAX, GROSS PAY, DEDUCTION AND NET PAY.
<html>
<head>
<script type="text/javascript">
function show()
{
var name=document.getElementById("txtname").value;
var num=document.getElementById("txtnum").value;
var sal=parseInt(document.getElementById("txtsal").value);
var hra=(sal*40)/100;
var da=(sal*60)/100;
var gross=sal+hra+da;
var pf=(sal*13)/100;
var tax=(sal*20)/100;
var deduct=pf+tax;
var net=gross-deduct;
document.writeln("<b>Employee Name:"+name+" </b>"+"<br>"+"<br>");
document.writeln("<b>Employee Number:"+num+" </b>"+"<br>"+"<br>");
document.writeln("<b>Basic salary:"+sal+" </b>"+"<br>"+"<br>");
document.writeln("<b>HRA:"+hra+" </b>"+"<br>"+"<br>");
document.writeln("<b>DA:"+da+" </b>"+"<br>"+"<br>");
document.writeln("<b>Gross Salary:"+gross+" </b>"+"<br>"+"<br>");
document.writeln("<b>PF:"+pf+" </b>"+"<br>"+"<br>");
document.writeln("<b>tax:"+tax+" </b>"+"<br>"+"<br>");
document.writeln("<b>Deduction:"+deduct+" </b>"+"<br>"+"<br>");
document.writeln("<b>Net Salary:"+net+" </b>"+"<br>"+"<br>");
}
</script>
</head>
<body bgcolor="Pink" text="blue">
<center>
<h1> Employee Detail Form</h1>
<form name="emp">
<table border="2">
<tr><td colspan="2" align="center"> Employee Detail:</td></tr><br>
<tr><td>Employee Name:</td><td><input type="text" id="txtname"></td></tr><br>
<tr><td>Employee Number:</td><td><input type="text" id="txtnum"></td></tr><br>
<tr><td>Basic Salary:</td><td><input type="text" id="txtsal"></td></tr><br>
<tr><td><input type="button" onclick="show()" value="Salary Report"></td>
<tr><td><input type="reset" value="reset"></td></tr>
</table>
</form>
</center>
</body>
</html>
﻿
OUTPUT:
﻿


﻿
8. WRITE A PROGRAM IN PHP TO CHANGE BACKGROUND COLOR BASED ON DAY OF THE WEEK USING IF ELSE IF STATEMENTS AND USING ARRAYS.
<html>
<head>
<title>Color Change by Day</title>
<?php
$daysOfWeek=array
(
'Sunday'=>'#FF5733',
'Monday'=>'#33FF57',
'Tuesday'=>'#3357FF',
'Wednesday'=>'#FFFF33',
'Thursday'=>'#FF33FF',
'Friday'=>'#33FFFF',
'Saturday'=>'#FF3333'
);
$currentDay=date('l');
$backgroundColor='#FFFFFF';
if(array_key_exists($currentDay,$daysOfWeek))
{
$backgroundColor=$daysOfWeek[$currentDay];
}
?>
<style>
body
{
background-color: <?php echo $backgroundColor; ?>;
}
</style>
</head>
<body>
<h1> Welcome! Today is <?php echo $currentDay; ?>.</h1>
</body>
</html>
OUTPUT:
﻿
﻿
9. WRITE A SIMPLE PROGRAM IN PHP FOR
(i)generating prime number
(ii)generate Fibonacci series.
<?php
$count=0;
$num=2;
echo "<h3> Prime numbers from 1 to 50:</h3>";
echo "\n";
while($count<15)
{
$div_count=0;
for($i=1;$i<=$num;$i++)
{
if(($num%$i)==0)
{
$div_count++;
}
}
if($div_count<3)
{
echo $num.",";
$count=$count+1;
}
$num=$num+1;
}
?>
<?php
$num=0;
$n1=0;
$n2=1;
echo "<h3>Fibonacci series for first 12 numbers:</h3>";
echo"\n";
echo $n1.' '.$n2.' ';
while($num<10)
{
$n3=$n2+$n1;
echo $n3.' ';
$n1=$n2;
$n2=$n3;
$num=$num+1;
}
?>
﻿
﻿
﻿
﻿
﻿
﻿
﻿
OUTPUT:

﻿
10. WRITE A PHP PROGRAM TO REMOVE DUPLICATES FROM A SORTED LIST.
<?php
function removeDuplicates($array)
{
$result = array_values(array_unique($array));
return $result;
}
$sortedList = [1,1,2,2,3,3,4,5,5];
$uniqueList = removeDuplicates($sortedList);
echo "Original List:";
Print_r($sortedList);
echo "<br>Unique List:";
Print_r($uniqueList);
?>
﻿
﻿
﻿
﻿
OUTPUT:

﻿
11. WRITE A PHP SCRIPT TO PRINT THE FOLLOWING PATTERN ON THE SCREEN.
* * * * *
﻿* * * *
﻿* * *
﻿* *
    *
<?php﻿
$rows=5;
for($i=$rows; $i>0; $i--)
{
for($j=$rows-$i; $j>0; $j--)
{
echo "&nbsp;";
}
for($k=0; $k<$i; $k++)
{
echo"*";
}
echo"<br>";
}
?>
OUTPUT:

﻿
12. WRITE A SIMPLE PROGRAM IN PHP FOR SEARCHING OF DATA BY DIFFERENT CRITERIA.
<?php
$data=[﻿
['id' =>1, 'name'=>'Vijay','age'=>22],
['id' =>2, 'name'=>'Anu','age'=>21],
['id' =>3, 'name'=>'Sai','age'=>22],
['id' =>4, 'name'=>'Ashri','age'=>19],
['id' =>5, 'name'=>'Vyshu','age'=>20]
];
function searchByCriteria($data, $criteria)
{
$results=[];
foreach($data as $entry)
{
$match=true;
foreach($criteria as $key=>$value)
{
if(!isset($entry [$key])||$entry[$key]!=$value)
{
$match=false;
break;
}
}
if($match)
{
$results[]=$entry;
}
}
return $results;
}
$criteria=['age'=>19];
$searchResults=searchByCriteria($data,$criteria);
echo "Search Results: <br>";
print_r($searchResults);
?>
OUTPUT:

﻿
﻿
13. WRITE A FUNCTION IN PHP TO GENERATE CAPTCHA CODE.
<?php
session_start();
function generateCaptchaCode($length=6)
{
$characters='0123456789abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ';
$charactersLength=strlen($characters);
$randomString=' ';
for($i=0; $i< $length; $i++)
{
$randomString.=$characters[rand(0, $charactersLength -1)];
}
return $randomString;
}
echo "Captcha Code is : ".generateCaptchaCode();
?>
OUTPUT:

﻿
14. WRITE A PROGRAM IN PHP TO VALIDATE INPUT.
<html>
<head>
<title>Input Validation</title>
</head>
<body>
<form method="Post">
Name:<input type="text" name="name"><br><br>
Email:<input type="text" name="email"><br><br>
<input type="submit" name="submit" value="submit">
</form>
</body>
</html>
<?php
if ($_SERVER["REQUEST_METHOD"]=="POST")
{
$name=$_POST['name'];
$email=$_POST['email'];
if(empty($name))
{
echo "Name is required.<br><br>";
}
else
{
echo "Name:".$name."<br><br>";
}
if(empty($email))
{
echo "Email is required.<br><br>";
}
elseif(!filter_var($email, FILTER_VALIDATE_EMAIL))
{
echo "Invalid email format.<br><br>";
}
else
{
echo "Email:".$email."<br><br>";
}
}
?>
OUTPUT:


﻿
15. WRITE A PROGRAM IN PHP FOR SETTING AND RETRIEVING A COOKIE.
<?php
$cookie_name="UserID";
$cookie_value="ABCD";
$expiration_time=time()+(24*3600);
setcookie($cookie_name,$cookie_value,$expiration_time,"/");
echo "cookie '$cookie_name' is set,<br><br><br>";
if(isset($_COOKIE[$cookie_name]))
{
echo "value of cookie $cookie_name' is:".$_COOKIE[$cookie_name];
}
else
{
echo "Cookie named '$cookie_name' is not set.";
}
?>
OUTPUT:

﻿
16. WRITE A PHP PROGRAM TO CREATE A SAMPLE WEBPAGE OF A COLLEGE.
<html>
<head>
<title> College Website </title>
<!_CSS styles can be added here_>
<style>
body
{
font_family:Arial,sans-serif;
margin:20px;
}
h1
{
color:#333;
}
p
{
color:#666;
}
</style>
</head>
<body>
<header>
<h1> Welcome to our College</h1>
</header>
<nav>
<ul>
<li><a href="Home.html">Home</a></li>
<li><a href="#">About Us</a></li>
<li><a href="#">Courses</a></li>
<li><a href="#">Contact</a></li>
</ul>
</nav>
<main>
<section>
<h2>AboutOurCollege</h2>
<p>This is a breif description of our college</p>
</section>
<h2>Available Courses</h2>
<?php
$courses=['Computer Science','Engineering','Business','Arts','Science'];echo"<ul>";
foreach($courses as $course)
{
echo"<li>$course</li>";
}
echo"</ul>";
?>
</section>
<section>
<h2>Contact Information</h2>
<p>Address:123 College:Avenue,City,Country</p>
<p>Email:info@college.com</p>
<p>Phone:080-25634869</p>
</section>
</main>
<footer>
<p>&copy;
<?php
echo date("Y");
?>
Our College,All rights reserved</p>
</footer>
</body>
</html>
OUTPUT:

﻿
17. WRITE A PROGRAM IN PHP FOR EXCEPTION HANDLING FOR 
(i) DIVIDE BY ZERO
(ii) CHECKING DATE FORMAT
<?php
function divide ($numerator, $denominator)
{
if($denominator==0) {
throw new Exception("cannot divide by zero");
}
return $numerator/$denominator;
}
function checkDateFormat($date,$format='Y-m-d') {
$dateTime=DateTime :: createFromFormat($format, $date);
if(!$dateTime||$dateTime->format($format)!=$date) {
throw new Exception("invalid date format.");
}
echo "The date" .  $date . "is valid.<br>";
return true;
}
try {
echo divide(10,2). "<br>";
echo divide(10,0). "<br>";
}catch(Exception $e) {
echo "Division error:" . $e->getMessage() . "<br>";
}
try {
checkDateFormat("2023-03-10");
checkDateFormat("10/03/2023");
}catch(Exception $e) {
echo "Date error:" . $e->getMessage() . "<br>";
}
?>
OUTPUT:

﻿
﻿
﻿
﻿
﻿
﻿
﻿
﻿
