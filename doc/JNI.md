# JNI

* Java 与 C 之间的相互调用 
* Android 下 FFmpeg 的编译
* Android 下如何使用FFmpeg


### Java调用C/C++方法一  
* 在java层定义native 关键字函数  
* 方法一：在C/C++层创建 Java_packname_classname_methodname 函数  

### Java调用C/C++方法二   
* RegisterNative 

```
 typedef struct{
      const char* name;
      const char* signature;
      void* fnPtr;
 }JNINativeMethod;  
```   
 
* 注册Native方法的最佳时机  
 - jint JNI_OnLoad(JavaVM *vm, void* reserved)
 - jint JNI_OnUnload(JavaVM *vm, void* reserved) 


#### Signature  
* Java与C/C++相互调用时，表示函数参数的描述符
