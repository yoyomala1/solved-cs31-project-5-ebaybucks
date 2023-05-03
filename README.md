Download Link: https://assignmentchef.com/product/solved-cs31-project-5-ebaybucks
<br>
According to Wikipedia, eBay Inc. is an American multinational e-commerce corporation based in San Jose, California, that facilitates consumer-to-consumer and business-to-consumer sales through its website.  eBay was founded in 1995, and became a notable success story of the dot-com bubble.  Today, eBay is a multibillion-dollar business with operations in about 30 countries.   The company manages the eBay website, an online auction and shopping website in which people and businesses buy and sell a wide variety of goods and services worldwide.  The website is free to use for buyers, but sellers are charged fees for listing items after a limited number of free listings, and again when those items are sold.  In order to incentivize buyers to use their site, eBay introduced eBay Bucks, a rewards program that allows buyers to receive a percentage of an Auction price in the form of an eBay Bucks certificate which can be used at a later time toward the cost of another item.

<b><span class="">Your task</span></b>







<span class="">Your assignment is to produce a two classes that work together to simulate Auctions and an EBayBucks account.  In an effort to help you, the design of these two classes will be discussed here.  In addition, some sample code has been provided to assist you with this task.  Various UML diagrams are shown below to communicate the code you need to create.  Please follow the steps outlined below and don’t jump ahead until you have finished the earlier step.</span>

<span class="">First, you will create the class Auction.  This class represents an auction for a listed item on the EBay site.  Each Auction object has a description and a minimum price it can be sold for.  These two parameters are provided to the Auction constructor.  Once an Auction is opened, it may receive bids of any amount.  Once an Auction is opened, the currentBid data member is tracking the highest bid value received so far.  Each bid that increases the currentBid value gets counted by the data member totalNumberOfBids.  Once an Auction is closed, no more bids are accepted.  Once an Auction is closed, the Auction will be deemed “successful” if the last bid received is larger than the minimum price originally established when the Auction was created.  That highest bid value gets returned when .winningBid( ) is called.  The Auction class also provides trivial getter methods to retrieve the description and current number of bids received.   <u>If there are no bids at all or no bids large enough to win the auction, then return -1 as the value for .winningBid( ).</u>   Please review the class diagram shown here:</span>

<img decoding="async" alt="Auction Class Diagram" width="500" height="360" data-src="./201A-COMSCI31-1_ Project 5_files/AuctionClass.png" class="img-responsive atto_image_button_text-bottom lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" class="img-responsive atto_image_button_text-bottom" src="./201A-COMSCI31-1_ Project 5_files/AuctionClass.png" alt="Auction Class Diagram" width="500" height="360">

 </noscript>

<span class="">For this project, you will create both a .h and .cpp for this class.  Write some sample driver code in your main( ) and create assertions to verify that your accessor methods are all working properly.  Some sample code is shown below to further document how this class should work.</span>

<span class="">Next, create the EBayBucks class.  Each EBayBucks object has an earnedAward member which represents the reward earned so far.  In the beginning of time, this earnedAward value should be zero.  That award amount should be increased by 1% of all the successful Auction winningBid values from all the Auctions passed to the .addAuction( … ) operation.</span><span class="">  The current award amount can be retrieved by calling .earnings( ).  The operation .issueCertificate( ) also returns the earned amount and then resets the earnedAward back to zero for later use.  Please review the class diagram shown here:</span>

<img decoding="async" alt="EBayBucks Class Diagram" width="501" height="184" data-src="./201A-COMSCI31-1_ Project 5_files/EbayBucksClass.png" class="img-responsive atto_image_button_text-bottom lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" class="img-responsive atto_image_button_text-bottom" src="./201A-COMSCI31-1_ Project 5_files/EbayBucksClass.png" alt="EBayBucks Class Diagram" width="501" height="184">

 </noscript>

<span class="">For this project, you will create both a .h and .cpp for this class.  Write some sample driver code in your main( ) and create assertions to verify that your accessor methods are all working properly.  Some sample code is shown below to further document how this class should work.</span>

<span class="">Y</span><span class="">ou are free to create additional public and private methods and data members as you see fit.  However, the test cases will only be driving the public methods of the two classes diagrammed here.</span>

<span class="">The source files you turn in will be these classes and a main routine.  You can have the main routine do whatever you want, because we will rename it to something harmless, never call it, and append our own main routine to your file.  Our main routine will thoroughly test your functions.  You’ll probably want your main routine to do the same.  If you wish, you may write additional class operation in addition to those required here.  We will not directly call any such additional operations directly.</span>

<span class="">The program you turn in must build successfully, and during execution, no method may read anything from cin.  If you want to print things out for debugging purposes, write to cerr instead of cout.  When we test your program, we will cause everything written to cerr to be discarded instead — we will never see that output, so you may leave those debugging output statements in your program if you wish. </span>

<span class="">Please read the posted <a href="https://ccle.ucla.edu/mod/page/view.php?id=2992780">FAQ</a> for further assistance.</span>

<span class="">Additionally, I have created a testing tool called CodeBoard to help you check your code.  CodeBoard enables you to be sure you are naming things correctly by running a small number of tests against your code.  Passing CodeBoard tests is not sufficient testing so please do additional testing yourself.  To access CodeBoard for Project 5, please click the link you see in this week named CodeBoard for Project 5.  Inside the files named Auction.h, Auction.cpp, EBayBucks.h and EBayBucks.cpp, copy and paste the versions you have developed.  CodeBoard uses its own main( ) to run tests against your code so you won’t get any opportunity to provide a main( ) function.  Click Compile and Run.  However please be aware that no editing changes can be saved inside CodeBoard.  In this anonymous user configuration, CodeBoard is read-only and does not allow for saving changes.</span>

<h3><b><span class="">Programming Guidelines</span></b></h3>

<span class="">Your program must <em>not</em> use any function templates from the algorithms portion of the Standard C++ library or use STL &lt;list&gt; or &lt;vector&gt;. If you don’t know what the previous sentence is talking about, you have nothing to worry about. Additionally, your code must <i>not</i> use any global variables which are variables declared outside the scope of your individual functions.</span>

<span class="">Your program must build successfully under both Visual C++ and either clang++ or g++.</span>

<span class="">The correctness of your program must not depend on undefined program behavior. </span>

<span class="">What you will turn in for this assignment is a zip file containing the following 6 files and nothing more:</span>




<ol>

 <li>The text files named <b>Auction.h</b> and <b>Auction.cpp</b> that implement the Auction class diagrammed above, the text files named <b>EBayBucks.h </b>and <b>EBayBucks.cpp</b> that implement the EBayBucks class diagrammed above, and the text file named <b>main.cpp</b> which will hold your main program. Your source code should have helpful comments that explain any non-obvious code.</li>

 <li>A file named <b>report.doc</b> or <b>report.docx</b> (in Microsoft Word format), or <b>report.txt</b> (an ordinary text file) that contains in addition <b>your name</b> and <b>your UCLA Id Number</b>:–<span class=""> A brief description of notable obstacles you overcame</span><span class="">– </span><span class="">A list of the test data that could be used to thoroughly test your functions, along with the reason for each test. You must note which test cases your program does not handle correctly. (This could happen if you didn’t have time to write a complete solution, or if you ran out of time while still debugging a supposedly complete solution.) Notice that most of this portion of your report can be written just after you read the requirements in this specification, before you even start designing your program.</span></li>

</ol>




<span class="">How nice! Your report this time doesn’t have to contain any design documentation.</span>

<span class="">As with Project 3 and 4, a nice way to test your functions is to use the </span><code><span class="">assert</span></code><span class=""> facility from the standard library. As an example, here’s a very incomplete set of tests for Project 5.  Again, please build your solution incrementally.  So I wouldn’t run all these tests from the start because many of them will fail until you have all your code working.  But I hope this gives you some ideas….</span>

<pre>	#include &lt;iostream&gt;	#include &lt;string&gt;	#include &lt;cassert&gt;        #include "Auction.h"        #include "EBayBucks.h"	using namespace std;	int main()	{<span class="s3">           </span><span class="s2">// sample test code </span></pre>

Auction auction( “4th Generation iPod”, 50.00 ); EBayBucks bucks;




assert( auction.numberOfBids( ) == 0 ); assert( auction.wasSuccessful( ) == false ); assert( auction.getDescription( ) == “4th Generation iPod” ); assert( std::to_string( auction.winningBid( ) ) == “-1.000000” ); // bids don’t count if the auction isn’t open… assert( auction.bid( 100.00 ) == false ); assert( auction.bid( 200.00 ) == false ); assert( auction.bid( 300.00 ) == false ); assert( auction.numberOfBids( ) == 0 ); assert( auction.wasSuccessful( ) == false ); assert( std::to_string( auction.winningBid( ) ) == “-1.000000” );

auction.openAuction( );

// an auction is not successful if the bids are too low… assert( auction.bid( -50.00 ) == false ); // negative bids are ignored assert( auction.bid( 1.00 ) == true ); assert( auction.bid( 2.00 ) == true ); assert( auction.bid( 3.00 ) == true ); assert( auction.bid( 1.50 ) == false ); // bids lower than the currentBid value are ignored assert( auction.numberOfBids( ) == 3 ); assert( auction.wasSuccessful( ) == false ); assert( std::to_string( auction.winningBid( ) ) == “-1.000000” ); // an auction must be closed to be deemed successful assert( auction.bid( 100.00 ) == true ); assert( auction.numberOfBids( ) == 4 ); assert( auction.wasSuccessful( ) == false );

auction.closeAuction( ); assert( auction.wasSuccessful( ) == true ); assert( std::to_string( auction.winningBid( ) ) == “100.000000” );

// bids don’t count if the auction is closed… assert( auction.bid( 500.00 ) == false ); assert( auction.bid( 600.00 ) == false ); assert( auction.numberOfBids( ) == 4 );

assert( std::to_string( bucks.earnings( ) ) == “0.000000” ); assert( std::to_string( bucks.issueCertificate( ) ) == “0.000000” ); bucks.addAuction( auction ); assert( std::to_string( bucks.earnings( ) ) == “1.000000” ); assert( std::to_string( bucks.issueCertificate( ) ) == “1.000000” ); // once a certificate is issued, the earned award gets reset to zero assert( std::to_string( bucks.earnings( ) ) == “0.000000” ); Auction a( “unsuccessful”, 10000.00 ); a.openAuction( ); assert( a.bid( 100.00 ) == true ); a.closeAuction( ); assert( a.wasSuccessful( ) == false );

// unsuccessful auctions don’t raise the earned award bucks.addAuction( a ); assert( std::to_string( bucks.earnings( ) ) == “0.000000” );

cout &lt;&lt; “all tests passed!” &lt;&lt; endl;

<span class="s1"> return</span> <span class="s5">0</span><span class="s2">; </span> }

<span class="">By August 5th, there will be links on the class webpage that will enable you to turn in your zip file electronically. Turn in the file by the due time above. Give yourself enough time to be sure you can turn something in, because we will not accept excuses like “My network connection at home was down, and I didn’t have a way to copy my files and bring them to a SEASnet machine.” There’s a lot to be said for turning in a preliminary version of your program and report early (You can always overwrite it with a later submission). That way you have something submitted in case there’s a problem later.</span>







<h3><b><span class="">G31 Build Commands </span></b></h3>

<span class="">g31 -c Auction.cppg31 -c EBayBucks.cpp</span><span class="">g31 -c main.cpp</span><span class="">g31 -o runnable    main.o    Auction.o    EBayBucks.o</span><span class="">./runnable</span>