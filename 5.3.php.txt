<?php
$i=1;
$Grade=['A' =>0,
        'B' =>0,
        'C' =>0,
        'D' =>0,
        'F' =>0,];
$grade_name=['A' =>[' '],
           'B' =>[' '],
            'C' =>[' '],
            'D' =>[' '],
            'F' =>[' '],];
 
 
while(true)
{
  echo"Student ".$i.": (name grade, enter for end of data) :";
  $input=trim(fgets(STDIN));
  if($input=="e")
  {
    break;
  }
  $tmp=explode(' ',$input);
  $name=$tmp[0];
  $input_grade=$tmp[1];
  $Grade[$input_grade]++;
  $grade_name[$input_grade][$i-1]=  $name;
  $i++;
}
$key =array_keys($Grade);
foreach($key as $K )
{
  echo $K." (".$Grade[$K].") :". implode(",",$grade_name[$K])."\n";
}
