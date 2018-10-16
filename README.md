# Project3
Join a Botnet

The plan:
1. Implement server and any necessary C&C Client support

2. Provide at least 3 routing snapshots of the network, at least 2 hours apart. The snapshot should contain at least 3 servers that are more than 1-hop from your server. You may, and probably should, provide more than 3 snapshots, but do not provide more than 1 per minute connected in the botnet.

3. Have been successfully connected to by an Instructor’s server.


To compile: g++ server.cpp -o server -lpthread



--------

You do not have to run your server on skel.ru.is, as long as it can connect to at least one server that is running on skel.ru.is. If you are having problems connecting to skel, contact an Instructor in the first week.

Your server should listen on two ports for other servers to connect to it, and continue to listen to a separate port for your clients to connect.

The first port on the command line is for TCP connections to the server from other servers. The second port is a UDP port, purely for information requests. Both of the server ports should be specified on the command line (to make it easy for the servers running on skel.ru.is to be found.) For example:

./tsamvgroup1 8888 8889

where 8888 is the TCP port for server connections, and port 8889 is a UDP port. Connections to 8889 should receive a single message in reply, listing the servers known to this server (the contents of the LISTSERVERS command below.) This is to allow servers to find servers that aren’t full, from servers which are.

The server should support at least the following commands with other servers, in addition to the commands in Project 2:
Each registered group in Canvas will receive their own list of 5 unique hashes. Your server should provide access to your hashes, but not to any other group’s.





Criteria	Ratings	Pts
This criterion is linked to a learning outcome Clear instructions on compiling and OS, as per Assignment p1.
You must provide clear instructions in a README file on how to compile and run your program, and what OS it was compiled on. If your program does not compile, please provide a detailed explanation of why you think that is, and why you decided not to use a source code management system with frequent commits for your project.
1.0 Pts
Full marks
0.0 Pts
No marks
1.0 pts
This criterion is linked to a learning outcome Code quality
Programs are well structured, modular, well commented and have sensible variable names.
2.0 Pts
Full marks
0.0 Pts
No marks
2.0 pts
This criterion is linked to a learning outcome Token Characters and Bitstuffing
All communication between servers uses start/end characters as per RoE 7.
1.0 Pts
Full marks
0.0 Pts
No marks
1.0 pts
This criterion is linked to a learning outcome API Implemented correctly
All server commands implemented exactly as described in assignment. Points will be deducted for deviations from the "standard".
2.0 Pts
Full marks
0.0 Pts
No marks
2.0 pts
This criterion is linked to a learning outcome Hash message deconstructed
Partial credit may be given for a list of hashes from other servers.
1.0 Pts
Full marks
0.0 Pts
No marks
1.0 pts
This criterion is linked to a learning outcome Provide Routing Snapshots and Connectivity
Provide at least 3 routing snapshots as described in Assignment, and have connected to an Instructor's server
3.0 Pts
Full marks
0.0 Pts
No marks
3.0 pts
