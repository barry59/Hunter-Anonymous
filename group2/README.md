# Hunter Anonymous (Group 2)

[Click here to visit Website](https://blog-46407.web.app/#/)

[Click here to view Presentation](https://docs.google.com/presentation/d/1PU2PNOFfkAZ-gafUKT_uRxyB3tuTdlG8Aj2ME25DHBo/edit?usp=sharing)


## Website Description

Hunter Anonymous is an anonymous online messaging board where students can post about their feeling about the Hunter community. If you want to complain about the rats, bedbugs, the food here, or whatever your heart desires. Go ahead no one will know you said it. Anyone can have access to Hunter Anonymous as there is no authentication or sign up. When on the website you can type your message in the text field and press on the submit button to have your message posted on the board. All posts on the website can be upvoted or downvoted as a way to agree or disagree on a person's message. 


## FlutterFire (Flutter + Firebase)

By using FlutterFire it connected our Flutter application to Firebase. The message entered by a user in the text field are stored in the Firebase database, then the data is queried and put into a card to be displayed in a list format.  This works almost the same way for the total votes on a post where they’re stored in the database and retrieved to be displayed on the website. 


## Front-end Implementation 

- Our single page application consists of a build widget which returns a scaffold
- The primary elements of the scaffold are an Appbar, Card and a ListView
- Appbar, this is where we have our app title and social media links:
- Card, this is where we display are message to all users:

**Our ListView consists of Card and StreamBuilder**
- We use a textfield and elevated button inside our Card to take the user input and write our post to the database:

**Finally our most important widget is the StreamBuilder**
- The StreamBuilder allows us to turn collection references, queries, or data structures into a list format.
- The Streambuilder can be modified to make a robust list-view of our data, and using physics: _NeverScrollableScrollPhysics()_ we can create a scrolling list view


## Upvote/Downvote Implementation

- The Upvote counter, Upvote/ DownVote button, text and post date of each post live in the ListView.builder() method of the Streambuilder:          This method takes a snapshot (is json-like response from Firebase) which allows us to access the document fields values of a given document from a collection
- I.E Text, Date, #of votes
- We can use the snapshot to access the number of votes
- Depending on the users action (upvoting/ Downvoting), we can either increment or decrement the votes in the buttons onPressed() method
- Then we finally take the new altered vote count and write it to the database
- We can add some additional logic using boolean variables to make the buttons colors visually react to the upvotes/downvotes


## Libraries/Packages

- Cupertino icons: provides a set of icon assets (up and down arrows) 
- Flutter icon: provides customizable icons for Flutter
- Firebase core: provides use of the Firebase Core API to connect to Firebase apps
- Cloud firestore: gives a cloud-hosted, noSQL database with live synchronization and offline support 
- Google fonts: used to get a variety of web fonts (we used Neuton)
- Intl: used to format and parse DateTime/TimeStamp types to String
- Url launcher: used to launch a URL (our Social Media accounts)




