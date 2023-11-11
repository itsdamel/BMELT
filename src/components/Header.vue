<script setup>
    import Line from './Line.vue';
</script>
<template>
    <header >
        <span id='logo'>B</span>
        <div class="search">
            <div>
            <input type="text" placeholder="Any special request?" required>
            <Line />
            </div>
        </div>
        

    </header>
</template>
<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Pattaya&display=swap');
 
    #logo{
        left: 5%;
        font-family: 'pattaya', sans-serif;
        font-size: 50px;
        
    }

    #logo:hover > span{
        visibility: visible;
        animation: flip 2s infinite;
        animation-delay: calc(.2s * var(--i))
    }
   
    #logo, .search{
        position: absolute;
        height: fit-content;
        top: 10%; 
        z-index: 1;
    }
    .search{
        right: 0;
        z-index: 3; 
    }
    #line-div{
        width: 54px;
        display: inline-block;
        height: 2px;
        background: #FFF;
        
    }

   /*Animation*/
  .search div{
    display: flex;
    align-items: center;
    gap: 20px;
  }
  .search > div > input {
        color: #fff;
        font-size: 16px;
        background: transparent;
        width: 25px;
        height: 25px;
        padding: 20px;
        border: 2px solid #cccaca;
        outline: none;
        border-radius: 35px;
        transition: width 0.5s;
    }
  
  .search input::placeholder {
        color: #cccaca;
    }
  .search > div > input:hover, .search > div > input:not(:placeholder-shown) {
        width: 250px;
  }
  
</style>