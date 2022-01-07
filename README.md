iframe父子传参通信


f为父文件，s为子文件


保证文档和资源加载完成两种方式： 1.readyState 2.onload
1. sonWindow.document.readyState === 'complete'
2. sonWindow.onload = function () {}


父获取子window
<iframe name ='iframeName' id = 'iframeId>
sonWindow == iframeName == document.getElementById('iframeId').contentWindow


子获取父window
window.parent