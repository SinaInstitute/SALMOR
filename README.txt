# Almor Generator Program

------====== INPUT ======------

	This generator, through the "Input file" button, takes as input a file with each line written in the following manner:

	lex:_____ pos:_____

	After "lex:" write down the lemma from the database you wish to generate inflections of.
	After "pos:" write down the part of speech of the lemma's inflections (noun, verb, etc.)




------====== OUTPUT ======------

	When clicking the "Output File" button, a window pops up, where you will choose the destination
	directory and name of your desired output file.

	The output format is as follows, with each value tab-separated:
	Lemma, Criteria Matches Count, Generated Inflection, Prefixes 1-6, Stem, Suffixes 1-6, Stem category

	Press the "Generate" button to start the generation process.




------====== Additional Files Needed ======------

	For the version not bundled with ALMOR or the SAMA database:
		Place the ALMOR3IRQgen.pm file in the same directory as the generator executable.
		Create a directory called "script" in the same directory as the generator executable. Place within it:

			ALMOR3gallSina.pl  <== This is the Generator script run by the program
			
			
	The File structure in the end should be as follows:
	Generator
	|_____ ALMOR3IRQgenSina.pm (Generator Library)
	|_____ almor-s31.db (Database)
	|_____ Generator.exe (Executable)
	|_____ script
	        |_____ ALMOR3gallSina.pl (Almor Generation Script)
