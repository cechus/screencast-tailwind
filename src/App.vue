<template>
  <!-- <div id="app" class="bg-gray-100 sm:bg-green-500 md:bg-indigo-500 lg:bg-yellow-500 xl:bg-pink-500"> -->
  <div id="app" class="bg-gray-300 antialiased ">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/house">House</router-link>
    </div>
    <router-view/>
  </div>
</template>
