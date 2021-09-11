# blkstuff
A .blk decryptor and mhy0 extractor for Genshin Impact that doesn't require hooking into the game. Tested working as of 2.0.

The code isn't very good, but it's meant as more of a reference than an actual tool. Any efforts to rewrite the project are highly appreciated.

~~Also, you'll need a modified AssetStudio to load these files. Since I didn't write it, I won't distribute it here. Sorry.~~

I finished my own AssetStudio fork that can load .blk files directly, which can be found [here](https://github.com/khang06/AssetStudio). If you're simply interested in datamining or something, you may want to download this instead.

# configure project
1. install cmake  
2. run configure_win.bat if you're under windows  
3. run configure_linux.sh if you're under linux  

# usage
```
blkstuff [[-s <path>] | [-d <file>]] [-o <path=./output>] [-t <thread_count=16>] [-l <file>] [-h]
 -s, --scan FOLDER         scan all the blk files in FOLDER and decrypt them
 -d, --decrypt BLK_FILE    decrypt BLK_FILE
 -o, --output FOLDER       write unlocked blks to FOLDER, default: ./output
 -t, --thread_count COUNT  specify the thread count to decrypt blk files, default: 16
 -l, --log_file FILE       set the log file to save the log. log will NOT be saved if this option is not specified
 -h, --help                print this message

notice:
 if you specify -s and -d in the same time the -d option will be ignore
```

for example:  
```
blkstuff -s ./blk_folder -o ./output_folder
blkstuff -s "Genshin Impact/blk_folder" -t 8 -l log/genshin_blk.log
blkstuff -d ./test.blk -o .
```

