<template>
  <div class="home">
    <h1 class="titulo"> Home Component </h1>
    <img alt="Vue logo" src="../assets/logo.png">
    <WatcherComponent />
    <hr>

    <ul>
        <li v-for="(price,date) in ventas" class="price" v-bind:class="{red: price<=100, green:price>100}"> 
          {{ date }} ____________ {{ price }}
        </li>
    </ul>

    <hr>

    <button v-bind:class="['btn', isError ? 'btn-danger' : 'btn-primary' ]" v-on:click="isError = !isError"> presionar</button>

    <hr>

    <p v-bind:style="{'color': colorFuenteParrafo, 'background-color': colorFondoParrafo}">
      Lorem, ipsum dolor sit amet consectetur adipisicing elit. Numquam maxime nulla in recusandae voluptate aperiam consequuntur itaque obcaecati? Ea magni doloribus deleniti mollitia sunt quia animi aperiam, porro perferendis cupiditate?
    </p>


  </div>
</template>

<script>
// @ is an alias to /src
import WatcherComponent from '@/components/WatcherComponent.vue';

export default {
  name: 'HomeView',
  components: {
    WatcherComponent,
  },
  data:function(){
    return{
      ventas:{
        '2020-01-01':100,
        '2020-01-02':200,
        '2020-01-03':30,
      },
      isError: true,
      colorFondoParrafo: 'orange',
      colorFuenteParrafo: 'brown',
    }
  },

}
</script>



<style scoped>
.red{
  color: red;
}

.green{
  color:green;
}

.price{
  letter-spacing: 4px;
}

.titulo{
  background-color: yellow;
  color: blue;
}

.btn{
  font-size: 18px;
}

.btn-primary{
  background-color: blue;
  color: white;
}

.btn-danger{
  background-color: red;
  color: yellow;
}

</style>
