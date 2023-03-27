
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
        ],

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
                            <li v-for="link in linkList.links">
                                <a href="#">{{ link }}</a>
                            </li>
                        </ul>
                        
                        
                    </div>
                    
                </div>
            </div>
        </div>
        
        <div id="footer-bottom">

            <div class="container-centered">

                
                <div id="sign-up">
                    <button>
                       <a href="#">
                           Sign-Up Now!
                       </a> 
                    </button>
                </div>
                
                <div id="follow">
                    <span>Follow Us</span>

                    <div id="icons">

                        <div id="icons">

                        <div>
                            <a href="#">
                                <img src="/public/img/footer-facebook.png" alt="facebook-logo">
                            </a>
                        </div>

                        <div>
                            <a href="#">
                                <img src="/public/img/footer-twitter.png" alt="twitter-logo">
                            </a>
                        </div>

                        <div>
                            <a href="#">
                                <img src="/public/img/footer-youtube.png" alt="youtube-logo">
                            </a>
                        </div>

                        <div>
                            <a href="#">
                                <img src="/public/img/footer-pinterest.png" alt="pinterest-logo">
                            </a>
                        </div>

                        <div>
                            <a href="#">
                                <img src="/public/img/footer-periscope.png" alt="periscope-logo">
                            </a>
                        </div>

                        
                    </div>

                        
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

        padding: 0 20px;





        // background-image: url("/public/img/dc-logo-bg.png");


        .container-centered{

            background-image: url("/public/img/dc-logo-bg.png");
            background-repeat: no-repeat;
            background-position: center;
            background-position-x:right;

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
                    
                    li a{
                        color: gray;
                    }
                }
            }
        }
    }

    #footer-bottom{

        padding: 0 20px;

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
                    
                    border: 2px solid #0582f9;
                    background-color: transparent;
                    
                    padding: 20px;
                    
                    a{
                        color: white;
                        
                    }
                }
            }
            
            #follow{
                display: flex;
                gap: 20px;
                
                span{
                    flex-shrink: 0;
                    text-transform: uppercase;
                    font-weight: bold;
                    font-size: 1.4em;
                    
                    color: #0582f9;
                }

                #icons{
                    display: flex;
                    flex-wrap: wrap;
                    gap: 15px;

                }
            }
        }
    }
}

@media screen and (max-width:768px) {
  
    footer #footer-bottom .container-centered #follow span{
        display: none;
    }
}
    
</style>