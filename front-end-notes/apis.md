#APIs: Application Programming Interfaces

##Definition 
A way to access web-based data or software tools.

An API is (usually) not a user interface. It provides software-to-software interaction, not user interactions.

##REST: Representational State Transfer
A RESTful API exposes a URL that can accept requests containing parameters (often contained in the url string).  The API will return a response based on the query parameters. The response format is often in JSON (JavaScript Object Notation).

##Example API usage with an AJAX call
This call should return information about a movie with the title "The Godfather", with a short version of the plot, in JSON format. In the URL string, you could replace "The+Godfather" with any movie title and it should return that movie's information.

    $.ajax({
      url: "http://www.omdbapi.com/?t=The+Godfather&y=&plot=short&r=json"
    })
    .done(function( data ) {
      console.log("Response Data: ", data);
    });

##Special Consideration
Due to the asynchronous nature of javascript, it is important to make sure the response data is received before trying to do something with it (race condition).  Promises can be used to prevent race conditions by pausing the execution until the data is returned. 

![Promise resolution diagram](https://mdn.mozillademos.org/files/8633/promises.png "Promise resolution diagram")

##Library Based APIs
Code librarys that provide access to complex functions using concise syntax. Examples: GoogleMaps, Firebase and Twilio.

##Useful APIs
- [Movies](http://www.omdbapi.com/)
- [Card Deck](http://deckofcardsapi.com/)
- [Zip Codes](http://www.zippopotam.us/)
- [Spotify](https://developer.spotify.com/web-api/)
- [Beer](http://www.brewerydb.com/developers)
- [GoogleMaps](https://developers.google.com/maps/?hl=en)
- [50 Useful APIs](http://www.computersciencezone.org/50-most-useful-apis-for-developers/)
