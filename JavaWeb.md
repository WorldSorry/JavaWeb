Java Web
    Tomcat 修改端口
        conf文件下 server.xml
Spring mvc 框架
        前端控制器 DispatcherServlet 接口用户请求，相应
        处理映射器 HandlerMapping 返回执行链 HandlerExecutionChain{HandlerInterceptor1..}
        处理器适配器 HandlerAdapter 
        handler处理器 平常叫做 Controller  返回 ModelAndView 给前端控制器
        视图解析器 View resolver
        视图
             
            第一步：发起请求到前端控制器（DispatcherServlet）
            第二步：前端控制器请求HandlerMapping 查找Handler 可以根据xml配置、注解查找
            第三部：处理映射器HandlerMapping 向前端控制器返回Handler
            第四部：前端控制器调用处理适配器去执行Handler
            第五步：处理器去执行Handler
            第六步：Handler执行完成给适配器返回ModelAndView
            第七步：处理器适配器向前端返回ModelAndView，ModelAndView是SpringMVC框架的一个底层对象，包括Model和View
            地八步：前端控制器请求视图解析器去进行视图解析，根据逻辑视图名解析成真正的视图（jsp）
            第九步：视图解析器向前端控制器返回View
            第十步：前端控制器进行视图渲染，视图渲染将模型数据填充到request域
            第十一步：前端控制器向用户响应 

   组件
        