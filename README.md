# baidu-searchData
仿百度搜索数据
主要为学习 vue 通过引入 vue-resource.js 进行数据绑定 三种方式：

     get ：例：获取一个普通文本数据
               this.$http.get('aa.txt').then( function( res ) {
                         console.log(res.data) ;
               },function( res）｛
                                        console.log( res.status );
               });
           例：给服务器发送数据：
              this.$this.get( 'get.php' , { a:1 , b:2 }).then( function(res) {
                                      console.log(res.data); 
              }, function(res){
                                      console.log( res.status );
              }) ;
              
    post： 例：【 post 要加请求头】
               this.$http.post( 'post.php' ,{ a:1 , b:20 }, { emulateJSON:true } ).then ( function( res ) {
                                          alert( res.data );
              },function(res){
                                           alert(res.status);
              } );
              
    jsonP: 例：【查看网页接口 chrome下面可以直接点击控制台的 js 】
                http://sp0.baidu.com/5a1Fazu8AA54nxGko9WTAnF6hhy/su?wd=a&cb=jshow

                this.$http.jsonp('https://sp0.baidu.com/5a1Fazu8AA54nxGko9WTAnF6hhy/su？',{
                                              wd:' a '
                },{ jsonP: ' cb' }).then( function(res){   // cb就是callback
                                               alert(res.data.s);
                },function(res){
                                               alert( res.status ) ;
                });
