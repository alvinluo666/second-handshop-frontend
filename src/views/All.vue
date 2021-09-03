<template>
  <div class="all">
      <div class="container">
            <div class="category-board skeleton">               
                    <el-skeleton animated :loading="rootCategory.length==0">
                        <template slot="template">
                            <div class="box " >
                                <div class="title">
                                    <el-skeleton-item  variant="text" style="margin-right: 16px;width:100px;margin-bottom:10px" />
                                </div>
                                <div class="children">
                                    <el-skeleton-item v-for="i in 10" :key="i" variant="text" style="margin-right: 16px;width:100px;margin-bottom:10px" />
                                </div>
                            </div>
                            <div class="box " >
                                <div class="title">
                                    <el-skeleton-item  variant="text" style="margin-right: 16px;width:100px;margin-bottom:10px" />
                                </div>
                                <div class="children">
                                    <el-skeleton-item  v-for="i in 5" :key="i" variant="text" style="margin-right: 16px;width:100px;margin-bottom:10px" />
                                </div>
                            </div>
                            <div class="box " >
                                <div class="title">
                                    <el-skeleton-item  variant="text" style="margin-right: 16px;width:100px;margin-bottom:10px" />
                                </div>
                                <div class="children">
                                    <el-skeleton-item  v-for="i in 7" :key="i" variant="text" style="margin-right: 16px;width:100px;margin-bottom:10px" />
                                </div>
                            </div>
                        </template>
                    </el-skeleton>
                    
                </div>
                
            </div>
      </div>
  </div>
</template>

<script>
export default {
    data(){
        return {
            rootCategory : [],
        }
    },
    mounted(){
        this.loadCategory();
    },
    methods:{
        loadCategory(){
            this.axios.get(api.getRootCategory).then((res)=>{
                if(res.data.data.items){
                    this.rootCategory = res.data.data.items
                }
            }).catch((e)=>{
                this.$message.error('အမျိုးအစားရယူမှု မအောင်မြင်ပါ');
            })
        }
    }
}
</script>

<style lang="scss">
    @import '../assets/scss/constant.scss';
    .all{
        .container{
            @include container;  
                
            .category-board{
                margin-top:20px;
                padding:20px;
                background: white;   
                width:100%;
                min-height: 148px;
                .box{
                    display:Flex;
                    .title{
                        margin-right:50px;        
                    }
                    .children{
                        text-align: left;
                    }
                }
            }
        }
    }
</style>