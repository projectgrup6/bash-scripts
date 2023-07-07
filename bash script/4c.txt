#!/usr/bin/bash
echo "enter the input string"
read -s string
whitespace='                          '
j=1
if [[ $string =~ [A-Z] ]]
then
string=$(echo $string | tr [:upper:] [:lower:])
fi
echo "$string"
substring=$string
for((i=${#substring};i>0;i-=2))
do      
substring="${substring:1:i-2}"
echo "${whitespace:0:j}""$substring"
j=$j+1
done