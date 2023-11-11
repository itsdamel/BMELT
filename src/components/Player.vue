
<template>
    <div id="player">
        <div id='date'>
            <Line />
            <h2>02/01</h2>
        </div>
        <div id='song'>
            <div id='song-cover'>
                
            </div>
            <div id='song-info'>
                <span>PLAYING NOW</span>
                <a href='https://music.apple.com/br/artist/bright-eyes/6547614' target='_blank'>
                    BRIGHT EYES
                </a>
                <p>02. LUA</p>
            </div>
        </div>
        <div id='controlls'>
            <img alt='previous' src='../assets/svg/previous-controller.svg'/>
            <img id='play' :class="{spinning: playerOn}" alt='play' @click="handlePlayer" src='../assets/svg/play-controller.svg'/>
            <img alt='next' src='../assets/svg/next-controller.svg'/>
        </div>
    </div>
</template>

<script setup>
   
    import Line from './Line.vue';
    const props = defineProps(['playerOn'])
    const emit = defineEmits(['handle-player'])
    const handlePlayer = () =>{
        emit('handle-player') 
    }    
  
    
</script>
<style scoped>
   
    
    #player{
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 100vw;
        position: absolute;
        bottom: 20px;
        z-index: 3;
        height: 120px;
        background: linear-gradient(90deg, rgba(140, 102, 165, 0.20) 1.1%, rgba(179, 178, 193, 0.20) 90.1%);
        backdrop-filter: blur(31.24287223815918px);
    
    }
    #date{
        width: 20%;
        display: flex;
        align-items: center;
        height: 100%;
        gap: 30px;
    }
    #date h2{
        font-size: 50px;
        font-style: italic;
        font-weight: 100;
    }
    #song{
        display: flex;
        align-items: center;
        gap: 40px;

        width: 35%;
    }

    #song-cover{
        width: 120px;
        height: 120px;
        background-image: url('../assets/img/album-cover.png');
        background-size: cover;
        background-position: top;
    }
   
    #song-info span{
        font-size: 18.066px;
        font-weight: bold;
        background: linear-gradient(180deg, #7c1755 0%, rgba(64, 40, 199, 0.842) 100%);
        background-clip: text;
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
    }
   
    #song-info p, #song-info a{
        font-size: 19px;
        letter-spacing: 2.8px;
    }
    #song-info a{
        display: block;
        color: #fff;
        text-decoration: none;
        font-weight: normal;
    } 
    #song-info p{
        font-weight: 100;
    }
    #controlls{
        width: 25%;
        display: flex;
        justify-content: space-evenly;
        display: flex;
    }
    #controlls img{
        cursor: pointer;
    }
    /* animation */
    .spinning{
        animation: loading 4s linear infinite;
    }

    @keyframes loading {
        0% {
            transform: rotate(0deg);
        }
        100% {
        transform: rotate(360deg);
        }   
    }
</style>