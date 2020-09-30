<?php
echo "Input Number of data :";
$number = trim(fgets(STDIN));
for($i=1;$i<=$number;$i++)
{
  echo"\nData ".$i;
  echo"\nName Prefix (0: Mr., 1: Miss.) :";
$prefix = trim(fgets(STDIN));
echo"\n\tFirst Name :";
$f_name = trim(fgets(STDIN));
echo"\n\tLast Name :";
$l_name = trim(fgets(STDIN));
echo"\nGender (0: Male,1: Female,2: Transgender) :";
$gender = trim(fgets(STDIN));
echo"\n\t Number of Phone:";
$number_of_phone = trim(fgets(STDIN));
for($j=1;$j<=$number_of_phone;$j++)
{
echo"\n\tPhone Number ".$j." :";
$phone_number[$j] = trim(fgets(STDIN));
}
$data[]=[
'n' =>$prefix,
'f' =>$f_name,
'l' =>$l_name,
'g' =>$gender,
'p' =>$phone_number,
];
 
$phone_number = [];
}
$prefix=['Mr.','Miss.'];
$gender=['Male','Female','Transgender'];
 
foreach($data as $key)
{
echo"\n\n-------------------------------------------------------";
echo"\n".$prefix[$key['n']]. " ".$key['f']." ".$key['l'];
echo"\n Gender :".$gender[$key['g']];
echo"\n Phone Nmuber :".implode(',',$key['p'])." ";
}
