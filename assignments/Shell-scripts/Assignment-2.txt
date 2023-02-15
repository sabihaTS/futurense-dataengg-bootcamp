#!/bin/bash
echo "enter your city name:"
read city1
echo "enter your city name:"
read city2
echo "enter your city name:"
read city3
echo "enter your city name:"
read city4
echo $city1 >> cities.txt
echo $city2 >> cities.txt
echo $city3 >> cities.txt
echo $city4 >> cities.txt

cat cities.txt | grep new > new_cities.txt
cat cities.txt | grep -i new|sed 's/New/Old/g' > old_cities.txt
cat old_cities.txt

sabi@MILE-BL-4500-LAP:~$ vi cities.sh
sabi@MILE-BL-4500-LAP:~$ "cities.sh" 17L,433B written
sabi@MILE-BL-4500-LAP:~$ chmod +x cities.sh
sabi@MILE-BL-4500-LAP:~$ ./cities.sh
enter your city name:
New Delhi
enter your city name:
New York
enter your city name:
New Delhi New Jersey
enter your city name:
New Delhi New Jersey
Old Delhi
Old York
Old Jersey
Old Delhi Old Jersey