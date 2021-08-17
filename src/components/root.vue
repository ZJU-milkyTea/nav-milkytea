<template>
    <div>
		<header-com></header-com>
		<search-root></search-root>
		<nav-root></nav-root>
    </div>
</template>

<script type="text/javascript">
import header from './header.vue';
import searchRoot from './search.vue'
import navRoot from './navRoot.vue';

// import xxx from someSrc     es6中得到模块的方法。


export default {
    //注册组件
    components: {
        'header-com': header,
		'search-root':searchRoot,
		'nav-root': navRoot
    },
    data: function() {
        return {
        
        }
    },
    methods: {
        // &event是实参，表示event对象
        
    }
}
</script>

<style type="text/css">

.body{
	background-color: crimson;
}




</style>
