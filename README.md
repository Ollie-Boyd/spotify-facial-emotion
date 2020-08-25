# Spotify playlist generator based on perceived facial emotion

### Screenshots of finished webapp
<p align="center">
<img src="https://raw.githubusercontent.com/Ollie-Boyd/spotify-facial-emotion/master/screenshots/Screen_Recording_2020_08_25_at_17_42_46.gif" width=50% height=auto%>
  <img src="https://raw.githubusercontent.com/Ollie-Boyd/spotify-facial-emotion/master/screenshots/Screen_Recording_2020_08_25_at_17_42_46%20(1).gif" width=50% height=auto%>
 <img src="https://raw.githubusercontent.com/Ollie-Boyd/spotify-facial-emotion/master/screenshots/spicify_login.png" width=80% height=auto%>
  <img src="https://raw.githubusercontent.com/Ollie-Boyd/spotify-facial-emotion/master/screenshots/cam_view.png" width=80% height=auto%>
 <img src="https://raw.githubusercontent.com/Ollie-Boyd/spotify-facial-emotion/master/screenshots/playlist_view.png" width=80% height=auto%>
</p>

## Brief
As our cohort was pretty strong we had an open brief to choose our tech stack and brief.
5 was the biggest group I'd worked with on a project however it only took an hour or so to go from absolutely no ideas to the idea of combining facial emotional recognition with the Spotify API (which contains emotional traits in the song API) and making a playlist generator based on a user's existing playlists. 

## Planning
We made database relationship diagrams, 5 sets of wireframes (one per person then cherry-picked features we liked), and mapped out the React components. 
We split up the reasearch, I researched various facial-recognition libraries and APIs and a bit on accessing the webcam. I opted for the Azure API as the emotion API response looked promising and the documentation looked fairly thorough. 

<p align="center">
 <img src="https://raw.githubusercontent.com/Ollie-Boyd/spotify-facial-emotion/master/screenshots/api.png" width=80% height=auto%>
 </p>
 
We had originally opted for a Java backend but after spending a whole day mob coding the Spotify OAuth 2.0 API without success we opted for a switch to Node as there was a lot more Node documentation. 

## What I learned. 
I learned a whole heap from this project. I wrote the code taking the image from webcam to the backend a base64 encoded jpg. In Node I converted the base64 image to a binary Blob which could be streamed to the Azure endpoint. 
I converted the emotional JSON returned from the API to an emotional valence figure and married the facial emotion to matching Spotify songs returned from the API.
I had never dealt with images in code, their encoding and transcoding was new to me and so it was good to learn about JavaScript Streams to bitstream the image to Azure. 

After that was done I focused on React and made the webcam ring with emoji slider, and the playbar as well as helping my team mates out with their CSS. 

## To run

### /frontend/

```
npm install
```
```
npm run serve
```

### /backend_node/

```
npm install
```
```
npm run server:dev
```
