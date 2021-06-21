<template style="height:50px">
	<div class="row pt-3" style="position:relative;min-width:100%;">
    <div class="row" style="width:10%">
      <div class="arrows vertical-center is-centered-middle" >
        <div  style="width:25%;">
          <a class="arrow left vertical-center" style="float: left;"></a>
        </div>
        <div style="width:25%;align-content: right">
          <a class="arrow right vertical-center" style="float: left;"></a>
        </div>
      </div>
    </div>
    <div class="search is-centered-middle">
      <form class="form">
      <input  placeholder="Search" class="search-field" />
      <button class="search-button">
        <img :src="require('@/assets/images/search.svg')">
      </button>
    </form>
    </div>
    <div class="profile" style="vertical-align: middle; overflow: hidden;">
      <div class="cursor" style=" width:80%;height:100%;color: #f6f7eb; overflow: hidden; vertical-align: middle; padding:3px">
        David R...
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<style scoped>
.row {
  display: flex;
  width: 100%;
  max-height: 40px;
}
.arrows {
  width: 10%;
}
.search {
  width: 80%;
}
.profile {
  width: 10%;
}
.is-centered-middle {
  display: flex;
  justify-content: center;
  align-items: center;
}
.is-flex-column {
  flex-direction: column;
}
.is-flex-row {
  flex-direction: row;
}
.input:hover, .input:active, .input:focus {
  border-color: #C0F9FA;
}
.input {
  background-color: #f6f7eb;
}
.input:focus {
  border-color: #C0F9FA;
}
.title {
  color: #C0F9FA;
}
.arrow {
  border: solid #f6f7eb;
  border-width: 0 3px 3px 0;
  display: inline-block;
  padding: 3px;
}

.right {
  transform: rotate(-45deg);
  -webkit-transform: rotate(-45deg);
}

.left {
  transform: rotate(135deg);
  -webkit-transform: rotate(135deg);
}

.vertical-center {
  margin: 0;
  position: absolute;
  top: 50%;
  /*-ms-transform: translateY(-50%);
  transform: translateY(-50%);*/
}

.form {
  display: flex;
  flex-direction: row;
  width: 60%;
}
.search-field {
  width: 100%;
  padding: 10px 35px 10px 15px;
  border: none;
  border-radius: 100px;
  outline: none;
  background-color: #f6f7eb;
}

.search-button {
  background: transparent;
  border: none;
  outline: none;
  margin-left: -33px;
}

.search-button img {
  width: 20px;
  height: 20px;
  object-fit: cover;
}

.cursor:hover {
  cursor: pointer;
}


</style>