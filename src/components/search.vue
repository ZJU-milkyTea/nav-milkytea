<template>
    <div class="search-root">
        <!-- 添加搜索引擎对应图标 -->
        <!-- <el-image
            style="width: 90px; height: 50px; position: absolute; margin-left: -100px; margin-top: -5px"
            :src="require('@/assets/ima/fafu_logo.png')"
            fit="contain">
        </el-image> -->
		<el-input  placeholder="请输入内容" v-model="input" class="input-with-select" @keydown.enter.native="clickSearch()">	
            <el-select placeholder="请选择" v-model="select" slot="prepend" >
                <el-option label="百度" value="0"></el-option>
                <el-option label="搜狗" value="1"></el-option>
                <el-option label="360搜索" value="2"></el-option>
            </el-select>
            <el-button slot="append" icon="el-icon-search" @click="clickSearch()">

            </el-button>
        </el-input>
       
	</div>
</template>

<script>
export default {
    data: function(){
        return{
            input: '',
            select: '0',
            urlData:[{
                title:'baidu',
                url: 'https://www.baidu.com/s?ie=utf-8&f=8&rsv_bp=0&rsv_idx=1&tn=baidu&wd='
            },{
                title:'sougou',
                url: 'https://www.sogou.com/web?query='
            },{
                title:'360',
                url: 'https://www.so.com/s?ie=utf-8&shb=1&src=360sou_newhome&q='
            }]
        }
    },
    methods:{
        clickSearch: function(){
            window.open(this.urlData[this.select].url + this.input);
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.search-root{
	width: 30%;
	height: 100px;
	margin: 0 auto;
	margin-top: 50px;
}
.el-select{
    font-size: 20px;
}

.el-select .el-input {
    width: 150px;
}

.input-with-select .el-input-group__prepend {
    background-color: #fff;
}


</style>
