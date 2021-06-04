<template>
 <div>
     <div class="center"  v-for="item in products" v-bind:key="item.item" >
  <b-card img-alt="rad" :img-src="item.source" class="td">
    <b-card-text>
    <label variant=" float-left" for="product">{{item.item}}</label>
      <label variant=" float-right" for="product">{{item.price}}Fbu</label>
       </b-card-text>
    <b-button  variant="primary float-left">
      like
    </b-button>
    <b-button  variant="success float-right">
      buy
    </b-button>
  </b-card>
</div>
    </div>
</template>
<script>
export default {
  name: 'Product',
   data() {
    return {
     products:[ {item: 'pizza',price: 1500,desc:'the best pizza made in burundi with burundian products', source : require('@/assets/agro/product1.jpeg')},
                {item: 'haricot',price: 1200,desc:'Haricots de kirundo ', source : require('@/assets/agro/product2.jpg') },
                {item: 'riz',price: 1000,desc:'The best rice in burundi from Gihanga ', source : require('@/assets/agro/product3.jpg') },
                {item: 'pizza',price: 2000,desc:'Delicious flavered and chip ', source : require('@/assets/agro/product1.jpeg') },
                {item: 'pizza',price: 1500,desc:'the best pizza made in burundi with burundian products', source : require('@/assets/agro/product1.jpeg')},
                {item: 'haricot',price: 1200,desc:'Haricots de kirundo ', source : require('@/assets/agro/product2.jpg') },
                {item: 'riz',price: 1000,desc:'The best rice in burundi from Gihanga ', source : require('@/assets/agro/product3.jpg') },
                {item: 'pizza',price: 2000,desc:'Delicious flavered and chip ', source : require('@/assets/agro/product1.jpeg') }
                ]
    }
  }

}
</script>
<style scoped>
.center{
 
  text-align: center;
}
.price{
 text-decoration:bold ;
  
 margin-left: 30%;
}
.name{
 text-decoration:bold ;
 margin-left: 0px;
}
.like{ margin-bottom: 10px;
   background-color: rgb(34, 76, 139);
 color: white;
 margin-right: 30%;
 width: 30%;
 height:  45%;
}
.see{ margin-bottom: 10px;
 background-color: forestgreen;
  color: white;
 width: 30%;
 height:  45%;
}
.logo {
 width: 100px;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
div {
  display:inline-block;
  margin: 0 10px;
}
.td{
  background-color: rgb(231, 228, 228);
  display: inline-block;
   width:250px;
  border-radius:5px;
  margin-bottom: 30px;
}
.block{
  display: inline-block;
  margin-bottom:30px;
 
}
tr{
  width: 100%;
}
img{ border-top-right-radius: 5px;
border-top-left-radius: 5px;
  width: 100%;
}
button{
  border-radius:10%;
  color: aliceblue;
  size:50px;
}

</style>
