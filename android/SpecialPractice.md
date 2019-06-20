1. 当`Activity`被销毁时，如何保存它原来的状态？

   实现`Activity`的`onSaveInstanceState()`方法

   > 当你的程序中某一个Activity **A** 在运行时，主动或被动地运行另一个新的Activity **B**,这个时候**A**会执行`onSaveInstanceState()`。
   >
   > **B** 完成以后又会回来找 **A**,这个时候就有两种情况：
   >
   > 	1. **A**被回收，被回收的**A**就要重新调用`onCreate()`方法，不同于直接启动的是这回`onCreate()`里是带上了参数`saveInstanceState`;
   >  	2. **A**未被回收，直接执行`onResume()`，跳过`onCreate()`.

参考 [https://developer.android.com/guide/components/activities#SavingActivityState](https://developer.android.com/guide/components/activities#SavingActivityState)

