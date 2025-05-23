**Larry DeMar:**

When I arrived at Williams in 1980 Williams was in need of a new updated “Background” program. They didn’t think in terms of “Operating System” at the time, but rather a fixed resident “Background” program that was produced in mass quantity in masked ROMs - which at the time was the only way to affordably put 4K (or 6K) bytes of code into a machine. The game program was called the “Foreground” and was burned into two or three 512 x 8 Bipolar PROM chips. EPROMs were wayyyyyyy too expensive in the early days of electronic pinball.

Ron Crouse wrote the first Background program (I’m sure Duncan can tell us what color ROM labels this used) used in the first Solid State production game Hot Tip. I’m pretty sure that Ron’s program was updated one or more times before Randy Pfeiffer came on the scene.  

**Duncan Brown:**

This first standard Background had white labels… but I’m pretty sure it was not standardized at first, so there are a couple of unique backgrounds floating out there too, also with white labels.

The next Background, used on most System 3 games, had yellow labels.  There was a version of Flash made to run with the green label background, and I believe they even shipped a handful, but that was by and large the last yellow label game.

Green label came next, and it was by and large a System 6 board ROM set. With System 7 boards came the blue label background and 7 digit displays.

Stern’s PIGS stands for "Pinball Interpreted Game System" - a SWI (software interrupt) in the code would run the next bytes through the PIGS interpreter. Written by Alan McNeil

**Larry DeMar:**

Randy was a talented computer wizard who programmed Williams breakout Flash Pinball before going to Taito where he developed Qix among other games. My memory of the history (which predated my arrival by a year or two) was that Randy updated the Background program to a new version providing new facilities for Flash. He probably developed the amazing sound package for Flash too.

Eugene did the foreground programming of Firepower which I believed used the same Background chips as Flash. He also created the legendary sound package for Firepower. To make Multi-Ball work as well as the spectacular presentation leading up to Multiball required pulling every trick in the book that he could muster up to make it work without altering the main masked ROM program, an exercise that would serve him well when he needed to figure out how to create a scrolling game on a bitmap video system with hardware that could classically only do a fraction of the job.

To put all of the special effects into Firepower it was the first game to use an EPROM, a 2K x 8 2716 (along with three 512 x 8 Bipolar PROMs).  If my memory serves me correctly, Eugene had to code the game to work with the 3 PROMs if the EPROM wasn’t present with the EPROM containing the enhanced Multiball presentation and a monster attract mode that this large real-estate addition made possible.

I came on the scene in 1980 when Gorgar was on the production line and Firepower was getting ready for production. Steve and Eugene showed me Firepower for the first time when they were interviewing me for a possible software position and I was blown away by the steps made in this game to advance the art, and proud of my performance to put it through its paces and starting Multiball on my first game to Steve and Eugene’s amazement.

Steve was losing Eugene to the Defender project and quickly put me in position to be the programmer on his next game which would be Black Knight. My first project was to program Scorpion using the existing Background which helped me intricately understand its capabilities and shortcomings. We talked about my programming the New Background and I remember the concern of management to trust this to someone so inexperienced because the economics of the ROMs only worked with a large order placed with a long lead time (EPROMs were now affordable for the game program but still cost several times the cost of the larger masked ROM chips).

I created PERC from the ground up, analyzing each facility of the previous background to learn what to incorporate and what to improve. The biggest additions were adding multi-threading and process control, greatly enhanced modes of processing switch activity and separating the state elements for score and lamp state from the hardware to allow use of these elements for purposes other than state 

For example, for Firepower, the Background program which was in ROM that could not be modified, refreshed the displays from the data that comprised the players’ score. To do the multi ball countdown in the displays, Eugene moved the scores to a scratch area and put the countdown numbers in for the player’s scores so they would show in the displays. He had to ensure that no score processing took place during this time which would have garbled the numbers and possibly awarded erroneous replays were this to have happened.

I also added an interpreter (called PINBOL - “Pinbol Is Not a Bogus Operating Language”) to allow sequenced operation of common functions using a much smaller ROM footprint than would be used for the assembly code to create the same result.

As I was far along in the process of writing the code for PERC, management was still concerned about the success of this endeavor and asked Paul to see if he could write the game code for Blackout (the game he just finished programming using Randy’s background) using PERC.  My memory is that he cranked it out in a day or two to everyone’s amazement.

PERC was put into masked ROM which were first used on Black Knight with new System 7 hardware which natively supported 7-digit scoring with commas (although Alien Poker presented 7 digit scoring first with some brilliant work-arounds by Paul with the hard coded background). This ROMed program was used for several years going forward.  Somewhere during the 1981-1984 time period when I was working solely on Video Games at Vid Kidz, Bill Pfutzenreuter took over development of PERC and modified it for other hardware and capabilities, not only for Pinball but for other game formats like the High Noon wall game, the 3 in 1 Pachinko-style game and the Still Crazy vertical flipper game. Was System 8 made for one of these games?  System 10?  

* *Editor’s Note: System 8 was a single-board design that used a reduced set of System 7 features and was used on the “Still Crazy” prototype novelty game, (https://www.ipdb.org/machine.cgi?id=3730,) and two pitch-and-bat style games, “Pennant Fever” and the unreleased “Gridiron” conversion kit. The “Direct Hit” prototype novelty (http://www.backglass.org/williams/direct_hit_cab.jpg) and the bartop pachinko-style novelty game “4-in-1” by Barry Oursler used System 10, see https://www.ipdb.org/machine.cgi?id=6011* *

In this era the system was modified regularly and produced in EPROMs along with the game code.

When I started working on Pinball Machines again in 1984 for Space Shuttle I adapted PERC for system 9 hardware which I believe was only used for 3 pinball machines—Space Shuttle, Sorcerer and Comet.

My next project was High Speed and System 11 hardware was in development by Mark Loffredo. Like my time working on Pinball designs with Ed Boon in the late 80’s I knew that Mark was a rock star but had no idea of the depth of his talent and the amazing things he would accomplish down the road. I adapted PERC for alphanumeric displays (including individual segment control) and multiple languages. 

The alpha-numeric displays were a significant cost increase and most everyone has heard of the heated “discussion” that Steve and I had with Ken when he came in to tell us that the alphanumeric displays that we were using in the High Speed prototype were too expensive and had to be taken out of the game. And yes, I did push the top of the prototype backbox toward Ken in anger, but I had no idea that my push would be hard enough to topple the entire machine in his direction which he luckily caught to push it back on its legs.  

After a period of sulking on my side and reflecting on both sides, a compromise was reached to use Alphanumerics on top and 7-segments on the bottom which was a brilliant way to solve this situation and barely had any impact on the results or perception (I would guess that most players would tell you that the displays were all alphanumeric).

I was away from Williams for a couple of years after High Speed and Bill took over PERC development for games such as Pin*Bot, Millionaire, Fire, F-14 Tomcat etc.

I came back into Williams in 1988 for the Banzai Run project and made the decision to update the High Speed PERC which I was using for the Wreck n’ Ball prototype rather than using the version that Bill had evolved. From this point until WPC/APPLE started with Fun House there were 2 versions of PERC being used with different programmers developing games on their preferred version.

After Banzai Run was complete I started the development of APPLE for the WPC hardware which was under development. We began with a plan to use a 68000 processor and to program games in C. Pinball was in a bit of a downturn and we collectively made the call to contain cost and stay with the cheaper processor and 8-bit architecture. No pinball machines were harmed in the making of this decision. Our programs had now grown to the size where it was clear that they couldn’t remained confined to the 64K address space afforded by 16 address lines of an 8 bit microprocessor. We settled on an architecture using a 6809 running at 2 MHz using bank-switched blocks of ROM space. With PTSD of the complications of working with a bank switching architecture on Defender (which we got rid of on Stargate and subsequent games through a brilliant idea from Eugene) I went in search of a C compiler for 6809 that would support relatively transparent bank-switching.  

My friend Jim Challenger ran a company called Software Development Systems that had a C compiler in their Uniware line that could help support mostly transparent bank switching through an “overlay” function which could resolve a variable to a byte value at link time (the assembler can’t tell which bank an external symbol resides in but the linker can lookup the overlay associated with the symbol). This compiler had different targets including the 68000 but they did not have a 6809 version.  When we discussed this, Jim pointed out that their 6809 assembler used the same linker as their 68000 version which meant that if they would make the small change to the 6809 assembler to add the overlay feature then I could develop an assembly language system that provided near transparent management of the bank switching.  

Jim explained that their system programmer, Anthony was too swamped to make this small change for us. I asked Jim if offering Anthony a pinball machine could persuade him to find some time. He said "if you make it a High Speed, then hell, I’ll make the change.” I obtained a used High Speed from an operator we knew (Williams had no inventory of a 4 year old game) and after we set up the game in Jim’s basement, he had Anthony make the changes to the 6809 assembler.

Using the overlay feature of the Uniware tools I incorporated a bank switching scheme with a restriction that required all data and tables to reside within the same code module that contains all references (a good object oriented style practice anyway). The new software allowed any function to transparently call any other function regardless of whether or not the 2 functions could be mapped into memory at the same time. I added a post-linker tool that took out the system call for inter-module references between co-resident code not known to be co-resident at compile time.

The other big focus of APPLE was on sanity and error checking. There were checks everywhere and many fatal and non-fatal errors that would trap for the programmer in the debugging environment and leave logs for the programmer to check in the operating environment. The PINBOL interpreter (which saves program space at the cost of real time) was traded out for a powerful set of macros that took up much more space but ran much faster.  A great choice given that Dot Matrix was around the bend.

With the addition of the dot matrix display for Terminator II, Slugfest and Gilligan’s Island (all in development after Steve and Mark Penacho prototyped the first version for Terminator II), Mark and Bill made the modifications to APPLE to support the display of images and animations on this new hardware.

My memory is sketchy on this next part, but before Pinball 2000, I believe that Ted began work on what was going to be the next pinball system which he called HIPPO (Highly Interactive Pinball Processing Organizer (or maybe Operations?)  I think this was set aside when Ted took on the new OS project for the gaming group.  I had always wished that I had come up with the HIPPO acronym for APPLE which was a good acronym but caused confusion with a small company in Cupertino.

Tom Uban was the system architect for Pinball 2000 and created a system called XINA.  XINA was based on an open source operating system called XINU (Xinu is not Unix).  The acronym fo XINA stood for “Xina Is Not APPLE”  (for some reason, Engineers seem to love recursive acronyms).  I remember Xina the Warrior Princess used on tee shirts that were made up during the development of that project which had several engineers on Tom’s team (I’m thinking Graham and Louis, but probably others too).

* *(Editor’s Note: here’s the shirt: https://imgur.com/a/z54CGZG)*
  
**Tom Uban:**

I saw Pin2K as an opportunity to make the programming of ever more complex pinball games both easier and manageable. Giving the programmer an environment where they could use a modern language (C/C++) versus assembly allowed for them to more easily add to their tool sets and concentrate on the game.

Because Pin2K used XINU, a lightweight preemptive O/S which included features such as networking, there was also the possibility of new pinball features (tournaments, etc). This would all run on the current low cost all-in-one PC motherboard (MediaGX for the first round).

A new Power Driver Board, connected over a parallel port would provide all of the usual switch, lamp, and coil features plus some new diagnostic capabilities.

A new PCI based DCS2/Masked ROM/Flash card would provide stereo sound as well as production and/or development (code, image, sound) storage.

Because of the networking capabilities of the new system, game code flash could be loaded relatively quickly during game development via a TFTP boot loader. The suite of GCC tools used to develop the system and games included GDB, which allowed for symbolic inspection of variables, code, memory breakpointing, single stepping, disassembly, etc.

The XINU shell was also extensible, allowing for the easy addition of any kind of diagnostic queries that the programmer desired.

On top of XINU, I built the new object oriented pinball game programming environment, XINA (XINA Is Not APPLE). The whole acronym thing was kind of silly. Oddly, XINA was pretty much a "port" of APPLE's API to C++. Because all of the programmers knew APPLE and because APPLE was so well thought through (with it's game modes, hooks, multi-ball handling system and everything) it made sense (to me anyway) that moving it to C++ would be the obvious next level.

Of course XINA had numerous new features as well. A complete system for managing system / game parameters based on concepts derived from Apple Corp's operating systems. Louis did the majority of this work, creating the diagnostic, adjustment, settings GUI along the way.

In order to support the new GUIs and game graphics et al, Graham developed an entire system which utilized the minimal hardware acceleration, did image compression and generally added video game capability to pinball, which had been previously limited to 32x128x4 shades of orange (including black).

While I did perform the initial work to take control from the PCI POST code, initialize the MediaGX and XINU O/S, etc, Duncan productized this code and figured out some of the more esoteric MediaGX hardware for Graham and others.

The updates were installed through the ISA POST code when the ISA update board was plugged in, it would take over and FLASH the update, doing a simple progress indicator graphic on the display during the process.

All in all, I would say that the nearly 7 years I spent at Williams was one of the most fun times in all of my career. The wide range of smart, create and interesting people with whom I had the pleasure to work, never ceased to amaze me and that the last thing we did was to develop Pin2k in 18 months, including the first game out the door was simply a fantastic experience.

**Graham West:**

To add to Tom’s comments here regarding graphics for Pin2K: the original image compression algorithms came from Mark Guidarelli who developed them for MK Trilogy on N64 I believe. I don’t remember if I reimplemented the encoder, but I did rewrite the decoder to coax better cache warming given the slowness of reading flash over the PCI bus. The video codec was inspired by DirectX Texture Compression.

Duncan was the one who explained the hardware acceleration in the MediaGX to me, so I could make rendering faster. I couldn’t have figured it out without his help. In fact I learned a huge amount from everyone who worked on Pin2000. It’s a time I still treasure.

**Larry DeMar:**

With regard to the debuggers, the first native debugger we created was DCON, created by the Vid Kids to first use on the development of Robotron 2084. I designed the digital circuit for the DCON PC board and Chuck touched it up (adding some buffers as I remember) and made PC boards for us. I’ve added Chuck to this thread for his comments/corrections. Eugene wrote the DCON program using a similar syntax and command set as the Motorola Exorciser debugger.  In addition to allowing breakpoints and memory operations it had a hardware trap that would seize control if a watched address was accessed and we added the condition of read/write/either to give finer control to find who was corrupting a location. The primary interface it the board was the buss ribbon that connected the CPU and ROM boards, however the system needed a series of small modifications to the CPU board to work (including a watchdog disable) and mods to the ROM board to all “PIGS” to used as RAM in the program ROM space.


“PIGS” were two 2K x 8 RAM chips placed piggyback with an inverter on it’s back (probably a 7400) to decode select the chips based on the high address line for the 4K ROM socket.


* *Editor’s Note: The PIGS continued with later systems, eventually ending up with 8 megabits of SRAM in a small daughter board that fit to the WPC or WPC-95 ROM socket. An extra pad on the CPU’s circuit board carried the write signal from the custom ASIC to the PIG* *


In some order, there was a RAID board created for the short-lived 68000 color vector system that Eugene and I started working with before Blaster and BLACK FLAG was created for Pinball with software by Pfutz.


BLACK FLAG eventually morphed into ORKIN and many more advanced commands were added by Pfutz for PERC and later by Pfutz and me for APPLE to make it more and more aware of the system that it was working with.


I think that for TMS 34010 video system, crude off the shelf debuggers were used until the non-insecticide named Toddview (named for Todd Allen) created an amazing facility for Source Level Debugging.


After the 34010 era I don’t know how the debugging evolved in Video, and I remember using something that was effective during my short stint of poking at the XINA switch matrix scanning and hope that the P2K team can add some color there.


**Graham West:**


I can talk a little about the Pin2K debugging setup. Tom wrote a stub that let you use gdb on the host since we were using cygwin for the compiler etc. I don’t know if it had Emacs integration, but this is Tom we’re talking about so probably. There was also a serial console (Tom did the low level work there too) and I added a way for game code to define custom commands. We used that a lot, I remember when we were looking for one of the last crash bugs, that took a week to happen, we used commands to dump the memory allocated and free lists and that’s how we learned we had a tiny memory leak in a very specific place.


It’s weird to me that so many programmers these days in languages like PHP and Javascript rely on printf-style debugging and don’t understand the benefits of single stepping or inspecting variables, especially given how powerful modern machines are.

