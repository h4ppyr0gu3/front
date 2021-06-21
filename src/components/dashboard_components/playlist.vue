<template>
<div class="columns" style="overflow-x: hidden;">
<div class="column is-3 is-centered-middle">
  <img class="icon" style="float:left; flex:;" :src="require('@/assets/images/video-playlist.svg')">
</div>
<div class="column is-centered-middle" style="overflow-y: hidden;">
  <div class="sidebar-items" style="flex:70%;float: left; overflow-y: hidden;">
    {{title}}
  </div>
</div>
</div>
<hr>
</template>

<script>
export default {
  name: 'Playlist',
  props: {
    title: String
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