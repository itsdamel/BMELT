<script setup>
    import Player from './Player.vue';
</script>
<template>
    <div class='banner'>
        <span class='background-letter' id='uimusic'>UIMUSIC</span>
        <span class='background-letter' id='newway'>NEWWAY</span>
       <!--  <span class='background-letter'>NEWWAY</span> -->
        <div id='main-content'>
            <h1>
                PLAY.
            </h1>
            <p>
                Be the first to hear new tracks, connect directly with fellow fans and your favorite artists in real time, and support the future of music with every play, like, repost and comment
            </p>
            <div id='download-content'>
                <img src='../assets/svg/apple-icon.svg' class='store-icon'/>
                <img src='../assets/svg/android-icon.svg' class='store-icon'/>
                <button id='download-button'><a href='https://www.linkedin.com/in/mel-de-melo-dev/' target="_blank">DOWNLOAD</a></button>

            </div>
        </div>
        <div>
            <img id='cover-girl' src='../assets/img/banner-girl.png' alt=''/>
        </div>
        <Player />
    </div>
</template>

<style scoped>
    /*Background text*/
    .background-letter{
        position: absolute;
        width: 300%;
        font-weight: 800;
        color: rgba(254, 254, 254, 0.07);
        z-index: 1;
        font-size: 380px;
        -webkit-touch-callout: none;
        -webkit-user-select: none;
        -khtml-user-select: none;
        -moz-user-select: none;
        -ms-user-select: none;
        user-select: none;
    }
     
    #uimusic{
        top: -15%;
        left: -10%;
    }
    #newway{
        bottom: -5%;
        left: -10%;
    }
    /*Banner*/
    .banner, #main-content, #download-content{
        display:flex;
    }
    .banner{
        position: relative;
        width: 90vw;
        z-index: 2;
        align-items: center;
        justify-content: space-around;
        height: 100vh;
    }

    .banner h1{
        font-size: 170px;
        text-shadow: 0px 4.1504716873168945px 21.897809982299805px rgba(0, 0, 0, 0.39);   
    }
    .banner p{
        font-size: 20px;
        font-weight:100;
        max-width: 440px;
    
    }
    #main-content{
        position: relative;
        z-index: 3;
        height: 100%;
        justify-content: center;
        margin-bottom: 100px;
        flex-direction: column;
        gap: 20px;
    }
    #download-content{
        width: fit-content;
        gap: 30px;
    }

    #download-content button{
        font-size: 14px;
        
        cursor: pointer;
        font-weight: 800;
        border: 0;
        border-radius: 20px;
        padding: 10px 30px;        
    }
    #download-content button a{
        color: #c43153;
        text-decoration: none;
    }
    #download-content button:hover > a{
        color: #68242f;
    }

    #cover-girl{
        position: relative;
        z-index: 1;
        max-height: 660px;
    }
</style>