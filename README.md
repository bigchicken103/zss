1.交互逻辑
当进入app 首先显示启动页，在展示启动页的同时请求接口获取配置数据，请求接口时会有一个loading ui。
如果接口请求失败或者没有拿到正确的数据，就一直卡在loading。
如果接口请求成功，判断是否是A面或者B面。当是B面的时候打开接口中的地址页面。

2.接口数据结构 接口地址https://raw.githubusercontent.com/bigchicken103/app/refs/heads/master/v30/p.json（接口可能会有缓存，注意清理）
{
"0":"https://wa.me,upi://,upi://",
"1":"https://www.baidu.com", 
"2":"0"
}
Key 0，外跳链接url前缀，以逗号分隔，当匹配到UIR时 ，跳转到safari浏览器
Key 1 ，页面地址 
Key 2，马甲包标识，0 A面 1 B面

3.需求
一 .接口中获取外跳，默认浏览器url 前缀
二 .需要支持图片权限
三 启动页 停留时间稍微长一点 2s左右
四 包大小，加入字体文件，调大一些（10M左右）
五webview在加载页面的时 有进度条
APP 名字 ：華和Tw