<template>
    <!-- top 没啥意义， 后面改名字  这个组件就是最子的组件了 -->
    <div class="container-top">
        <div class="nav-content" v-for="(item,index) in namelist[message].nameNav" :key="index">
            <img :src= "namelist[message].picPath[index]" >
            <p>{{namelist[message].nameNav[index]}}</p>
        </div>
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
                id: 2,
                title: '竞赛'
            }],
            linkList:[{
                
            }]
        }
    },
    props:['message']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container-top{
    width: 30%;
    height: 230px;
    background-color:sandybrown;
    float: left;
    margin-left: 50px;
    margin-top: 50px;
}

.nav-content{
    width: 30%;
    height: 40px;
    margin: 0 auto;
    float: left;
    background-color: #fff;
    margin-left: 10px;
    margin-top: 10px;
} 

.nav-content:hover{
    background-color: blue;
    cursor: pointer;
}

.nav-content img{
    margin-top: 7px;
    max-width: 25px;
}

.nav-content span{
    font-size: 20px;
    font-weight: bold;
    text-align: center;
    vertical-align:6px;
}



</style>
