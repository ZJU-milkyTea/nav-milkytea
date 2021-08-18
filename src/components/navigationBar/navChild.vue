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
                            <div>
                                <img :src= "namelist[message].picPath[index]" >
                                <p>{{namelist[message].nameNav[index]}}</p>
                            </div>
                        </div>
                    </el-col>
                </el-row>
            </el-col>

            <el-col :span="8">
                <el-row :gutter="5">
                    <el-col :span="8"  v-for="(item,index) in namelist[message].nameNav" :key="index">
                        <div class="grid-content bg-purple"  @click=clickNavChild(message,index)>
                            <div>
                                <img :src= "namelist[message].picPath[index]" >
                                <p>{{namelist[message].nameNav[index]}}</p>
                            </div>
                        </div>
                    </el-col>
                </el-row>
            </el-col>

            <el-col :span="8">
                <el-row :gutter="5">
                    <el-col :span="8"  v-for="(item,index) in namelist[message].nameNav" :key="index">
                        <div class="grid-content bg-purple"  @click=clickNavChild(message,index)>
                            <div>
                                <img :src= "namelist[message].picPath[index]" >
                                <p>{{namelist[message].nameNav[index]}}</p>
                            </div>
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
    /* background: #d3dce6; */
    background: white;
}

.bg-purple-light {
    background: #e5e9f2;
}

.grid-content {
    margin-bottom: 5px;
    border-radius: 3px;
    min-height: 36px;
    text-align: center;
    color:rgb(128, 128, 128);
}

.grid-content div {
    transition: all 0.3s;
}

.grid-content img{
    max-width: 25px;
    vertical-align: middle; /* 对齐 */
}

.grid-content:hover > div{ /* 设置 hover 在 div 子元素上的作用 */
    transform: scale(1.1);
    font-weight: bold;
}

.grid-content:hover{
    background-color: rgb(69, 157, 245);
    color: white;
    cursor: pointer;
}

.grid-content p {
    font-family:'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin-left: 5px;
    font-size: 15px;
    line-height: 15px;
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
