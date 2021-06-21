<template>
  <div style="height:90vh; position: static;" >
  <h1 class="is-size-2" style="color:#C0F9FA;">musicApp</h1>
	<hr>
  <div class="columns cursor highlight pl-3">
    <div class="column is-3 is-centered-middle">
      <img class="icon" style="float:left; flex:;" :src="require('@/assets/images/star-full.svg')">
    </div>
    <div class="column is-centered-middle">
      <div class=" sidebar-items" style="flex:70%;float: left;font-weight: bold;">
        Favourites
      </div>
    </div>
  </div>
  <hr>
   <div class="columns cursor highlight pl-3">
    <div class="column is-3 is-centered-middle">
      <img class="icon" style="float:left; flex:;" :src="require('@/assets/images/vinyl.svg')">
    </div>
    <div class="column is-centered-middle">
      <div class=" sidebar-items" style="flex:70%;float: left;font-weight: bold;">
        Tracks
      </div>
    </div>
  </div>
  <hr>
  <div class="columns cursor highlight pl-3">
    <div class="column is-3 is-centered-middle">
      <img class="icon" style="float:left; flex:;" :src="require('@/assets/images/compass.svg')">
    </div>
    <div class="column is-centered-middle">
      <div class=" sidebar-items" style="flex:70%;float: left;font-weight: bold;">
        Explore
      </div>
    </div>
  </div>
  <hr>
  <div class="columns cursor highlight pl-3">
    <div class="column is-3 is-centered-middle">
      <img class="icon" style="float:left; flex:;" :src="require('@/assets/images/cluster-data.svg')">
    </div>
    <div class="column is-centered-middle">
      <div class="sidebar-items" style="flex:70%;float: left;font-weight: bold;">
        Friends
      </div>
    </div>
  </div>
  <hr>
  <div style="height:50px"></div>
  <div class="columns pl-3">
    <div class="column is-3 is-centered-middle">
      <img class="icon" style="float:left; flex:;" :src="require('@/assets/images/video-playlist.svg')">
    </div>
    <div class="column is-centered-middle">
      <div class="sidebar-items" style="flex:70%;float: left;font-weight: bold;">
        Playlists
      </div>
    </div>
  </div>
  <hr>
    <ul id="example-1">
      <li v-for="i in playlists.slice(0, 5)" :key="i">
        <Playlist :title="i"/>
      </li>
    </ul>
    <div>
      show more
    </div>
  </div>
</template>

<script>

import Playlist from './dashboard_components/playlist'
export default {
  name: 'Sidebar',
    components: {
    Playlist
  },
  data: function () {
    return {
      playlists: [
      "a","b","c","d","e","f","g","h"
      ]
    }
  }
}
</script>

<style scoped>
hr {
  margin: 0px;
  border: none;
  height: 1px;
  color: #333; /* old IE */
  background-color: #333; /* Modern Browsers */
}

.scroll {
  height: 40%;
  overflow-y: scroll;
  overflow-x: hidden;
}

::-webkit-scrollbar {
  width: 5px;
}
::-webkit-scrollbar-track {
  box-shadow: inset 0 0 5px grey;
  border-radius: 10px;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: #92F294;
  border-radius: 500px;
}

.sidebar-items {
  color: #f6f7eb;
}
.row {
  display: flex;
  width: 100%;
}
.column {
  padding:0px;
  margin: 0px;
  border: 0px;
}
.columns {
  height: 48px;
  padding:0px;
  margin: 0px;
  border: 0px;
}

.is-centered-middle {
  display: flex;
  justify-content: center;
  align-items: center;
}
.cursor {
  cursor: pointer;
}
.highlight:hover {
  background-color: #333;
}
</style>