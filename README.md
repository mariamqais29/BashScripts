# BashScripts

First Assignment , We asked to write a solutions- bash scripts .
You can see here the solution for all tasks ,also you can find each one of them in file .

Q1- Write a bash script that collects two numbers from the user and then
prints a message if these two numbers are smaller or greater than 100.

My Solution-

    #! /usr/bin/bash
    read -p "Enter First Number ! " num1
    read -p "Enter Second Number ! " num2
    SUM=$(($num1+$num2))
    if [ $SUM -lt 100 ]
    then
            echo "Sum is Less than 100"
    elif [ $SUM -gt 100 ]
    then
            echo "Sum is Greater than 100"
    else
            echo "Sum Equals 100"
    fi

Q2- Write a bash script that reads a temperature in Fahrenheit and converts
it to Celcius.

My Solution- 

    #! /usr/bin/bash
    read -p "Enter temperature in Fahrenheit : " temp
    cel=$((($temp-32)*5/9))
    echo "The Temperatue in Celcius is : $cel"
    
    
Q3- Using the find, du, and sort commands, please write a script that finds
the largest 10 files in a directory.

My Solution -

    #! /usr/bin/bash
    read -p "Enter Path : " path
    echo "The Largest 10 files in  $path : "
    if [[ -z $path ]]
    then
            echo "Incorrect input "
    else
    find $path -type f | du -a | sort -rh | head -10
    fi

