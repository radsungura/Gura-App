<template>
  <div>
      
    <p v-if="$fetchState.pending">Chargement....</p>
    <p v-else-if="$fetchState.error">
      Erreur lors de la récupération des montagnes
    </p>
    <div v-else>
      
    <b-card v-for="(beer, index) in beers" :key="index" :img-src="beer.image_url" img-alt="Card image" img-left class="mb-3">
      <b-card-text>
        {{ beer.name }}
      </b-card-text>
      <b-card-text>
        {{ beer.category }}
      </b-card-text>
      <b-card-text>
        {{ beer.brewer }}
      </b-card-text>
      <b-card-text>
        {{ beer.style }}
      </b-card-text>
      <b-button class="buton">
        Par aime
      </b-button>

    </b-card>
    
    </div>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        beers: []
      }
    },
    async fetch() {
      this.beers = await fetch(
        'https://api.nuxtjs.dev/beers'
      ).then(res => res.json())
    }
  }
</script>
<style>
.buton{display: flex;
flex-direction: row;
justify-content: center;
align-items: center;
padding: 8px 12px;

position: static;
width: 204px;
height: 36px;
left: 12px;
top: 47px;

/* Success */

background: #0CB345;
border-radius: 6px;

/* Inside Auto Layout */

flex: none;
order: 1;
flex-grow: 0;
margin: 16px 0px;}

</style>