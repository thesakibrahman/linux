# User and give permission
sudo useradd sakib
passwd sakib
cat /etc/passwd { show the user )

sudo groupadd sakib_group
grep sakib_group /etc/group { very the group }
sudo usermod sakib_group sakib

mkdir sakib
chmod 777 sakib
ls -l

#  process shown
sudo ps aux
sudo ps aux | head - 15
sudo ps -eo pid, ppid, cmd, %mem, %cpu --sort=-%cpu | head -10

#  date and time
sudo date --set="2023-05-31 01:25:06"

#  even-odd
#!/bin/bash
echo "Enter a Number:"
read number
if [ $((number % 2)) -eq 0 ];
then
echo "The number $number is even"
else
echo "The number $number is odd"
fi

#  prime-number
#!/bin/bash
echo "prime number between 0 and 100."
for ((num = 2; num <=100; num++));
do
is_prime=true
for ((i = 2; i < num; i++));
do
if ((num % i == 0));
then
is_prime=false
break
fi
done
if [ "$is_prime" = true ];
then
echo "$num"
fi
done

#  Palindrome-number
#!/bin/bash

echo "Enter a number:"
read num
reverse=$(echo $num | rev)
if [ $num -eq $reverse ]; then
  echo "The number $num is a palindrome."
else
  echo "The number $num is not a palindrome."
fi

#  Fibonacci series
#!/bin/bash
echo "enter the number of term in the fibonacci series:"
read num
term1=0
term2=1
echo "Fibonacci series with $num terms:"
for ((i = 1; i <= num; i++));
do
echo -n "$term1"
next_term=$((term1 + term2))
term1=$term2
term2=$next_term
done
echo

#  Factorial-Number
#!/bin/bash
echo "Enter a Number:"
read num
fact=1
for ((i = 1; i <= num; i++));
do
fact=$((fact * i))
done
echo "The factoril of $num is $fact."


#  reverse number
#!/bin/bash
echo "Enter a number: "
read number

reverse=0
temp=$number

while [ $temp -gt 0 ]; do
  remainder=$((temp % 10))
  reverse=$((reverse * 10 + remainder))
  temp=$((temp / 10))
done

echo "The reverse of $number is: $reverse"

#  add number range
#!/bin/bash

echo "Enter the starting number: "
read start
echo "Enter the ending number: "
read end
sum=0
for ((i = start; i <= end; i++)); do
  sum=$((sum + i))
done
echo "The sum of numbers from $start to $end is: $sum"
