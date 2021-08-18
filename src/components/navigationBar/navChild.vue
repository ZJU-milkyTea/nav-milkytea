<template>
    <!-- top 没啥意义， 后面改名字  这个组件就是最子的组件了 -->
    <div>
        <!-- 第一行 ----------------------------------------------------------------------------->
        <el-row :gutter="5">
            <el-col :span="8">
                <div class="container-top">
                    <p class="container-p"> {{ namelist[0].title }} </p>
                    <el-row :gutter="5">
                        <el-col :span="8"  v-for="(item,index) in namelist[0].NavItem" :key="index">
                            <div class="grid-content bg-purple"  @click=clickNavChild(item)>
                                <div>
                                    <img :src= "item.picPath" >
                                    <p>{{item.nameNav}}</p>
                                </div>
                            </div>
                        </el-col>
                    </el-row>
                </div>
            </el-col>

            <el-col :span="8">
                <div class="container-top">
                    <p class="container-p"> {{ namelist[1].title }} </p>
                    <el-row :gutter="5">
                        <el-col :span="8"  v-for="(item,index) in namelist[1].NavItem" :key="index">
                            <div class="grid-content bg-purple"  @click=clickNavChild(item)>
                                <div>
                                    <img :src= "item.picPath" >
                                    <p>{{item.nameNav}}</p>
                                </div>
                            </div>
                        </el-col>
                    </el-row>
                </div>
            </el-col>

            <el-col :span="8">
                <div class="container-top">
                    <p class="container-p"> {{ namelist[2].title }} </p>
                    <el-row :gutter="5">
                        <el-col :span="8"  v-for="(item,index) in namelist[2].NavItem" :key="index">
                            <div class="grid-content bg-purple"  @click=clickNavChild(item)>
                                <div>
                                    <img :src= "item.picPath" >
                                    <p>{{item.nameNav}}</p>
                                </div>
                            </div>
                        </el-col>
                    </el-row>
                </div>
            </el-col>
        </el-row>

        <!-- 第二行 ----------------------------------------------------------------------------->
        <el-row :gutter="5">
            <el-col :span="8">
                <div class="container-top">
                    <p class="container-p"> {{ namelist[3].title }} </p>
                    <el-row :gutter="5">
                        <el-col :span="8"  v-for="(item,index) in namelist[3].NavItem" :key="index">
                            <div class="grid-content bg-purple"  @click=clickNavChild(item)>
                                <div>
                                    <img :src= "item.picPath" >
                                    <p>{{item.nameNav}}</p>
                                </div>
                            </div>
                        </el-col>
                    </el-row>
                </div>
            </el-col>

            <el-col :span="8">
                <div class="container-top">
                    <p class="container-p"> {{ namelist[1].title }} </p>
                    <el-row :gutter="5">
                        <el-col :span="8"  v-for="(item,index) in namelist[1].NavItem" :key="index">
                            <div class="grid-content bg-purple"  @click=clickNavChild(item)>
                                <div>
                                    <img :src= "item.picPath" >
                                    <p>{{item.nameNav}}</p>
                                </div>
                            </div>
                        </el-col>
                    </el-row>
                </div>
            </el-col>

            <el-col :span="8">
                <div class="container-top">
                    <p class="container-p"> {{ namelist[2].title }} </p>
                    <el-row :gutter="5">
                        <el-col :span="8"  v-for="(item,index) in namelist[2].NavItem" :key="index">
                            <div class="grid-content bg-purple"  @click=clickNavChild(item)>
                                <div>
                                    <img :src= "item.picPath" >
                                    <p>{{item.nameNav}}</p>
                                </div>
                            </div>
                        </el-col>
                    </el-row>
                </div>
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
                title: '农大 · 常用',
                numberLink:5,
                NavItem: [
                    {nameNav: '农大官网', jumpPath: 'https://www.fafu.edu.cn', picPath: require('@/assets/ima/fafu_logo.png')},
                    {nameNav: '计信院官网', jumpPath: 'https://xxxy.fafu.edu.cn/', picPath: require('@/assets/ima/fafu_logo.png')},
                    {nameNav: '教务处', jumpPath: 'https://jwc.fafu.edu.cn', picPath: require('@/assets/ima/fafu_logo.png')},
                    {nameNav: '教务管理系统', jumpPath: 'ttps://jwgl.fafu.edu.cn', picPath: require('@/assets/ima/fafu_logo.png')},
                    {nameNav: '网上办事大厅', jumpPath: 'https://app.fafu.edu.cn', picPath: require('@/assets/ima/fafu_logo.png')},
                    {nameNav: '网络教学平台', jumpPath: 'https://jxpt.fafu.edu.cn', picPath: require('@/assets/ima/fafu_logo.png')},
                    {nameNav: '信息公开网', jumpPath: 'https://xxgk.fafu.edu.cn/', picPath: require('@/assets/ima/fafu_logo.png')},
                    {nameNav: '后勤管理处', jumpPath: 'http://hq.fafu.edu.cn/', picPath: require('@/assets/ima/fafu_logo.png')},
                    {nameNav: '校医院', jumpPath: 'http://hq.fafu.edu.cn/', picPath: require('@/assets/ima/fafu_logo.png')},
                ]
            },{
                id: 2,
                title: '刷题 OJ',
                numberLink:5,
                NavItem: [
                    {nameNav: '牛客竞赛', jumpPath: 'https://ac.nowcoder.com/acm/contest/vip-index', picPath: require('@/assets/ima/newcoder.png')},
                    {nameNav: 'AcWing', jumpPath: 'https://www.acwing.com/problem/', picPath: require('@/assets/ima/AcWing.png')},
                    {nameNav: 'POJ（北大）', jumpPath: 'http://poj.org/', picPath: require('@/assets/ima/POJ.png')},
                    {nameNav: 'HDU（杭电）', jumpPath: 'https://acm.hdu.edu.cn/', picPath: require('@/assets/ima/HDU.png')},
                    {nameNav: 'ZOJ（浙大）', jumpPath: 'https://zoj.pintia.cn/home', picPath: require('@/assets/ima/ZOJ.png')},
                    {nameNav: 'PAT', jumpPath: 'https://pintia.cn/', picPath: require('@/assets/ima/PAT.png')},
                    {nameNav: '洛谷', jumpPath: 'https://www.luogu.com.cn/problem/list', picPath: require('@/assets/ima/luogu.png')},
                    {nameNav: 'LeetCode', jumpPath: 'https://leetcode-cn.com/', picPath: require('@/assets/ima/leetcode.png')},
                    {nameNav: '蓝桥杯', jumpPath: 'http://lx.lanqiao.cn/', picPath: require('@/assets/ima/lanqiao.png')},
                ]
            },{
                id: 3,
                title: '效率 · 工具',
                numberLink:5,
                NavItem: [
                    {nameNav: '百度翻译', jumpPath: 'https://fanyi.baidu.com/?aldtype=16047#auto/zh', picPath: require('@/assets/ima/baidufanyi.png')},
                    {nameNav: 'PDF编辑', jumpPath: 'https://lightpdf.com/zh/', picPath: require('@/assets/ima/pdf_online.png')},
                    {nameNav: '文本对比', jumpPath: 'https://www.jq22.com/textDifference', picPath: require('@/assets/ima/text_compare.png')},
                    {nameNav: 'QQ邮箱', jumpPath: 'https://mail.qq.com/', picPath: require('@/assets/ima/qqMail.png')},
                    {nameNav: '格式转换', jumpPath: 'https://convertio.co/zh/', picPath: require('@/assets/ima/formatTrans.png')},
                    // {nameNav: '', jumpPath: '', picPath: require('@/assets/ima/.png')},
                    // {nameNav: '', jumpPath: '', picPath: require('@/assets/ima/.png')},
                    // {nameNav: '', jumpPath: '', picPath: require('@/assets/ima/.png')},
                    // {nameNav: '', jumpPath: '', picPath: require('@/assets/ima/.png')},
                ]
            },{
                id: 4,
                title: '学习资源',
                numberLink:5,
                NavItem: [
                    {nameNav: '菜鸟教程', jumpPath: 'https://www.runoob.com/', picPath: require('@/assets/ima/cainiao.png')},
                    {nameNav: 'GitHub', jumpPath: 'https://github.com/', picPath: require('@/assets/ima/github.png')},
                    {nameNav: '知乎', jumpPath: 'https://www.zhihu.com/explore', picPath: require('@/assets/ima/zhihu.png')},
                    {nameNav: 'W3school', jumpPath: 'https://www.w3school.com.cn/', picPath: require('@/assets/ima/w3school.png')},
                    {nameNav: 'MOOC', jumpPath: 'https://www.icourse163.org/', picPath: require('@/assets/ima/MOOC.png')},
                    {nameNav: '网易公开课', jumpPath: 'https://open.163.com/', picPath: require('@/assets/ima/wangyi_course.png')},
                    // {nameNav: '', jumpPath: '', picPath: require('@/assets/ima/.png')},
                    // {nameNav: '', jumpPath: '', picPath: require('@/assets/ima/.png')},
                    // {nameNav: '', jumpPath: '', picPath: require('@/assets/ima/.png')},
                ]
            }]  
        }
    },
    methods:{
        clickNavChild: function(item){
            window.open(item.jumpPath);
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
    transition: 0.2s linear;    /* hover 蓝色背景动画 0.2s */
}

.grid-content div {
    transition: all 0.1s linear;   /*  hover 字体放大动画 0.1s  */
}

.grid-content img{
    max-width: 22px;
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
    /* width: 30%;
    height: 230px; */
    /* background-color:sandybrown; */
    background-color: rgb(242, 242, 242);
    float: left;
    /* margin-left: 50px;
    margin-top: 50px; */
}
.container-p {
    padding-left: 20px;
    color:rgb(128, 128, 128);
    font-family:'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-size: 20px;
    line-height: 20px;
}

</style>
