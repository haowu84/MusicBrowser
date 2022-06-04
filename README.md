# Music Browser with Angular, Express

## Structure
- webserver/client_secret.json: secret information
- webserver/tokens.json: secret information
- webserver/routes/index.js: communicate with the Spotify API

- client/src/app/components: folder that contains 6 components: about, carousel, carousel-card, search, track-list, and thermometer
- client/src/app/pages: folder that contains 4 components: home-page, album-page, artist-page, and track-page
- client/src/app/services: folder that contains 1 service
- client/src/app/data: folder that contains 6 data types

## Setup
- Installing Angular Command Line Interface (CLI): ```npm install -g @angular/cli```
- Running the webserver: ```npm start```
- Running the client: ```ng serve```

## Summary
### Communicate with the Webserver
- Handle OAuth flow between the Spotify server and the webserver
- Authenticate and authorize access
- Refresh access token when it expires
- Make API requests with Sportfy service and return appropriate data type for each API call

### Home Page
- View user information (name, profile picture, and profile link) upon login
- Trigger search request (input and select/dropdown that declares data type) to Spotify API and map responses (JSON) to into an array of the appropriate resource type (object): Artist, Album, or Track
- Display the search results in a carousel component (Bootstrap carousel) or a track-list component (Bootstrap table)

### Artist Page
- Retrieve the basic information about the artist, top tracks, albums, and similar artists
- Display the albums/similar artists with carousel and top tracks with track-list components

### Album Page
- Retrieve the basic information about the album and tracks
- Display the tracks with track-list component

### Track Page
- Retrieve the basic information about the track and audio features
- Display the track's audio features with a thermometer component (Bootstrap progress bar)
