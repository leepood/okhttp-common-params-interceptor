# okhttp-common-params-interceptor
A simple interceptor for okhttp3 to add common paramters

# how to use
### Add to gradle

```
repositories {
  maven { url 'https://dl.bintray.com/leepood/maven' }
  
}  
 ```
 
 ```
 dependencies {
    compile 'com.leepood:okhttp3-common-params-interceptor:v0.1'
 }
 ```
 
 ### Add to OkHttp
 
 ```
 
HttpCommonParamsInterceptor interceptor = new HttpCommonParamsInterceptor.Builder()
                .type(HttpCommonParamsInterceptor.Builder.Type.AUTO)
                .params("f","android")
                .params("weixin",0)
                .params("v",8.4)
                .build();
                
 OkHttpClient httpClient =  new OkHttpClient.Builder()
                .addInterceptor(interceptor)
                .connectTimeout(1, TimeUnit.MINUTES)
                .build();
 
 ```
 
 
 
