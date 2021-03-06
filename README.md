#KyLog

这是一个Android上关于LogCat的工具库，它十分方便好用。

具体说明可以看该[博客](http://blog.csdn.net/kyosky110/article/details/50470463)

KyLog的特性:
- 打印类名信息
- 打印方法信息
- 打印json内容
- 打印类的属性值
- 打印数据集合list、map

##Dependency
```
dependencies {
	compile 'com.kyosky110.kylog:kylog:1.0.1'
}
```

##Usage

####简单的打印
```
KyLog.d("hello,word");
KyLog.e("hello,word");
KyLog.d("%d个小蜜蜂", 4);//打印统配符
```

![](https://github.com/kyosky110/Kylog/blob/master/screenshots/kylog_string.png)

####打印json
```
KyLog.json("{\"person\":{\"name\":\"小蜜蜂\",\"sex\":\"男\",\"age\":\"18\"}}");
```

![](https://github.com/kyosky110/Kylog/blob/master/screenshots/klog_json.png)

####打印map
```
Map<String,String> map = new HashMap<>();
map.put("你好","我很好");
map.put("我好", "你很好");
KyLog.object(map);
```
![](https://github.com/kyosky110/Kylog/blob/master/screenshots/klog_map.png)

####打印对象
```
Person person = new Person();
person.setAge(10);
person.setSex(true);
person.setName("lily");
person.setSays("hello man");
KyLog.object(person);
```
![](https://github.com/kyosky110/Kylog/blob/master/screenshots/kylog_object.png)

####打印List
```
List<Person> list = new ArrayList<>();
list.add(person);
KyLog.object(list);
```
![](https://github.com/kyosky110/Kylog/blob/master/screenshots/kylog_list.png)

####取消打印
推荐在自己的applicatoin类里面添加
```
KyLog.configAllowLog = false;
```

##About


###Thanks
 thanks to [pengwei1024/LogUtils](https://github.com/pengwei1024/LogUtils) . it give me a great deal of help.





