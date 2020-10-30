<?php
$i=1;
$ave=0;
$sum=0;
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
  fscanf(STDIN,"%s %s",$name,$grade);
  if($grade=='A')
  {
    $score=4;
  }
  if($grade=='B')
  {
    $score=3;
  }
  if($grade=='C')
  {
    $score=2;
  }
  if($grade=='D')
  {
    $score=1;
  }
  if($grade=='F')
  {
    $score=0;
  }
  if($name=="e"||$grade=="e")
  {
    break;
  }
  $sum+=$score;
  $grade_name[$grade][$name]= $name;
  $Grade[$grade]++;
  $i++;
}
$ave=$sum/($i-1);
$key =array_keys($Grade);
foreach($key as $K )
{
  echo $K." (".$Grade[$K].") :". implode(",",$grade_name[$K])."\n";
}
echo"Average Grade Point :".$ave;
