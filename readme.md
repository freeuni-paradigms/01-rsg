0. install valgrind
ubuntu: sudo apt-get install valgrind
arch: yay -S valgrind

1. build
run make command from terminal

2. run
./rsg data/bionic.g 	

3. test
./rsgChecker32 ./rsg data/bionic.g
./rsgChecker64 ./rsg data/bionic.g

4. test all
for i in $(/bin/ls data); do; ./rsgChecker64 ./rsg data/$i; done
