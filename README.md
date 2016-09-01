# networking_applications
"Networking Applications" course projects from USC M.S. in intelligent robotics

**zip file contains all cpp files
- auctionserver.cpp:
	Sets up a synchronous I/O multiplexing server (per Beej's networking code) that can handle data from multiple clients.
	The main workhorse of this file is CreateMultiSynchIOServer_Phase1() and CreateMultiSynchIOServer_Phase2().
	These files contain not only the networking code, but also the logic to process and reply to message from clients.
	Seller and Client data are stored into structs for use in phases 1 and 2.
- bidder1.cpp and bidder2.cpp:
	Sets up a simple socket connection, and talks and receives over that socket for phases 1 and 2.
	Each talk and receive command is done in serial according the flow of operations in the project description.
	Phase 1 commands are sent in the format of "Login#<Type> <Name> <Password> <BankAcct>"
- seller1.cpp and seller1.cpp
	Sets up a simple socket connection, and talks and receives over that socket for phases 1 and 2.
	Each talk and receive command is done in serial according the flow of operations in the project description.
	Phase 1 commands are sent in the format of "Login#<Type> <Name> <Password> <BankAcct>"
	Phase 1 response messages for received item lists are in the format of "Accepted#<Phase 2 IP address> <Phase 2 port number>"
	Phase 2 commands set with with "ItemList#<Name> <Item \n;{repeats}>"
	Phase 2 response messages for received item lists are "Accepted#" - there are not argument for this reponse message in phase 2.
- MakeFile
	runs all the g++ compile commands for the .cpp files
- runProj
	execute the c++ executable files in the proper order
The last two files (MakeFile and runProj) are shell scripts that will compile and run the program for the user.
The scripts will shut themselves down.
