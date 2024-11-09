# 济宁市专业技术人员继续教育刷课脚本


## 脚本

学习网站：jnzjplat.chinahrt.cn,sdjn.yxlearning.com

脚本地址：[济宁市专业技术人员继续教育-刷课脚本][2]

## 教程

浏览器安装篡改猴插件后，打开[脚本安装地址][2]，进入后点击安装脚本，安装完成刷新你的学习网页就可以愉快使用了。

## 代学

注：如果需要代学，可以联系我微信yizhituziang或者QQ2422270452。

微信二维码：  
![微信二维码](https://www.tuziang.com/wx.jpg)

## 代码

关键代码分享：
```

  var course = document.getElementsByClassName("rightnav cursor-p")[0]
  var list = course.getElementsByTagName("li")
  var i
  setInterval(function () {
    for (i = 0; i < list.length; i++) {
      //定位当前课程
      if (list[i].className == "active" && list[i].innerText.indexOf("目录") == -1) {
        console.log(list[i].innerText)
        console.log(i)
        var current_course = i
      }
    }
    //当前课程播放完成
    if (list[current_course].innerText.indexOf("100%") != -1) {
      //防止点击章节名
      if (list[current_course + 1].innerText.indexOf("%") == -1) {
        list[current_course + 2].click()
      } else {
        list[current_course + 1].click()
      }
    }
  }, 2000)
```


  [1]: https://microsoftedge.microsoft.com/addons/detail/%E7%AF%A1%E6%94%B9%E7%8C%B4/iikmkjmpaadaobahmlepeloendndfphd?refid=bingshortanswersdownload
  [2]: https://greasyfork.org/zh-CN/scripts/403635-%E6%B5%8E%E5%AE%81%E5%B8%82%E4%B8%93%E4%B8%9A%E6%8A%80%E6%9C%AF%E4%BA%BA%E5%91%98%E7%BB%A7%E7%BB%AD%E6%95%99%E8%82%B2-%E5%88%B7%E8%AF%BE%E8%84%9A%E6%9C%AC
