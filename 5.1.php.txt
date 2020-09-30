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
echo"\nGender (0: Male,1: Female) :";
$gender = trim(fgets(STDIN));
echo"\n\tPhone Number :";
$phone_number = trim(fgets(STDIN));
$data[]=[
'n' =>$prefix,
'f' =>$f_name,
'l' =>$l_name,
'g' =>$gender,
'p' =>$phone_number,
];
}
$prefix=['Mr.','Miss.'];
$gender=['Male','Female'];
foreach($data as $key)
{
echo"\n\n-------------------------------------------------------";
echo"\n".$prefix[$key['n']]. " ".$key['f']." ".$key['l'];
echo"\n Gender :".$gender[$key['g']];
echo"\n Phone Nmuber :".$key['p']."\n";
}
