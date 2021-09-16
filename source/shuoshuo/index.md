---
comments: false
---
<!-- 引用 artitalk -->
<script type="text/javascript" src="https://unpkg.com/artitalk"></script>
<!-- 存放说说的容器 -->
<div id="artitalk_main"></div>
<script>
new Artitalk({
    appId: 't1Ws9VcwcfE6TTMLzktmB6yL-MdYXbMMI', 
    appKey: 'eQg3qrjLwEf92atm10A267As'
})
</script>
<script>
function reurl(){

url = location.href; //把当前页面的地址赋给变量 url

var times = url.split("?"); //分切变量 url 分隔符号为 "?"

if(times[1] != 1){ //如果?后的值不等于1表示没有刷新

url += "?1"; //把变量 url 的值加入 ?1

self.location.replace(url); //刷新页面

}
}

reurl();//执行这个函数
</script>
