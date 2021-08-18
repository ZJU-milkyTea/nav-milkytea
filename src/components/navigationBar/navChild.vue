<template>
    <!-- top 没啥意义， 后面改名字  这个组件就是最子的组件了 -->
    <!-- <div class="container-top">
        <p>{{namelist[message].title}}</p>
        <div class="nav-content" v-for="(item,index) in namelist[message].nameNav" :key="index" @click=clickNavChild(message,index)>
            <img :src= "namelist[message].picPath[index]" >
            <p>{{namelist[message].nameNav[index]}}</p>
        </div>
    </div> -->
    <div>
        <el-row :gutter="10">
            <el-col :span="8">
                <el-row :gutter="5">
                    <el-col :span="8"  v-for="(item,index) in namelist[message].nameNav" :key="index">
                        <div class="grid-content bg-purple"  @click=clickNavChild(message,index)>
                            <img :src= "namelist[message].picPath[index]" >
                            <p>{{namelist[message].nameNav[index]}}</p>
                        </div>
                    </el-col>
                </el-row>
            </el-col>

            <el-col :span="8">
                <el-row :gutter="5">
                    <el-col :span="8"  v-for="(item,index) in namelist[message].nameNav" :key="index">
                        <div class="grid-content bg-purple"  @click=clickNavChild(message,index)>
                            <img :src= "namelist[message].picPath[index]" >
                            <p>{{namelist[message].nameNav[index]}}</p>
                        </div>
                    </el-col>
                </el-row>
            </el-col>

            <el-col :span="8">
                <el-row :gutter="5">
                    <el-col :span="8"  v-for="(item,index) in namelist[message].nameNav" :key="index">
                        <div class="grid-content bg-purple"  @click=clickNavChild(message,index)>
                            <img :src= "namelist[message].picPath[index]" >
                            <p>{{namelist[message].nameNav[index]}}</p>
                        </div>
                    </el-col>
                </el-row>
            </el-col>
        </el-row>
        
    </div>
</template>

<script>
export default {
    data() {
        return{
            namelist:[{
                id: 1,
                title: '学术，科研',
                numberLink:5,
                nameNav:[
                    'cc98',
                    'fafu',
                    'apple',
                    'xiaomi',
                    'alibaba',
                    'zju',
                    'csdn',
                    'infoQ',
                    'dji'
                ],
                jumpPath:[
                    'https://www.baidu.com',
                    'https://www.baidu.com',
                    'https://www.baidu.com',
                    'https://www.baidu.com',
                    'https://www.baidu.com',
                    'https://www.baidu.com',
                    'https://www.baidu.com',
                    'https://www.baidu.com',
                    'https://www.baidu.com',
                    'https://www.baidu.com'
                ],
                picPath:[
                    require('@/assets/ima/head1.png'),
                    require('@/assets/ima/head1.png'),
                    require('@/assets/ima/head1.png'),
                    require('@/assets/ima/head1.png'),
                    require('@/assets/ima/head1.png'),
                    require('@/assets/ima/head1.png'),
                    require('@/assets/ima/head1.png'),
                    require('@/assets/ima/head1.png'),
                    require('@/assets/ima/head1.png'),
                    require('@/assets/ima/head1.png'),
                ]
                
            },{
               
            },{
               


            }]  
        }
    },
    methods:{
        clickNavChild: function(mes,index){
            window.open(this.namelist[mes].jumpPath[index]);
        }
    },
    props:['message']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.el-row {
    padding-left: 10px;
    padding-right: 10px;
    /* &:last-child {
      margin-bottom: 0;
    } */
}

.el-col {
    border-radius: 2px;
}

.bg-purple-dark {
    background: #99a9bf;
}

.bg-purple {
    background: #d3dce6;
}

.bg-purple-light {
    background: #e5e9f2;
}

.grid-content {
    margin-bottom: 5px;
    border-radius: 2px;
    min-height: 36px;
    text-align: center;
}

.grid-content img{
    max-width: 25px;
    vertical-align: middle; /* 对齐 */
}

.grid-content:hover{
    background-color: rgb(104, 141, 245);
    color: white;
    cursor: pointer;
    font-size: 20px;
}

.grid-content p {
    margin-left: 5px;
    font-size: 15px;
    line-height: 15px;
    font-weight: bold;
    display: inline-block; /* 转换为行内元素才可对齐 */ 
}  

.row-bg {
    padding: 10px 0;
    background-color: #f9fafc;
}

.container-top{
    width: 30%;
    height: 230px;
    background-color:sandybrown;
    float: left;
    margin-left: 50px;
    margin-top: 50px;
}

</style>
