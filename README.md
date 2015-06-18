# SALMOR

SALMOR is an expansion of and a graphical front-end for the ALMOR inflectional generation software by the LDC. Given a file with a list of lemmas and other linguistic features, SALMOR creates a new file of your choosing filled with generated inflections from each lemma.


------====== INPUT ======------

This generator, through the "Input file" button, takes as input a file with each line having a lex value (the lemma) from the SAMA database. Each line can also include the following properties from the SAMA database:

pos (Part of Speech)
prc[0-3] (Proclitics)
per (Person)
asp (Aspect)
vox (Voice)
mod (Mood)
gen (Gender)
num (Number)
stt (State)
cas (Case)
enc0 (Enclitics)

For information about these properties, please refer to the ALMOR manual.


------====== OUTPUT ======------

When clicking the "Output File" button, a window pops up, where you will choose the destination directory and name of your desired output file.

The output format is as follows, with each value tab-separated:
Lemma, Criteria Matches Count, Generated Inflection, Prefixes 1-6, Stem, Suffixes 1-6, Stem category

Press the "Generate" button to start the generation process.




------====== Additional Files Needed ======------

For the version not bundled with ALMOR or the SAMA database:
Place the ALMOR3IRQgen.pm file in the same directory as the generator executable.
Create a directory called "script" in the same directory as the generator executable. 
Place within it:

	ALMOR3gallSina.pl  <== This is the Generator script run by the program
			
			
The File structure in the end should be as follows:
Generator
|_____ ALMOR3IRQgenSina.pm (Generator Library)
|_____ almor-s31.db (Database)
|_____ Generator.exe (Executable)
|_____ script
        |_____ ALMOR3gallSina.pl (Almor Generation Script)
