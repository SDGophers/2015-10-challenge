
Challange for Oct.


http://www.ietf.org/rfc/rfc1436.txt

We are going to implement a simplifed version of the Gopher Protocol. 

Default port 70.



	Client:			{Opens connection to rawBits.micro.umn.edu at port 70}

	Server:			{Accepts connection but says nothing}

	Client: <LF><LF>	{Sends an empty line: Meaning "list what you have"}

	Server:			{Sends a series of lines, each ending with CR LF}
		0About internet GopherFStuff:About usFrawBits.micro.umn.eduF70
		1Around University of MinnesotaFZ,5692,AUMFunderdog.micro.umn.eduF70
		1Microcomputer News & PricesFPrices/Fpserver.bookstore.umn.eduF70
		1Courses, Schedules, CalendarsFFevents.ais.umn.eduF9120
		1Student-Staff DirectoriesFFuinfo.ais.umn.eduF70
		1Departmental PublicationsFStuff:DP:FrawBits.micro.umn.eduF70
				{.....etc.....}
		.		{Period on a line by itself}
				{Server closes connection}



	0 Item is a file
	1 Item is a directory
	2 Item is a CSO phone-book server
	3 Error
	4 Item is a BinHexed Macintosh file.
	5 Item is DOS binary archive of some sort.
		Client must read until the TCP connection closes.  Beware.
	6 Item is a UNIX uuencoded file.
	7 Item is an Index-Search server.
	8 Item points to a text-based telnet session.
	9 Item is a binary file!
		Client must read until the TCP connection closes.  Beware.
	+ Item is a redundant server
	T Item points to a text-based tn3270 session.
	g Item is a GIF format graphics file.
	I Item is some kind of image file.  Client decides how to display.


#For This months challange we are going to implement a simpilifed Gopher Server

   This server will have to following behavior.

   The server will listen on port 1337. 
   For this server we will only support 
   0,1,9,I

# The application will be started as follows
   sdgopher directory_to_serve

   using telenet we will connect to the 


