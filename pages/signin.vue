<!-- eslint-disable vue/singleline-html-element-content-newline -->
<template>
  <div>
    <h1 class="game-name">SOS GAME</h1>
    <v-card class="mx-auto" max-width="344" style="    padding: 20px;" variant="outlined">
      <v-card-item>
        <div>
          <div class="text-caption">
            Enter your game name
          </div>
          <v-text-field placeholder="crazyMan_00" variant="outlined" />
        </div>
      </v-card-item>

      <v-card-actions>
        <v-btn class="border-gradient border-gradient-purple" block variant="outlined"> Start </v-btn>
      </v-card-actions>
      <v-card-actions>
        <v-btn class="border-gradient border-gradient-purple" block variant="outlined"> Leaderboard  </v-btn>
      </v-card-actions>
    </v-card>
  </div>
</template>
<script>
export default {
  name: 'Signin',
  layout: 'starsLayout'
}
</script>
<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300&family=Rubik+Iso&display=swap');
.game-name{
  font-size: 3em;
  font-family: 'Poppins', sans-serif;
font-family: 'Rubik Iso', cursive;
color: #FF5F9E;
    text-shadow: 0px -2px 6px;
    letter-spacing: 9px;
    filter: drop-shadow(0px 3px 3px #E90064);
    text-align: center;
}
.border-gradient {
  background: linear-gradient(white, white) padding-box, linear-gradient(to right, darkblue, darkorchid) border-box;
    border: 2px solid transparent;
}

</style>
