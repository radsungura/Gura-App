<template>
  <div >
   
  <b-nav pills style="background-color:black;">
    <b-nav-item ><NuxtLink to="/">Home</NuxtLink></b-nav-item> 
    <b-nav-item><NuxtLink to="/pannier">Pannier</NuxtLink></b-nav-item>
    <b-nav-item><NuxtLink to="/about">About</NuxtLink></b-nav-item>
    <b-nav-item-dropdown
      id="my-nav-dropdown"
      text="Categorie"
      toggle-class="nav-link-custom"
      right
    >
      <b-dropdown-item><NuxtLink to="/">Voiture</NuxtLink></b-dropdown-item>
      <b-dropdown-item><NuxtLink to="/">Restaurant</NuxtLink></b-dropdown-item>
      <b-dropdown-divider></b-dropdown-divider>
      <b-dropdown-item><NuxtLink to="/">Fashion</NuxtLink></b-dropdown-item>
    </b-nav-item-dropdown>
  </b-nav>
   <Nuxt />
</div>
</template>