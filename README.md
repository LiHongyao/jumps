<!--
 * @Author: Lee
 * @Date: 2022-11-01 16:53:45
 * @LastEditors: Lee
 * @LastEditTime: 2022-11-01 16:55:04
 * @Description: 
-->
# 跳转至QQ指定联系人


```js
function jumpTencentContactWith(qqNum) {
  var jumpToComputer = `http://wpa.qq.com/msgrd?v=3&uin=${qqNum}&site=qq&menu=yes`;
  var jumpToMobile = `mqqwpa://im/chat?chat_type=wpa&uin=${qqNum}&version=1&src_type=web`;
  if (/Mobile/i.test(navigator.userAgent)) {
    /** 如果是手机,跳转到 */
    window.location.href = jumpToMobile;
  } else {
    /** 如果是电脑跳转到 */
    window.location.href = jumpToComputer;
  }
}
```