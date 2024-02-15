<template>
<div class="content">
    <div class="movie" v-for="movie in movies">
   <a href="movie.trailerLink" target="_blank">
    <img :src="movie.imageUrl">
    <h3>{{movie.name}}</h3></a>
    </div>
</div>
</template>
<script setup>
import {reactive} from 'vue';
const movies = reactive([
  {
    name: "Inception",
    imageUrl: "https://m.media-amazon.com/images/M/MV5BZGFjOTRiYjgtYjEzMS00ZjQ2LTkzY2YtOGQ0NDI2NTVjOGFmXkEyXkFqcGdeQXVyNDQ5MDYzMTk@._V1_.jpg",
    trailerLink: "https://www.youtube.com/watch?v=8hP9D6kZseM"
  },
  {
    name: "The Shawshank Redemption",
    imageUrl: "https://m.media-amazon.com/images/I/91VIHzW1kvL._AC_UF1000,1000_QL80_.jpg",
    trailerLink: "https://www.youtube.com/watch?v=6hB3S9bIaco"
  },
  {
    name: "The Dark Knight",
    imageUrl: "https://images.moviesanywhere.com/bd47f9b7d090170d79b3085804075d41/c6140695-a35f-46e2-adb7-45ed829fc0c0.jpg",
    trailerLink: "https://www.youtube.com/watch?v=EXeTwQWrcwY"
  },
  {
    name: "Interstellar",
    imageUrl: "https://images.fandango.com/ImageRenderer/0/0/redesign/static/img/default_poster.png/0/images/masterrepository/Fandango/176739/Interstellar-Film.jpg",
    trailerLink: "https://www.youtube.com/watch?v=zSWdZVtXT7E"
  },
  {
    name: "The Godfather",
    imageUrl: "https://m.media-amazon.com/images/M/MV5BM2MyNjYxNmUtYTAwNi00MTYxLWJmNWYtYzZlODY3ZTk3OTFlXkEyXkFqcGdeQXVyNzkwMjQ5NzM@._V1_.jpg",
    trailerLink: "https://www.youtube.com/watch?v=sY1S34973zA"
  },
  {
    name: "Pulp Fiction",
    imageUrl: "https://m.media-amazon.com/images/M/MV5BNGNhMDIzZTUtNTBlZi00MTRlLWFjM2ItYzViMjE3YzI5MjljXkEyXkFqcGdeQXVyNzkwMjQ5NzM@._V1_.jpg",
    trailerLink: "https://www.youtube.com/watch?v=s7EdQ4FqbhY"
  },
  {
    name: "Avatar",
    imageUrl: "https://m.media-amazon.com/images/M/MV5BYjhiNjBlODctY2ZiOC00YjVlLWFlNzAtNTVhNzM1YjI1NzMxXkEyXkFqcGdeQXVyMjQxNTE1MDA@._V1_.jpg",
    trailerLink: "https://www.youtube.com/watch?v=cRdxXPV9GNQ"
  },
  {
    name: "Forrest Gump",
    imageUrl: "https://resizing.flixster.com/-XZAfHZM39UwaGJIFWKAE8fS0ak=/v3/t/assets/p15829_v_v13_aa.jpg",
    trailerLink: "https://www.youtube.com/watch?v=bLvqoHBptjg"
  },
  {
    name: "The Matrix",
    imageUrl: "https://images.moviesanywhere.com/7cd69a71b6643254b4ec1f7819923934/94aa20fe-6767-49f4-ba36-cf601f4c5d9c.jpg",
    trailerLink: "https://www.youtube.com/watch?v=m8e-FF8MsqU"
  },
  {
    name: "Fight Club",
    imageUrl: "https://m.media-amazon.com/images/M/MV5BMmEzNTkxYjQtZTc0MC00YTVjLTg5ZTEtZWMwOWVlYzY0NWIwXkEyXkFqcGdeQXVyNzkwMjQ5NzM@._V1_.jpg",
    trailerLink: "https://www.youtube.com/watch?v=SUXWAEX2jlg"
  }
]);

</script>
<style>
.content{
    margin-top:30px;
display:grid;
grid-template-columns:repeat(auto-fill,minmax(300px,1fr));
grid-gap:30px;
}
img{
    height:350px;
    width:100%;
}
a{
    text-decoration:none;
    color:black;
}
</style>