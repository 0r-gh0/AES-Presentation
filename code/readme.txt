AESFINAL: Contains our Rijndael AES Implementation in C (with various modes of operations)
	1) Header Compilation: gcc -c utils.c
						   gcc -c moops.c
	This should generate "utils.o" and "moops.o"
	
	2) Compilation with static linking: gcc -o AES AES.c utils.o moops.o -lcrypto
																		 (for openssl)
	3) Execution: Mentioned in the "print_usage" function.
	./AES e 1 test.pdf out.pdf YELLOW_SUBMARINE
	 <operation> <mode_of_operation> <inputfile> <outputfile> <key>

