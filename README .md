# Text-In-Image Steganography

## About


## Files

Each folder, sequential and linear, includes:

bmp_steg_tool.c => our code
bmplib.c 		=> open source bmp i/o functions
bmplib.h 		=> open source bmp i/o functions header
example.bmp	=> the original photo
Makefile		=> A makefile that should compile the program on 				starship.
test.txt 		=> The constitution in plaintext for encrypting.

## Usage

		usage: bmp_steg_tool  [-e efile | -d dfile] [-m messageFile] [-o ouput_file]  [image_file]

- If the ***-e encrypt*** flag is on *bmp_steg_tool* takes the image from ***efile***
	- If no file is specified, *bmp_steg_tool* takes the image from the console

- If the ***-d decrypt*** flag is on, *bmp_steg_tool* takes the image from ***dfile***
	- If no file is specified, *bmp_steg_tool* takes the image from the console

- If the ***-m messageFile*** flag is on and *bmp_steg_tool* is encrypting, it reads the message to be encrypted from the given file
	- If no file is specified, *bmp_steg_tool* prompts the user for a message on the console

- If *bmp_steg_tool* is *decryptiing* and the ***-o ooutput_file*** fla is provided *bmp_steg_tool* places the decrypted text message message into ***output_file***

- If *bmp_steg_tool* is *encrypting* and the ***-o ooutput_file*** is provided *bmp_steg_tool* places the encrypted image in ***output_file***



## Compiling Instructions:

###Sequential version - navigate to the Sequential Folder

		Type "make" in the command line.

encrypting example:

		./bmpsteg -e -m test.txt -o output.bmp example.bmp

decrypting example:
	
		./bmpsteg -d output.bmp


### Parallel Version - navigate to the Sequential Folder

		Type "make" in the command line.

encrypting example:

		mpirun -np 8 bmpsteg -e -m test.txt -o output.bmp example.bmp

decrypting example:
	
		mpirun -np 8 bmpsteg -d example.bmp
#### Notes

- The number after the flag "-np" specifies the number of processors






