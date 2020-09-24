<div align="center">

## TIPS: Optimizing your VB code\-15 ways to tighten your code


</div>

### Description

This article is just a paper i wrote, in jot-note form about diferent things to check for while programming in VB to make your program run as efficiently as possible, it is concentrated on making your program faster and is a must see for game developers! Enjoy... ALSO NOTE - This article does not cover usingf the compiler options to optimize code in detail, maybe in my next version of this article...
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[\(Tim Miron\) yar\-interactive software](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/tim-miron-yar-interactive-software.md)
**Level**          |Intermediate
**User Rating**    |4.3 (51 globes from 12 users)
**Compatibility**  |VB 4\.0 \(16\-bit\), VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0
**Category**       |[Coding Standards](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/coding-standards__1-43.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/tim-miron-yar-interactive-software-tips-optimizing-your-vb-code-15-ways-to-tighten-your-co__1-25924/archive/master.zip)





### Source Code

<center>
<font face="Arial" size=5><b>Notes about optimising code...</b></center>
<font face="Arial" size=3>
<p><b>IMPORTANT</b>: Alot of this stuff is common knowledge, and alot of you might start reading this and laugh because it seems like pretty simple stuff, but make sure you read the whole thing because i'm sure theres a few things in here you didn't know yet... The following has been discovered by day-to-day trial, or even personal experiments i have prepared to test processing speed in diferent conditions... Enjoy</p>
<p>
Boolean values process faster
than byte values
</p><p>
select case work faster than If statements
</p><p>
bytes, integers, and long variable types work faster
than other numeric data-types because they dont have
any decimal points...
</p><p>
For...Next loops work faster than Do...Loop loops
</p><p>
When changing multiple attributes of the same object
or type, using the With statement will speed up processing
</p><p>
When working with graphics processing, keeping graphics' width and height attributes
in the binary system (8,16,32,64,128,256 etc.) allows faster
processing on some systems
</p><p>
Avoid using the Sqr statement whenever possible, (used
often in games for trig and circular collision detection)
it is known to take great time processing...
</p><p>
Use the smallest data-type possible when declaring a variable -
it will use less ram, and generally process faster...
</p><p>
You can use the LoadResString function instead of string
literals in your code. Storing long strings of data in and accessing them from resource files improves load time because you can load them individually as needed from the resource file, rather than all at once when a form is loaded.
</p>
<p> using the Load statement to pre-load forms allows forms to be shown instantly when the form's Show event is called... Use the Unload statement to unload the form out of memory when your program is done with it...
</p>
<p> Constants are easier to program wth, but did ya know they process alot slower than raw numbers... instead of declaring a Const and using it through-out your program, try feeding your program raw data instead, according to my tests, raw numbers are referenced and processed 23% faster than equivilant constants...</p>
<p> Constants do process ever-slightly faster than equivilant variables, clocked at being 2.1% faster in processing and reference speed then equivilant variables...</p>
<p> Try to avoid using VB timer controls whenever possible and use LOOPs instead, they work faster, and can even be more accurate if you make a code timer... this rule applies more to games and whatnot then to any other type of program, and FYI - timers dont process any quicker than about 56MS, even when their interval is set below that value</p>
<p> Any images you use in your program will increase the size of your final executable file, to help keep this problem to a minimum, it is a good idea to save any images as JPGs or GIFs, when the images are compiled into the executable, the file size is greatly reduced.</p>
<p> Try to avoid using brackets in mathimatical equations where they are not needed, this boggs down processing time aswell...</p>
<p> More optimizations can be performed from VB's project properties Compile options screen (see VB help for more info).</p>

