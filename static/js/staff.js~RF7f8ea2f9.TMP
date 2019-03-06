
var root = new Vue({
	el:".wrap",
	data:{
		list:[],
		judge:false
	},
	mounted(){
		axios.get("http://127.0.0.1:8080/getData",{

		}).then((response)=>{
			console.log(response.data);
			root.list = response.data
		})
	},
	methods:{
		delete1(id){
			this.$confirm("确定删除这条信息吗?","提示",{
				type:"error"
			}).then(()=>{
				axios.get("http://127.0.0.1:8080/deleteData",{
					params:{
						ID:id
					}
				}).then((response)=>{
						if(response.data=="success"){
							this.$message({
								type:"error",
								title:"警告",
								message:"删除成功"					
							});
						}
					})
				})
			
		},
		edit(){
			this.judge=true
		}
	}

})
