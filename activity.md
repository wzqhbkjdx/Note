#activity的生命周期

1. onCreate()方法 Activity完整生存周期开始时调用
2. onStart()方法 Activity可见的时候调用
3. onResum()方法 Activity生存期开始的时候调用 恢复Activity时
4. onPause()方法 当Activity不是前台活动的Activity时
5. onStop()方法 Activity不可见时
6. onDestory()方法 Activity完整生存周期结束时调用
7. onRestart()方法 Activity可见 加装载改变的时候调用

##onCreate()方法：

*inflate用户界面

*得到对fragment的引用

*分配对类变量的引用

*将数据绑定到控件

*启动service和定时器

**如果activity意外终止了，onCreate()方法接收一个包含UI状态的Bundle对象通过最后一次调用onSaveInstanceState()方法保存，这个Bundle将UI恢复成上一次的状态，既可以通过重写onRestoreInstanceState方法，也可以通过onCreate()方法**

##可见生存期
##onStop()方法
*暂停或者停止动画/线程/传感器监听器/GPS查找/定时器/Service/或者其他专门用于更新用户界面的进程。当UI再次可见的时候，可以使用onStart()方法或者onRestart()方法来恢复或者重启这些进程。