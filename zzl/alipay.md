# 支付宝

## 一面(电话面试)

- 自我介绍，根据项目问细节
- 无头浏览器如何爬取移动端首屏，hybrid应用开发经验问题
- react生命周期，hook模拟didComponentMount
- es6都有什么新语法，箭头函数和function区别
- function bind，apply，call区别，连续两次bind，call的时候上下文
- babel怎么配置语法向前兼容，preset-env，babel/polyfill，配置和使用
- 怎么实现跨域请求，怎么带cookie
- script标签，defer和async区别
- css盒子模型
- 页面body下只有一个div，div空的paddingTop: 100%; 问页面是什么样子。
- 问问题



## 二面(coding)

- 实现一个useDelayRender

  ```js
  function useDelayRender(Comp, delay) {
    // code
  }
  
  // test
  function myComponent() {
    return 'xxxx';
  }
  
  function wrapperComponent() {
    const [component] = useDelayRender(myComponent, 3000);
    
    return component;
  }
    
  ```

  

- asyncAjaxGet try...catch...捕获

  ```JS
  try {
    asyncAjaxGet(url, (response) => {
      response.data.children = 1; // 可能有异常，期望被扑火
    });
  } catch(e) {
    // ....
  }
  ```

  

- 实现一个arrange函数

  ```js
  /**
   * --- 问题描述 ---
   *
   * 实现一个 arrange 函数，可以进行时间和工作调度
   * 注意，这里的 wait do 均可以无限调用
   *
   * --- 说明 ---
   *
   * - 具体功能参考下列示例
   * - 在示例中调用到的方法都需要实现
   * - 下面示例中 `>` 表示在控制台中输出 (console.log)
   *
   * --- 示例 ---
   *
   * 示例一:
   * `arrange('William').execute();`
   * > William is notified
   *
   * 示例二:
   * `arrange('William').wait(5).do('commit').wait(5).do('push').execute();`
   * > William is notified
   * 等待 5s...
   * > Start to commit
   * 等待 5s
   * > Start to push
   */
  const arrage = (name) => {
    class TaskaArrange {}
    return new TaskaArrange(name);
  }
  ```

- retryAjax 实现

  ```js
  function retryAjax(url，{onSuccess, onFail, maxRetryTimes}) {
      
  }
  ```

  

- 前端安全xss攻击

  ```js
  //   前端安全
  // • 以下方法存在安全漏洞，请对其进行攻击，执行 alert(1);
  // • 如何解决这个漏洞？
  // url:  http://sample.com/?url=http%3A%2F%2FsampleImage
  var search = querySearch(locaiton.href);
  var content = '<img src="' + search.url + '"/>';
  document.getElementById('J_Container').innerHTML = content;
  ```

- 继续讲项目

