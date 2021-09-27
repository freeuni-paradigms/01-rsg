## დავალების ატვირთვა
პირველ რიგში ცადეთ ცვლილებები დააკომიტოთ Github-ზე თქვენი კლასრუმის რეპოზიტორიაში.  
მაგრამ რადგან ჯერ git-ის გამოყენებაში არ ხართ გაწაფული, შეგიძლიათ პირველი დავალება ატვირთოთ Google კლასრუმზე.  
ნამუშევრის დასაარქივებლად გამოიყენეთ ```sh make archive``` ბრძანება და მიღებული hw-01.tar.gz ფაილი ატვირთეთ Google კლასრუმზე.

## setup
0. install valgrind
### Ubuntu
```sh
sudo apt-get install valgrind
```

### Arch
```sh
yay -S valgrind
```

1. build: `make`

2. run: `./rsg data/bionic.g`

3. test
**გაითვალისწინეთ, რომ ტესტერებისთვის სასვენი ნიშნების წინ აუცილებელია იყოს `space`**
```sh
./rsgChecker32 ./rsg data/bionic.g
./rsgChecker64 ./rsg data/bionic.g
```

4. test all
```sh
for i in $(/bin/ls data); do
	echo $i
	./rsgChecker64 ./rsg data/$i
done
```

one line
```sh
for i in $(/bin/ls data); do echo $i; ./rsgChecker64 ./rsg data/$i; done
```
