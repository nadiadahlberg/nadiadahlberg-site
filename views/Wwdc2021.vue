<template>
    <div>
      <img
        src="@/assets/Wwdc/ssc2021.jpg"
        alt="Swift Student Challenge"
        class="hero"
      />
      <div class="inner-content">
        <h3 class="heading"><b>I do:</b></h3>
        <p class="paragraph">
          Text här.
        </p>
      </div>
    
      
      <div class="video">
        <embed
          src="https://www.youtube.com/embed/qGlhv0LeLVE?autohide=1&autoplay=0"
          wmode="transparent"
          type="video/mp4"
          width="100%"
          height="100%"
          allow="autoplay; encrypted-media; picture-in-picture"
          allowfullscreen
          title="WWDC Interview"
        />
      </div>
    </div>
  </template>
  
  <style scoped>
  .hero {
    width: 100%;
    background-position: center center;
    background-size: 100%;
    background-repeat: no-repeat;
    border: 1px solid rgb(0, 0, 0, 0.1);
  }
  
  .images {
    width: 100%;
    height: auto;
    /* object-fit: cover; */
  }
  
  .images-full {
    width: 100%;
    height: auto;
    object-fit: cover;
  }

  .video {
    width: 100%;
    height: 350px;
  }
  
  .subtitle {
    font-size: 12px;
    color: gray;
    text-align: center;
  }
  
  .heading {
    padding-bottom: 5px;
  }
  
  .inner-content {
    padding-top: 30px;
    padding-bottom: 30px;
  }
  
  h6,
  h3 {
    margin: 0;
    padding: 0;
  }
  </style>
  
