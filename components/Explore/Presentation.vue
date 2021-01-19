<template>
  <div class='container'>
    <vs-row vs-w="12">
      <vs-col vs-type="flex"  vs-lg="6" vs-sm="12" vs-xs="12">
        <div class='image'>
          <img  src="../../assets/images/Presentation-BG.png" alt="">
          <div class='image__iconbox '>
            <div class="image__icon">
              <i class='bx bx-chevron-left'></i>
            </div>
            <div class="image__icon active">
              <i class='bx bx-chevron-right'></i>
            </div>
          </div>
        </div>
      </vs-col>
      <vs-col vs-type="flex" vs-justify="center" vs-align="center" vs-lg="6" vs-sm="12" vs-xs="12">
        <div class='text'>
         <p class='text__title'>PRÉSENTATION</p>
         <p class='text__subtitle'>Découvrez ce qui vous entoure comme jamais auparavant. Dénichez les trésors cachés de l'ile de ré.</p>
         <p class='text__content'><strong>L’Île de Ré</strong>, reliée au continent par un pont, à une superficie de 85 km
         et une longueur de 32 km. Sa largeur varie de 5 km à 100 mètres à peine, au passage du <strong>Martray</strong>.
         Dans les terres, on découvre à <strong>vélo</strong> les vignes, les champs exploités puis plus au nord le spectacle des <strong> marais salants</strong>.</p>
         <br>
         <p class='text__content'>Le long des dix villages, partez à la découverte du <strong>patrimoine</strong>, des ports
         et de la riche histoire insulaire. Le littoral présente des aspects très différents <strong> : dunes, petites
         falaises, rochers, longues plages de sable fin ..</strong></p>
        </div>
      </vs-col>
    </vs-row>

  </div>
</template>

<style lang='scss' scoped>
  .image {
    position:relative;
    &__iconbox {
      border-top-left-radius:86px;
      position:absolute;
      right:0;
      bottom:0;
      background-color:white;
      display:flex;
      padding-top:30px;
      padding-left:48px;

    }
    &__icon{
      width:54px;
      height:54px;
      display:flex;
      justify-content:center;
      align-items:center;
      border:1px solid #3B96D2;
      border-radius:8px 0;
      &:first-child {
        margin-right:28px;
      }
      &.active{
        background-color:#3B96D2;
        i {
          color:white;
        }
      }
      i{
        font-size:36px;
        font-weight: normal;
        color:#3B96D2

      }
    }
  }
  .text{
    padding-top:16px;
    padding-left:100px;
    &__title {
        font-size:28px;
        color: #3B96D2;
        padding-bottom:15px;
    }
    &__subtitle {
       @include font(35px, 51px,normal);
       padding-right:37px;
    }
    &__content {
       padding-top:28px;
       @include font(20px, 36px);
    }
  }


</style>
