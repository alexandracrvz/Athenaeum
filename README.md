# Athenaeum
 # Project Overview
 # Beta 1

 ## Project Links

 - https://github.com/alexandracrvz/Athenaeum
 - [add your deployment link]()

 ## Project Description

 With this Film App called "Athenauem" users will be able to search for a film then be provided with the film's title, poster, genre, and synopsis by fetching the information from the OMDb API. 
Beta 2: The user can then add their favorite films to a list by clicking the "Add to Favorites" button. This App is useful for film lovers with a desire to be able to easily access a library of films that they love.

 ## API

 OMDb: https://www.omdbapi.com

 This API allows users for fetch data on any movie within OMDb.

```js
     fetch(`https://www.omdbapi.com/?apikey=${apiKey}&t=${searchTerm}`)
       .then((response) => response.json())
       .then((data) => {
         setSearchTerm("");
         if (data.Error) {
           setMessage(data.Error);
           setMovie(null);
         } else {
           setMovie(data);
           setMessage("");
         }
       })
       
```
      
   


 ## Wireframes

 Wireframes: https://imgur.com/a/SvMpmR9


 ### MVP/PostMVP - 5min

 The functionality will then be divided into two separate lists: MPV and PostMVP.  Carefully decided what is placed into your MVP as the client will expect this functionality to be implemented upon project completion.  

 #### MVP
 - Find and use external API
 - Render data on page 
 - Allow user to interact with the page

 #### PostMVP

 - Add localStorage or firebase for storage

 ## Components

 | Component | Description | 
 | --- | :---: |  
 | App | This will make the initial data pull and include React Router and render the header include the nav|
 | Home | This will render the interactive OMDb API search engine and App description |
 | Favorites | This will render a list of favorite films created by user |
 | Add to list | This will render form/input user uses to add favorite films to list |
 | About | This will render information about how the App works |


 | Component | Priority | Estimated Time | Time Invetsted | Actual Time |
 | --- | :---: |  :---: | :---: | :---: |
 | Adding Form | H | 3hrs| 3.5hrs | 3.5hrs |
 | Working with API | H | 3hrs| 2.5hrs | 2.5hrs |
 | Total | H | 6hrs| 5hrs | 5hrs | 

 ## Code Snippet

 ```js
  let movieDisplay = "";
   if (movie !== null) {
     movieDisplay = (
       <div>
         <h2>Title: {movie.Title}</h2>
         <h3>Year: {movie.Year}</h3>
         <img src={movie.Poster} alt={movie.Title} />
         <h4>Genre: {movie.Genre}</h4>
         <h5>Plot: {movie.Plot}</h5>
       </div>
     );
   }
```
