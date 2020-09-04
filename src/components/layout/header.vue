<template>
    <div class="header">
        <div class="title">
            <div class="titleName">智慧工地安全管理</div>
            <div class="sidebar">
                <!-- <el-menu
                class="sidebar-el-menu"
                
                mode="horizontal"
                :background-color="weiselectSty"
                text-color="#bfcbd9"
                :active-text-color="selectedSty"
                unique-opened
                
                >
                <template v-for="item in items">
                    <template >
                        <el-menu-item :index="item.index" :key="item.index">
                            
                            <span slot="title">{{ item.title }}</span>
                        </el-menu-item>
                    </template>
                </template>
                </el-menu> -->
                <div class="sidebar_left">
                    <div class="bg_juxing">项目概览</div>
                    <div class="bg_juxing">人员管理</div>
                    <div class="bg_juxing">安全管理</div>
                    <div class="bg_juxing">设备管理</div>
                    <div class="bg_juxing">视频管理</div>
                </div>
            </div>
        </div>
        
                
    </div>
</template>
<script>
   export default {
        
        data() {
            return {
                items: [
                    {
                    index: "index",
                    title: "项目概览"
                    },
                    {
                    index: "peopleManager",
                    title: "人员管理"
                    },
                    {
                    index: "safeManager",
                    title: "安全管理"
                    },
                    {
                    index: "deviceManager",
                    title: "设备管理"
                    },
                    {
                    index: "videoManager",
                    title: "视频管理"
                    },{
                    index: "greenSite",
                    title: "绿色施工"
                    },{
                    index: "produceManager",
                    title: "生产管理"
                    },{
                    index: "qualityManager",
                    title: "质量管理"
                    },{
                    index: "dataManager",
                    title: "资料管理"
                    },{
                    index: "enterSystem",
                    title: "进入后台"
                    }
                ]
            }
        },
        computed:{
            
        },
        methods:{
           
        },
        mounted(){

        }
            
    }

    
</script>
<style scoped>
    .header {
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 0;
        margin: 0;
        height: 0.69rem;
        background-image: url("../../assets/top_header.png");
        background-size: cover;
    }
    .title{

    }
    .titleName {
        
        font-size:0.38rem; 
        font-family: "MicrosoftYaHei";
        font-weight: bold;

    }
    .sidebar {
        display: flex;
        /* float: left; */
        
        justify-content: space-around;
    }
    .sidebar_left {
       display: flex;
       
        justify-content: space-around;
    }
    .bg_juxing {
        background-image: url("../../assets/xiaojuxing.png");
        height: 0.38rem;

    }
    .weiselectSty {
        background-image: url("../../assets/xiaojuxing.png")
    }
    .selectedSty {
        background-image: url("../../assets/xiaojuxing_selected.png")
    }


    
</style>
