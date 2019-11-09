<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
import config from "./../config/config";
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: '正在登陆微博...'
    }
  },
	mounted() {
		debugger;
			function getUrlParam(name) {
			  var reg = new RegExp("(^|&)" + name + "=([^&]*)(&|$)");
			  var r = window.location.search.substr(1).match(reg);
			  console.log(r)
			  if (r != null) return unescape(r[2]);
			  return null;
			}
var customerId = getUrlParam("customerId")
var targetUrl = getUrlParam("targetUrl")
//				this.$ajax({
//					url: "http://test.begogirls.com/gogirl_web_store/gogirl_user/weiboLogin",
//					method: "get",
//					params:{
//						customerId:customerId,
//						targetUrl:targetUrl
//					}
//				}).then(res => {
//					  console.log(res)
//					  if(res.data.success ==true){
//					  	   window.location.href = res.data.data;
//					  }else{
//					  	  alert(res.data.message)
//					  }
//					 
//				});
//window.location.href = "https://api.weibo.com/oauth2/authorize?client_id=2734334547&redirect_uri=http://begogirls.com/gogirl_user/weiboInfo&response_type=code&state="+customerId+","+targetUrl+"&scope=all&with_offical_account=1";
window.location.href = "https://api.weibo.com/oauth2/authorize?client_id=356453014&redirect_uri=http://test.begogirls.com/gogirl_user/weiboInfo&response_type=code&state="+customerId+","+targetUrl+"&scope=all&with_offical_account=1";
	}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
