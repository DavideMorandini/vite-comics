<script>
  export default {
    data () {
      return {
        links: [
            "characters",
            "comics",
            "movies",
            "tv",
            "games",
            "collectibles",
            "videos",
            "fans",
            "news",
            "shop"
        ],
      }      
    },
    methods: {
        activateLink(event) {
            const links = document.querySelectorAll("#links")
            links.forEach((link) =>{
                link.classList.remove("active")
            })
            event.target.classList.add("active")
        }
    }
  }
</script>

<template>
    <header>
        <div class="container-centered">
            <div id="logo">
                <img @click="window.location.reload()" src="../../public/img /dc-logo.png" alt="logo">
            </div>

            <a href="#" id="links" @click="activateLink" v-for="link in links">
                {{ link }}
            </a>
        </div>
    </header>
</template>

<style lang="scss" scoped>
    header {
        height: 120px;
        background-color: #fff;
    
        .container-centered {
            padding-bottom: 0;
            padding-top: 0;
            
            #logo{
                flex-grow: 1;
                cursor: pointer;
            }

            #links {
                display: flex;
                align-items: center;
                height: 100%;          
                text-transform: uppercase;
                text-decoration: none;
                font-weight: bold;
                color: #464646;
                padding: 8px;
                padding-bottom: 0;
            }

            .active {
                border-bottom: 6px solid #0282f9;
                color: #0282f9;
            }
        }
    }
</style>