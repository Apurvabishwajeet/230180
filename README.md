# 230180
LEVELS - PASSWORD

Level-0 : bandit0
[ls (gives the directory readme) ; cat readme (reads the file and gives the password)]

Level-1 : NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
[cat ./- (A dashed file is read through the format ./-)]

Level-2 : rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
[cat "spaces in this filename" (When there are spaces in the file name, it is written inside double inverted commas)]

Level-3 : aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
[cd inhere (change the current directory into inhere directory)
find (wrote names of all the files)
cat ./.hidden (reads the file)]

Level-4 : 2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
[cd inhere; file ./* () ; cat ./*file07 (gave the file data)]

Level-5 : lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR 
[cd inhere (current dir changed to inhere dir) ; find \! -executable -size 1033c (this specifies that the file is non-executable and is of size 1033c as c denotes bytes)]

Level-6 : P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU 
[find / -user bandit7 -group bandit6 -size 33c (we find the file on the server through the informations given using the find command) 
cat ( used to read the given file)]

Level-7 : z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
[grep -h "millionth" data.txt](here grep -h display the whole line that is matched with the pattern and the data next to the millionth word is the password for next level)

Level-8 : TESKZC0XvTetK0S9xNwm25STk5iWrBvP
[sort data.txt | uniq -u] (here we use uniq -u as it displays only the unique lines, this is done along with piping as uniq command works only on adjacent identical lines so we sorted the input and piped it with uniq command)

Level-9 : EN632PlfYiZbn3PhVK3XOGSlNInNE00t
[strings -w data.txt | grep ===] (to find the human readable strings,strings -w command is used and it is piped with grep to filter out the outputs that have the given pattern i.e several = symbols)

Level-10 : G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
[ base64 -d data.txt](base64 -d is used to decode the encoded data)

Level-11 : 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
[cat data.txt | tr 'a-zA-Z' 'n-za-mN-ZA-N'] (cat command reads the given file and it is piped with tr command to shift all the alphabets to its 13th position to get the password)

Level-12 : JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
[mktemp -d --->  /tmp/tmp.nzZRcAtQPK (A temporary dir is created)
cp data.txt /tmp/tmp.xzhhkHxx5G (copies the data in the dir /tmp/tmp.nzZRcAtQPK)
cd /tmp/tmp.xzhhkHxx5G (changes the current directory to /tmp/tmp.nzZRcAtQPK
mv data.txt apurva_data (file renamed)
xxd -r apurva_data > decompressed 
(converts hexdump back to binary and saved it into a new file named decompressed)
mv decompressed decompressed.gz (From here we check the data of the file and compare the left side digits to the right most side strings to identify whether gzid,bzip or tar will be used to decompress the current and the upcoming files and we repeat the process untill we get the decompressed file that gives password)
gzid -d decompressed.gz
mv decompressed decompressed.bz2
bzip2 -d decompressed.bz2
mv decompressed decompressed.gz
gzip -d decompressed.gz
tar -xf decompressed.tar
tar -xf data5.bin
xxd data6.bin
bzip2 -d data6.bin
xxd data8.bin
mv data8.bin data8.gz
gzip -d data8.gz
cat data8
gives the password]

Level-13 : wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
Level-14 : fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
Level-15 : jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
