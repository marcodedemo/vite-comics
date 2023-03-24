
<script>
  export default{
    data(){
      return{

        linkLists:[
            {

                title: "dc comics",
                links:[
                    "Charaters",
                    "Comics",
                    "Movies",
                    "TV",
                    "Games",
                    "Videos",
                    "News"
                ]
            },
            {

                title: "shop",
                links:[
                    "Shop DC",
                    "Shop DC Collectibles",
                    
                ]
            
            },
            {
                title:"DC",
                links:[
                    "Terms Of Use",
                    "Privacy policy(New)",
                    "Ad Choises",
                    "Advertising",
                    "Jobs",
                    "Subscriptions",
                    "Talent Workshops",
                    "CPSC Certificates",
                    "Ratings",
                    "Show Help",
                    "Contact Us",


                ]
            },
            {
                title:"Sites",
                links:[
                    "DC",
                    "MAD Magazine",
                    "DC Kids",
                    "DC Universe",
                    "DC Power Visa",
                ]
            }
        ]

      }
    },
    
  }

</script>

<template>
  <footer>

      
      <div id="footer-top">
            <div class="container-centered">

                <div id="footer-links">

                    
                    <div class="footer-link-list" v-for="linkList in linkLists">
                        
                        <strong>{{ linkList.title }}</strong>
                        
                        <ul>
                            <li v-for="link in linkList.links">{{ link }}</li>
                        </ul>
                        
                        
                    </div>
                    
                </div>
            </div>
        </div>
        
        <div id="footer-bottom">

            <div class="container-centered">

                
                <div id="sign-up">
                    <button>Sign-Up Now!</button>
                </div>
                
                <div id="follow">
                    <span>Follow Us</span>

                    <div id="icons">

                        <div><img src="/public/img/footer-facebook.png" alt="facebook-logo"></div>
                        <div><img src="/public/img/footer-twitter.png" alt="twitter-logo"></div>
                        <div><img src="/public/img/footer-youtube.png" alt="youtube-logo"></div>
                        <div><img src="/public/img/footer-pinterest.png" alt="pinterest-logo"></div>
                        <div><img src="/public/img/footer-periscope.png" alt="periscope-logo"></div>
                        
                    </div>



                </div>

            </div>

        </div>

        
  </footer>
</template>

<style lang="scss" scoped>

footer{
    background-color: #303030;

    
    #footer-top{

        background-image: url("public/img/footer-bg.jpg");
        background-repeat:no-repeat;
        background-size:cover;




        // background-image: url("/public/img/dc-logo-bg.png");


        .container-centered{

            background-image: url("/public/img/dc-logo-bg.png");
            background-repeat: no-repeat;
            background-position-x:right ;

            max-width: 1200px;
            margin-left: auto;
            margin-right: auto;
            
            padding: 60px;
            
            #footer-links{
                
                display: flex;
                flex-direction: column;
                flex-wrap: wrap;
                
                height: 400px;
                width: 500px;

                .footer-link-list{
                    
                    padding: 10px 0;
                    
                    
                    strong{
                        color: white;
                        font-size: 1.2em;
                        text-transform: uppercase;
                    }
                    
                    li{
                        color: gray;
                    }
                }
            }
        }
    }

    #footer-bottom{

        .container-centered{
            display: flex;
            justify-content: space-between;


            max-width: 1200px;
            margin-left: auto;
            margin-right: auto;

            padding: 60px 0;
            
            #sign-up{
                button{
                    text-transform: uppercase;
                    font-weight: bold;
                    
                    color: white;
                    border: 2px solid #0582f9;
                    background-color: transparent;
                    
                    padding: 20px;
                }
            }
            
            #follow{
                display: flex;
                gap: 20px;
                
                span{
                    text-transform: uppercase;
                    font-weight: bold;
                    font-size: 1.4em;
                    
                    color: #0582f9;
                }

                #icons{
                    display: flex;
                    gap: 15px;

                }
            }
        }
    }
}
    
</style>