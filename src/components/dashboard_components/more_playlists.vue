<template>
<div class="scroll" >
    <ul id="example-1">
      <li v-for="i in playlists" :key="i">
        <Playlist :title="i"/>
      </li>
    </ul>
  </div>
</template>
