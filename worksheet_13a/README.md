# DATE: 18/10/2026

**Tools learnt:**
- `qrencode` 
- `ffmpeg` 

**Commands learnt:**
- `qrencode`
	1. "`qrencode -o {filename} {string}`" : {self explanatory}
	2. "`qrencode -h`" : {for help}
- `ffmpeg`
	1. "`ffmpeg -i {input file name} {output file name}`" : {input file to be processed into desired output file}
	2. flags:
		1. "`-vframes`" : {to select a frame to be processed}
		2. "`-t`" : {designates time limit to output file (for video files, .gif files)}
		3. "`-vf`" : {"video filter"; to change characteristics of a video file like fps, scale etc.}

**What broke and fixes**:
- `qrencode`
	1. `qrencode o {filename} {string}` : said "no output filename mentioned"
		- *fix:* add hyphen before "o"; otherwise `qrencode` doesn't recognise the output filename in front of it.
- `ffmpeg`
	1. `ffmpeg -i Nature.mp4 abc.xyz` : 'said 'unable to choose an output format for "abc.xyz" '
		- *fix:* `.xyz` is **NOT** a recognised/valid file format; change it to something that is recognised like `.gif` .
	2. `ffmpeg -i Nature.mp4 -t 3 -vf "fpt=10 scale:-1" b.gif` : said 'no option name near "10" '
		- *fix:* the flag `fps` was misspelled; correct the spelling. 

**The first 5 steps for learning a new tool:**
1. Read documentation.
2. General command structure; go through it.
3. Try simple commands.
4. Try to predict the changes in the output, change small things within the command, and explain the changes.
5. Break the tool. Make simple mistakes and recognise the errors.

**One thing I'd like to try next time:**
`ffmpeg` is the one I found interesting. I'd want to check it audio/video capabilities to a more complex level.