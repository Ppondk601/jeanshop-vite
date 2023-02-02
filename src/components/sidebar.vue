<template>
    <div class="sidebar">
      <header class="header">
          <h1>LOGO</h1>
          
          <div class="sidebar-body">
              <div class="itemBar">
                  <div class="itemInbar">
                      <p>Shirts</p>
                  </div>
                  <div class="itemInbar">
                      <p>Dreses</p>
                  </div>
                  <div class="dropdown">
                      <dropdown class="Jeans" @click="clickForHide()">Jeans
                    <i class="fas fa-caret-down"></i></dropdown>
                      <sectionshow v-if="hideBar">
                          <div class="itemHide">
                              <p>Skinny</p>
                          </div>
                          <div class="itemHide">
                              <p>Relaxed</p>
                          </div>
                          <div class="itemHide">
                              <p>Bootcut</p>
                          </div>
                          <div class="itemHide">
                              <p>Straight</p>
                          </div>
                        </sectionshow>
                  </div>
                  <div class="itemInbar">
                      <p>Jackets</p>
                  </div>
                  <div class="itemInbar">
                      <p>Gymwear</p>
                  </div>
                  <div class="itemInbar">
                      <p>Blazers</p>
                  </div>
                  <div class="itemInbar">
                      <p>Shoes</p>
                  </div>
              </div>
          </div>
          
          <div class="itemFooter">
            <div class="itemInbar">
                <p>Contact</p>
            </div>
            <div class="itemInbar">
                <p>Newsletter</p>
            </div>
            <div class="itemInbar">
                <p>Subscribe</p>
            </div>
          </div>
      </header>
      </div>
  </template>

<script>
    export default {
        data(){
            return {
                hideBar:true
            }
        },
        methods:{
            clickForHide(){
                this.hideBar = !this.hideBar
            }
        }
        
    }
</script>

<style lang="scss" scoped>

    .sidebar{
        display:flex;
        flex-direction: column;
        width:100%;
        align-items: center;
        position:sticky;
        top:0;
        height:700px;
        overflow-y: scroll;
        overflow-x:hidden;

        .header{
            h1{
                font-size:25px;
                font-weight:600;
                padding:35px;
            }
            .sidebar-body{
                display:flex;
                flex-direction:column;
                .itemBar{
                    display:flex;
                    flex-direction:column;
                    padding-top:50px;
                    .itemInbar{
                        padding:10px 30px 10px 10px;
                        width:140%;
                        margin-left:30px;
                        font-size:18px;
                        color:rgb(105, 105, 105);
                        font-weight:600;
                    }
                    .itemInbar:hover {
                        background-color:#bbb;
                        color:black;
                    }
                }
                .dropdown{
                    display: flex;
                    flex-direction:column;
                    .Jeans{
                        padding:10px 30px 10px 10px;
                        width:140%;
                        margin-left:30px;
                        font-size:18px;
                        font-weight:600;
                    }
                    .Jeans:hover{
                        background-color:#bbb;
                        color:black;
                    }
                    .itemHide{
                        padding:10px 30px 10px 10px;
                        width:130%;
                        margin-left:50px;
                        font-size:16px;
                        font-weight:600;
                        color:rgb(105, 105, 105);
                    }
                    .itemHide:hover{
                        background-color:#bbb;
                        color:black;
                    }

                    
                }
            }
            .itemFooter{
                display:flex;
                flex-direction:column;
                padding-top:50px;
                .itemInbar{
                    padding:10px 30px 10px 10px;
                    margin-right:-135px;
                    margin-left:30px;
                    font-size:16px;
                    color:black;
                }
            }
        }
        
    }
</style>