<template>
  <div class="show_tv">
    <div class="body_wrapper">
      <div>
        <iframe class="video_player" width="735" height="409" src="https://www.youtube.com/embed/5dvPIdBNbEI" title="Рик и Морти - Фальшивые двери"
          frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen>
        </iframe>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.show_tv {
  width: 100%;
  height: 100vh;
  margin: 0 auto;
  
    .body_wrapper {
      background-image: url(../assets/image/r&m_4.jpg);
      background-repeat: no-repeat;
        background-size: cover;
        background-position: center;
        height: 100%;

          .video_player{
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            top: 100px;
            
          }
    }
}
</style>