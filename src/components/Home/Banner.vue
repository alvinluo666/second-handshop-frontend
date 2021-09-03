<template>
  <div class="banner">
      <div class="container">
            <div class="category">
                <div class="box">
                    <img src="@/assets/img/table-report.png" alt="">
                    <h2>မိုလ်ဘိုင်းဖုန်း</h2>
                </div>
                <div class="box">
                    <img src="@/assets/img/iphone.png" alt="">
                    <h2>တက်ပလက်</h2>
                </div>
                <div class="box">
                    <img src="@/assets/img/table-report.png" alt="">
                    <h2>မိုလ်ဘိုင်းဖုန်း</h2>
                </div>
                <div class="box">
                    <img src="@/assets/img/iphone.png" alt="">
                    <h2>တက်ပလက်</h2>
                </div>
                <div class="box">
                    <img src="@/assets/img/table-report.png" alt="">
                    <h2>မိုလ်ဘိုင်းဖုန်း</h2>
                </div>
                <div class="box">
                    <img src="@/assets/img/iphone.png" alt="">
                    <h2>တက်ပလက်</h2>
                </div>
                 <div class="box">
                    <img src="@/assets/img/iphone.png" alt="">
                    <h2>တက်ပလက်</h2>
                </div>
                <div class="box" @click="toAllPage()">
                    <img src="@/assets/img/more.png" alt="">
                    <h2>နောက်ထက်</h2>
                </div>
            </div>
            <div class="carousel">
                <el-carousel trigger="click" height="400px">
                    <el-carousel-item>
                        <img src="@/assets/img/banner/banner1.jpg" alt="" srcset="">
                    </el-carousel-item>
                    <el-carousel-item>
                        <img src="@/assets/img/banner/banner2.jpg" alt="" srcset="">
                    </el-carousel-item>
                    <el-carousel-item>
                        <img src="@/assets/img/banner/banner3.jpg" alt="" srcset="">
                    </el-carousel-item>
                </el-carousel>
            </div>
      </div>
  </div>
</template>

<script>
export default {
    methods:{
        toAllPage(){
            this.$router.push('/all')
        }
    }
}
</script>

<style lang="scss">
@import '../../assets/scss/constant.scss';
    .banner{
        margin:20px 0px;
        .container{
            @include container;
            background:red;
            height:400px;
            display:grid;
            grid-template-columns: 1fr 5fr;
            .category{
                background:white;
                height:400px;
                display: grid;
                grid-template-columns: 85px 85px;
                grid-template-rows: 85px 85px;
                padding:10px 0px 10px 10px;
                row-gap: 10px;
                column-gap: 10px;
                .box{
                    background:rgb(247, 247, 247);
                    width:85px;
                    height:85px;
                    display: flex;
                    flex-direction: column;
                    align-items: center;
                    justify-content: center;
                    border-radius: 5px;
                    transition:0.3s all;
                    border:2px solid white;
                    cursor:pointer;
                    img{
                        width:30px;
                        height:30px;
                    }
                    h2{
                        padding-top:12px;
                        font-size: 10px;
                    }
                    &:hover{
                        border:2px solid $brand-color;
                        
                    }
                }
            }
            .carousel{
                height:100%;
                background:white;
                img{
                    width:100% !important;
                }
            }
        }
    }
</style>