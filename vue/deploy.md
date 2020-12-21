### for go, use goframe
1. npm run build
2. cp disk/**** go_project/public
3. when vue router use history mode, edit main.go. hash mode is normal
> 参考 https://www.cnblogs.com/mafeng/p/7690748.html
> 由于启用了history模式，我直接在浏览里访问 http://www.xxx.com/hot/item/1 这样的url是又404了，为什么 我可以在首页通过点击进入 http://www.xxx.com/hot/item/1 这个页面，但是直接访问又不行呢
> 因为在history 模式下，只是动态的通过js 操作window.history 来改变有浏览器地址栏里的路径，并没有发起http请求，但当你直接 在浏览器里输入这个地址的时候 就一定要先对服务器放起http请求，但是这个目标在服务器上又不存在所以就返回了404了，怎么解决呢，就是把所有的请求全部转发到http://www.xxx.com/hot/index.hmtl上就可以了
> 以下 goframe 形式
    > s := g.Server()
    >	s.SetRewriteMap(g.MapStrStr{
    >		"/admin/login": "/index.html",
    >	})
    >	s.Run()
