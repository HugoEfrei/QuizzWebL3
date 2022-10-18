<template>
<body class="body">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/css/bootstrap.min.css"
rel="stylesheet"
integrity="sha384-gH2yIJqKdNHPEq0n4Mqa/HGKIhSkIHeL5AyhkYV8i59U5AR6csBvApHHNl/vI1Bx"
crossorigin="anonymous">

<img class="logocafe" alt="cafe_logo" src="../src/assets/logo-cafe.png">
<h1 class="namecafe">CAFE <span class="namecafe2">STREET</span></h1>
<div class="container text-center">
  <div class="nav_bar"> 
  <nav>
    <router-link to="/about">About us</router-link>  &nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp; 
    <router-link to="/FirstView">View</router-link> &nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;
    <router-link to="/">Home</router-link>
  </nav>
  </div>
</div>
  <router-view/>
</body>
</template>

<script>


</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.logocafe{
    width: 100px; 
}

.namecafe{
  color: #E0924B;
  font-style: italic;
  font-family: "STXingkai";
}

.namecafe2{
  color: rgb(165, 95, 42);
}

.nav_bar{
  font-size:larger;
  background-color: rgb(255, 226, 183);
  border : 3px solid #E0924B; 
  border-radius: 10px;
}

nav {
  padding: 15px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #E0924B;
    }
  }

  a:hover{
    color: #E0924B;
  }
  
}

.body{
  background-color: rgb(255, 235, 204);
  background-image: url("../src/assets/fond_cafe.png"),url("../src/assets/fond_cafe.png") ;
  background-position: top right, bottom left;  
  background-size: auto;
  background-repeat: no-repeat;
   
  
  
}

html{
  background-color: rgb(255, 235, 204);
  
}

button {
    font-size: 1.1em;
    background-color: antiquewhite;
    color: brown;
    border: 2px solid black;
    box-shadow: 4px 4px 4px #999999;
  }
  button:hover {
    /* swap colors */
    color: #EBF5FF;
    background-color: rgb(165, 95, 42);
    cursor: pointer; /* displays a hand */
  }

</style>
