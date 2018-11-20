<template>
  <div class="container index">
      <div class="card" v-for="recipe in recipes" :key="recipe.id">
        <div class="card-content">
            <h2 class="indigo-text">{{recipe.title}}</h2>
            <ul class="ingredients">
              <li v-for="(ing,index) in recipe.ingredients" :key="index">
                <span class="chip">{{ing}}</span>
              </li>
            </ul>
        </div>
      </div>
  </div>
</template>

<script>
export default {
  name: 'Index',
  data () {
    return {
      recipes:[
        {title:'Moong Dal Khichdi',slug:'moong-dal-khichdi',ingredients:['Dhuli moong dal – 1/2 cup','Rice – 1/2 cup','Salt to taste','Turmeric powder – 1/2 tsp','Desi ghee – 2 tsp','Black peppercorn – 4 to 5','Cloves – 3 to 4','Cinnamon stick -1 inch piece']}
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
  .index{
    display: grid;
    grid-template-columns:1fr 1fr 1fr;
    grid-gap:30px;
    margin-top:60px;
    h2{
      font-size:1.8rem;
      text-align: center;
      margin-top: 0;
    }
    .ingredients{
      margin:30px auto;
    }
  }
</style>
