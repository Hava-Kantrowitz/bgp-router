Hava Kantrowitz and Derek Ng 
CS3700
Project 3 README

High Level Code Approach 

Our code is written in Python and broken up into methods. A detailed description of each method can be found in comments within the code, but here is a quick overview:
 - Methods we created 
    - print\_table(): prints a well formatted routing table to the console
    - get\_longest\_prefix(): selects the routes with the most specific prefixes
    - getIPPrefixBin(): gets the binary of the IP prefix 
    - uncombine(): performs disaggregation of the routing table
 - Methods from starter code 
    - lookup\_routes(): finds valid routes for a given address, performs bit manipulation 
    - get\_shortest\_as\_path(): selects routes with the shortest AS Path
    - get\_highest\_preference(): selects routes with highest local pref value 
    - get\_self\_origin(): selects routes that are self originating 
    - get\_origin\_routes: selects origin routes, with preference given in order of IGP > EGP > UNK
    - filter\_relationships(): Selects routes to enforce business rules 
    - get\_route(): selects best route for a given address
    - forward(): forwards data packets 
    - coalesce(): performs the coalescing of the routing table, including determining if coalescing is possible 
    - update(): handles update packets, adjusts routing table, and sends updates to necessary neighbors
    - revoke(): handles revoking packets, adjusts routing table, and sends revoke updates to necessary neighbors
    - dump(): handles dump table requests
    - handle\_packet(): dispatches packets to the proper method 
    - send\_error(): sends no-route error messages 
    - run(): runs the overall BGP router

Challenges Faced 

Neither of us have worked with BGP architecture before, so one of our biggest challenges was simply understanding the theoretical basis of the router structure. To do this, we went over the class slides and our notes multiple times, and talked through the process until both of us were comfortable with our understanding. Other challenges we faced included figuring out the ordering in get\_route(), and figuring out how to properly coalesce routing table entries. 
 
Testing Overview

We did not write specific tests for our BGP router. Instead, we relied primarily upon ensuring we could pass the test cases covered in the simulator. To check our work in the interim, we relied on print statements, both basic print statements and a well-formatted print of the routing table we created in the function print\_table(). 

Sources Consulted 

Primary source used was the project 3 description
Class notes, especially slides from the Network lecture 
A few StackOverflow posts to look up specific error messages and embarrassing momentary lapses in basic Python syntax. 
Netmask reference sheet created by Steve Friedl at unixwiz.net: http://www.unixwiz.net/techtips/netmask-ref.html`
