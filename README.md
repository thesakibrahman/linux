# User and give permission
sudo useradd sakib <br>
passwd sakib <br>
cat /etc/passwd { show the user ) <br>

sudo groupadd sakib_group <br>
grep sakib_group /etc/group { very the group } <br>
sudo usermod sakib_group sakib <br>

mkdir sakib <br>
chmod 777 sakib <br>
ls -l <br>

#  process shown
sudo ps aux <br>
sudo ps aux | head - 15 <br>
sudo ps -eo pid, ppid, cmd, %mem, %cpu --sort=-%cpu | head -10 <br>

#  date and time
sudo date --set="2023-05-31 01:25:06" <br>

#  even-odd
#!/bin/bash <br>
echo "Enter a Number:" <br>
read number <br>
if [ $((number % 2)) -eq 0 ]; <br>
then <br>
echo "The number $number is even" <br>
else <br>
echo "The number $number is odd" <br>
fi <br>

#  prime-number
#!/bin/bash <br>
echo "prime number between 0 and 100." <br>
for ((num = 2; num <=100; num++)); <br>
do <br>
is_prime=true <br>
for ((i = 2; i < num; i++)); <br>
do <br>
if ((num % i == 0)); <br>
then <br>
is_prime=false <br>
break <br>
fi <br>
done <br>
if [ "$is_prime" = true ]; <br>
then <br>
echo "$num" <br>
fi <br>
done <br>

#  Palindrome-number
#!/bin/bash <br>

echo "Enter a number:" <br>
read num <br>
reverse=$(echo $num | rev) <br>
if [ $num -eq $reverse ]; then <br>
  echo "The number $num is a palindrome." <br>
else <br>
  echo "The number $num is not a palindrome." <br>
fi <br>

#  Fibonacci series
#!/bin/bash <br>
echo "enter the number of term in the fibonacci series:" <br>
read num <br>
term1=0 <br>
term2=1 <br>
echo "Fibonacci series with $num terms:" <br>
for ((i = 1; i <= num; i++)); <br>
do <br>
echo -n "$term1" <br>
next_term=$((term1 + term2)) <br>
term1=$term2 <br>
term2=$next_term <br>
done <br>
echo <br>

#  Factorial-Number
#!/bin/bash <br>
echo "Enter a Number:" <br>
read num <br>
fact=1 <br>
for ((i = 1; i <= num; i++)); <br>
do <br>
fact=$((fact * i)) <br>
done <br>
echo "The factoril of $num is $fact." <br>


#  reverse number
#!/bin/bash <br>
echo "Enter a number: " <br>
read number <br>

reverse=0 <br>
temp=$number <br>

while [ $temp -gt 0 ]; do <br>
  remainder=$((temp % 10)) <br>
  reverse=$((reverse * 10 + remainder)) <br>
  temp=$((temp / 10)) <br>
done <br>

echo "The reverse of $number is: $reverse" <br>

#  add number range
#!/bin/bash <br>

echo "Enter the starting number: " <br>
read start <br>
echo "Enter the ending number: " <br>
read end <br>
sum=0 <br>
for ((i = start; i <= end; i++)); 
do <br>
  sum=$((sum + i)) <br>
done <br>
echo "The sum of numbers from $start to $end is: $sum" <br>
