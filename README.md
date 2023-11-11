# znabc_rime
使用rime配置的 纯净版 智能abc


自用的rime配置znabc智能ABC方案

2023年了,还是有很多人喜欢使用智能ABC输入法, 

我就是其中一位. 我的智能ABC可是盲打级别的哟...


不大懂使用github 那么直接在这里写攻略吧.

1, 下载官方的rime windows安装程序
https://rime.im/download/
安装时只选择全拼
![image](https://github.com/manuelding/znabc_rime/assets/73762031/881daec7-7558-491f-8679-bd2c1950e7fb)


2, 从github下载智能abc的语序.
可以直接使用附件

我是从下面来源下载,并做微小修改的:

https://github.com/ma-ning/znabc

通过【小狼毫】用户词典管理 添加字典, 因为我只用小狼毫打智能ABC, 所以我去安装目录里把其他多余的用户字典删除了.

是否保留其他用户字典请自己评估.

%appdata%/rime 里有个xxxxx.userdb 的是用户字典, 其他的我全删了.


3,只在default.custom.yaml的patch下添加了键盘设置,其他全部没动.

```
patch:
  ascii_composer:
    good_old_caps_lock: true
    switch_key: {Caps_Lock: commit_code, Shift_L: commit_code, Shift_R: commit_code}
  key_binder:
    bindings: [{accept: ISO_Left_Tab, send: Page_Up, when: composing}, {accept: "Shift+Tab", send: Page_Up, when: composing}, {accept: Tab, send: Page_Down, when: composing}, {accept: minus, send: Page_Up, when: has_menu}, {accept: equal, send: Page_Down, when: has_menu}, {accept: comma, send: Page_Up, when: paging}, {accept: period, send: Page_Down, when: has_menu}, {accept: bracketleft, send: Page_Up, when: paging}, {accept: bracketright, send: Page_Down, when: has_menu}]
  "menu/page_size": 9
  translator/enable_user_dict: false

```

4,到上面一步,注销从新进系统, 就已经完成了.如果还有其他配置配置微调,可参考

https://github.com/pdog18/rime-soak

5, 愉快的智能ABC盲打吧

6, 关于用户词典的问题. 如果打开用户词典translator/enable_user_dict: true
会出现单字词频也被调整了. 但是关掉用户词典translator/enable_user_dict: false  后. 
会导致造词不被记录. 似乎也没有有效的办法.
想打长词, 还是换其他输入法吧. 智能ABC比较适合单字, 和词组盲打.
