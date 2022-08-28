<template>
  <div class="home">
    <div class="feature-card">
      <router-link to="/movie/tt0409591">
        <img class="featured-img" src="https://images.alphacoders.com/144/thumb-1920-144563.jpg" alt="The Dark Knight Poster">
        <div class="detail">
          <h3>The Dark Knight Rises</h3>
          <p>Eight years after the Joker's reign of anarchy, Batman, with the help of the enigmatic Catwoman, is forced from his exile to save Gotham City from the brutal guerrilla terrorist Bane.</p>
      </div>
      </router-link>
    </div>

    <form @submit.prevent="" class="search-box">
      <input type="text" placeholder="What are you looking for?" />
      <input type="submit" value="Search" />
    </form>

    <div class="movies-list">MOVIES</div>

  </div>
</template>

<script>

export default {
 
}
</script>

<style lang="scss">
  .home{
    .feature-card{
      position: relative; 
      .featured-img{
        display: block; 
        width: 100%; 
        height: 300px; 
        object-fit: cover; 

        position: relative; 
        z-index: 0; 
      }
      .detail {
        position: absolute; 
        left: 0; 
        right: 0; 
        bottom: 0; 
        background-color: rgba(0, 0, 0, 0.6);
        padding: 16px; 
        z-index: 1; 

        h3{
          color: #FFF;  
          margin-bottom: 16px; 
        } 

        p{
          color: #FFF; 
        }
      }
    }
    .search-box{
      display: flex;
      flex-direction: column; 
      justify-content: center;
      align-items: center; 
      padding: 16px;  

      input{
      display: block;
      appearance: none;
      border: none; 
      outline: none; 
      background: none;

      &[type = "text"] {
        width: 100%;
        color: #FFF;
        background-color: #496583;
        font-size: 20px;
        padding: 10px 16px;
        border-radius: 8px; 
        margin-bottom: 15px;
        transition: 0.4s;
        
        &::placeholder {
          color: #f3f3f3;
        }

        &:focus {
          box-shadow: 0px 3px 6px rgba(0, 0, 0, 0.2); 
        }
      }
      &[type = "submit"] {
        width: 100%;
        max-width: 300px;
        background-color: #42B883;
        padding: 16px;
        border-radius: 8px;
        color: white;
        font-size: 20px;
        text-transform: uppercase;
        transition: 0.4s;
        
        &:active {
          background-color: #3B8070;
        }
      }
    }
  }
   
  }
</style>
