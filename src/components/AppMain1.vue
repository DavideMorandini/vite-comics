<script>  
  import AppComic from './AppComic.vue';
  export default {
    data () {
      return {
        comics: [
          {
            "thumb": "../../public/img /jumbotron.jpg",
            "price": "$19.99",
            "series": "Action Comics",
            "type": "comic book"
          },
          {
            "thumb": "../../public/img /jumbotron.jpg",
            "price": "$3.99",
            "series": "American Vampire 1976",
            "type": "comic book"
          },
          {
            "thumb": "../../public/img /jumbotron.jpg",
            "price": "$16.99",
            "series": "Aquaman",
            "type": "graphic novel"
          },
          {
            "thumb": "../../public/img /jumbotron.jpg",
            "price": "$2.99",
            "series": "Batgirl",
            "type": "comic book"
          },
          {
            "thumb": "../../public/img /jumbotron.jpg",
            "price": "$3.99",
            "series": "Batman",
            "type": "comic book"
          },
          {
            "thumb": "../../public/img /jumbotron.jpg",
            "price": "$2.99",
            "series": "Batman Beyond",
            "type": "comic book"
          },
          {
            "thumb": "../../public/img /jumbotron.jpg",
            "price": "$3.99",
            "series": "Batman/Superman",
            "type": "comic book"
          },
          {
            "thumb": "../../public/img /jumbotron.jpg",
            "price": "$4.99",
            "series": "Batman/Superman Annual",
            "type": "comic book"
          },
          {
            "thumb": "../../public/img /jumbotron.jpg",
            "price": "$5.99",
            "series": "Batman: The Joker War Zone",
            "type": "comic book"
          },
          {
            "thumb": "../../public/img /jumbotron.jpg",
            "price": "$6.99",
            "series": "Batman: Three Jokers",
            "type": "comic book"
          },
          {
            "thumb": "../../public/img /jumbotron.jpg",
            "price": "$4.99",
            "series": "Batman: White Knight Presents: Harley Quinn",
            "type": "comic book"
          },
          {
            "thumb": "../../public/img /jumbotron.jpg",
            "price": "$16.99",
            "series": "Catwoman",
            "type": "graphic novel"
          }
        ]
      };
    },

    components: {
      AppComic,
    }
  }
</script>


<template>
    <div class="container">
       <div class="container-centered">
            <div id="box-title">
              <h2>Current Series</h2>
            </div>
            <AppComic  v-for="comic in comics" :img="comic.thumb" :title="comic.series"></AppComic>
            <button id="load-button">
              <a href="#">LOAD MORE</a>
            </button>
       </div>
    </div>
</template>


<style lang="scss" scoped>

@mixin blueSquare() {
  background-color: #0282f9;
  color: white;
  font-weight: bold;
  border: none;
  padding: 10px 35px;
}
  .container {
    display: flex;
    flex-flow: row wrap;
    background-color: #1c1c1c;
    text-transform: uppercase;

      &-centered {
        display: flex;
        flex-flow: row wrap;
        justify-content: center;
        align-items: baseline;
        gap: 15px;
        position: relative;
        padding-top: 40px;

          #box-title h2 {
            @include blueSquare();
            position: absolute;
            top: 0;
            transform: translate(0, -50%);
          }

          AppComic {
            width: calc(100% / 6 - (15px / 6 * 5));
          }

          #load-button {
            @include blueSquare();
            margin: 10px auto;

            &:hover {
              scale: 1.1;
            }

            a {
              text-decoration: none;
              color: white;
              font-weight: bold;
            }
          }
        }
   }
</style>