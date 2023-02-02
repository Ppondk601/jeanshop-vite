<template>
    <div class="container">
        <div class="sectionHeader">
            <div class="image">
                <img src="https://www.w3schools.com/w3images/jeans.jpg" style="width=100%">
                <div class="text-content">
                    <h1>New arrivals</h1>
                    <h5>COLLECTION 2016</h5>
                    <div class="shop">
                        <button>SHOP NOW</button>
                    </div>
                </div>
            </div>
        </div>

        <div class="sectionBody">
            <h5>8 Items</h5>
            <div class="image-item">
                <div class="item-card" v-for="item in jeanLists" :key="item.id">
                    <div class="image-incard">
                    <img :src="item.image">
                    <button class="fas fa-cart-plus"></button>
                    </div>
                    <select v-model="selected">
                    <option v-for="item in jeanLists" :value="key" :key="item.id" >
                    {{item.id}} ตัว
                    </option>
                    </select>
                    <div class="text-incard">
                        <p>{{ item.name }}</p>
                        <span>{{ item.price }}</span>
                    </div>
                </div>
            </div>
        </div>

        <div class="sectionContact">
            <h3>Subscribe</h3>
            <span>To get special offers and VIP treatment:</span>
            <input type="text" placeholder="Enter e-mail">
            <div class="buttonContact">
            <button type="submit">Subscribe</button>
            </div>
        </div>

        <div class="sectionFooter">
            <div class="box-left">
                <h3>Contact</h3>
                <p>Questions? Go ahead.</p>
                <input type="text" placeholder="Name">
                <input type="text" placeholder="Email">
                <input type="text" placeholder="Subject">
                <input type="text" placeholder="Message">
                <button>Send</button>
            </div>

            <div class="box-middle">
                <h3>About</h3>
                <a href="https:/google.com">About us</a>
                <a href="https:/google.com">We're hiring</a>
                <a href="https:/google.com">Support</a>
                <a href="https:/google.com">Find store</a>
                <a href="https:/google.com">Shipment</a>
                <a href="https:/google.com">Payment</a>
                <a href="https:/google.com">Gift Card</a>
                <a href="https:/google.com">Return</a>
                <a href="https:/google.com">Help</a>
            </div>

            <div class="box-right">
                <h3>Store</h3>
                <i class="fas fa-location-dot">
                    <span>Company Name</span>
                </i>
                <i class="fas fa-phone">
                    <span>0044123123</span>
                </i>
                <i class="fas fa-envelope">
                    <span>ex@mail.com</span>
                </i>
                <p>We accpet</p>
                <i class="fas fa-wallet">
                    <span>Amex</span>
                </i>
                <i class="fas fa-credit-card">
                    <span>Credit Card</span>
                </i>
                
            </div>
        </div>



    </div>
</template>

<script>
    export default {
        data(){
            return{
                jeanLists: [
                    {
                     id:1,
                     name: "Ripped Skinny Jeans",
                     price: 24.99 ,
                     image:"https://www.w3schools.com/w3images/jeans1.jpg",
                     
                    },
                    {
                     id:2,
                     name: "Mega Ripped Jeans",
                     price: 19.99 ,
                     image:"https://www.w3schools.com/w3images/jeans2.jpg",
                     
                    },
                    {
                     id:3,
                     name: "Washed Skinny Jeans",
                     price: 20.50 ,
                     image:"https://www.w3schools.com/w3images/jeans3.jpg",
                     
                    },
                    {
                     id:4,
                     name: "Vintage Skinny Jeans",
                     price: 14.99 ,
                     image:"https://www.w3schools.com/w3images/jeans4.jpg",
                     
                    },
                    {
                     id:5,
                     name: "Mega Ripped Jeans",
                     price: 19.99 ,
                     image:"https://www.w3schools.com/w3images/jeans2.jpg",
                     
                    },

                    {
                     id:6,
                     name: "Washed Skinny Jeans",
                     price: 20.50 ,
                     image:"https://www.w3schools.com/w3images/jeans3.jpg",
                     
                    },
                    {
                     id:7,
                     name: "Vintage Skinny Jeans",
                     price: 14.99 ,
                     image:"https://www.w3schools.com/w3images/jeans4.jpg",
                     
                    },

                    {
                     id:8,
                     name: "Ripped Skinny Jeans",
                     price: 24.99 ,
                     image:"https://www.w3schools.com/w3images/jeans1.jpg",
                     
                    },
                ],
                cartItems: 
                [
                    {id:""},
                    {amount:""},
                ]
            }
        }
        
    }
</script>

<style lang="scss" scoped>
.container{
    display:flex;
    flex-direction:column;
    .sectionHeader{
        display:flex;
        flex-direction:column;
        padding:0px 15px 0px 15px;
        .image{
            display:flex;
            position:relative;
            .text-content{
                display:flex;
                flex-direction:column;
                position:absolute;
                .shop{
                    padding-top:20px;
                    button{
                        background-color:black;
                        color:white;
                        padding:15px 30px 15px 30px;
                        margin-left:30px;
                        font-size:18px;
                    }
                    button:hover{
                        background-color: #ccc;
                        color:black;
                        border:none;
                    }
                }
                h1{
                    color:white;
                    font-size:60px;
                    padding:30px;
                }
                h5{
                    color:white;
                    font-size:30px;
                    padding:0px 30px 0px;
                }
            }
            img{
                width:100%;
            }
        }
    }
    .sectionBody{
        display:flex;
        flex-direction: column;
        h5{
            padding:18px 0px 18px 0px;
            font-size:16px;
            text-decoration:none;
            font-weight: normal;
        }
        .image-item{
            display:grid;
            grid-template-columns: 25% 25% 25% 25%;
            grid-template-rows:auto;
            align-items: center;
            .item-card{
                display:flex;
                flex-direction: column;
                justify-content: center;
                padding:0px 15px 0px 15px;
                .image-incard{
                    display:flex;
                    flex-direction:column;
                    position:relative;
                    button{
                        position:absolute;
                        top:40%;
                        right:35%;
                        padding:10px 30px 10px 30px;
                        border:none;
                        
                    }
                }
                .text-incard{
                padding:15px 0px 10px 0px;
            }

            img{
                width:100%;
                opacity:90%;
                height:100%;
            }
            }
        }
    }

    .sectionContact{
        background-color: black;
        display:flex;
        padding:30px;
        flex-direction: column;
        justify-content: start;
        .buttonContact{
            padding:15px 0px 15px 0px;
            button{
                padding:10px 15px 10px 15px;
                background-color: #f44336;
                color:white;
            }
            button:hover{
                background-color: #ccc;
                color:black;
            }
        }
        h3{
            color:white;
            font-size:40px;
        }
        span{
            color:white;
            padding:20px 0px 20px 0px;
        }
        input{
            padding:10px;
        }

    }

    .sectionFooter{
        display:grid;
        grid-template-columns: 32% 32% 32%;
        background-color: #eee;
        padding:40px 0px 0px 0px;
        justify-content: center;
        .box-left{
            display:flex;
            flex-direction: column;
            padding:20px 20px 20px 0px;
            h3{
                align-self: center;
                padding-bottom:15px;
            }
            p{
                align-self: center;
                padding-bottom:10px;
            }
            input{
                padding:10px;
                margin:5px;
                border:1px solid #ccc
            }
            button{
                padding:7px;
                margin:5px;
                background-color: black;
                color:white;
            }
            button:hover{
                background-color: #ccc;
                color:black;
                border:none;
            }
        }

        .box-middle{
            display:flex;
            flex-direction:column;
            padding:20px;
            align-items: center;
            a{
                padding:6px 0px 6px 0px;
                color:black;
                opacity:80%;
            }
        }
        h3{
            padding-bottom:10px;
            font-size:20px;
        }
        .box-right{
            display:flex;
            flex-direction:column;
            padding:20px;
            p{
                padding:10px 0px 10px 0px;
                font-size:20px;
                font-weight:600;
            }
            i{
                padding:10px 0px 10px 0px;
                font-size:10px;
                span{
                    letter-spacing:2px;
                    padding:10px;
                }
            }
        }
    }
    
}
</style>