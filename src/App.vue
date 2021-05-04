<template>
  <div id="nav">
    <router-link to="/">Home</router-link> 
    <router-link :to="{name: 'About'}">About</router-link> 
    <router-link :to="{name: 'Jobs'}">Jobs</router-link>
    <div class="button">
      <button @click="back">Back</button>
      <button @click="redirect">Redirect</button>
      <button @click="next">Next</button>
    </div>
  </div>
  <router-view/>
</template>

<script>
  export default{
    methods: {
      back() {
        this.$router.go(-1)
      },
      next() {
        this.$router.go(+1)
      },
      redirect() {
        this.$router.push({name: 'Home'})
      }
    }
  }
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.button{
  margin-top: 20px;
}
.button button{
  margin-top: 10px;
  padding: 10px 15px;
  margin-right: 5px;
  margin-left: 5px;
  border: none;
  border-radius: 3px;
  cursor: pointer;
  font-size: 18px;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
  margin: 5px;
  padding:  10px;
}

#nav a.router-link-exact-active {
  color: white;
  background-color: limegreen;
  border-radius: 5px;
}
p{
  padding: 20px;
  margin: 0 20px;
}
</style>
