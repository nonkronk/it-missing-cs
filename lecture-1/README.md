# Written solution

1. Make sure you're running an appropriate shell  
`$ echo $SHELL`

2. Create a new directory called `missing` under `tmp`  
`$ mkdir -p tmp/missing`

3. Look up the `touch` program  
`$ man touch`

4. Use touch to create a new file called `semester` in `missing`.  
`$ touch tmp/missing/semester`

5. Write the following into that file, one line at a time:  
`#!/bin/sh`  
`curl --head --silent https://missing.csail.mit.edu`  
\
`$ echo "#!/bin/sh" > tmp/missing/semester`  
`$ echo "curl --head --silent https://missing.csail.mit.edu" >> tmp/missing/semester`

6. Try to execute the file, i.e. type the path to the script  
`$ cd tmp/missing`  
`$ ./semester`

7. Run the command by explicitly starting the sh interpreter  
`$ sh semester`

8. Look up the chmod program  
`$ man chmod`

9. Use chmod to make it possible to run the command ./semester rather than having to type sh semester  
`$ chmod +x semester`

10. Use | and > to write the “last modified” date output by semester into a file called last-modified.txt  
`$ ./semester | grep last-modified > ../../last-modified.txt`

11. Write a command that reads out your laptop battery’s power level or your desktop machine’s CPU temperature from `/sys`  
`$ echo /sys/class/power_supply/BAT0/capacity`  
`$ echo /sys/class/thermal/thermal_zone0/temp`

