# SimpleTestForNodeJS
简单的Node JS测试

### 如何测试node js

node ${file} 


### 如何让.test.js的文件去运行所有已Test结尾的函数呢？

运行一下代码，简单例子
```
class SettingConfigTest {

  findConfigByIdTest() {
       //TDDO 进行测试
  }

  imageConfigTest() {
      //TODO 进行测试
  }
}

main = () => {
  console.log(__filename);
  let t = new SettingConfigTest();
  let props=t.__proto__;
  Object.getOwnPropertyNames(props).forEach(
    function(key){
      if (key.endsWith('Test')){
        console.log("\n\n\n")
        console.log("执行:%s() \t 测试",key)
        console.log("start-------------------------------------------------------")
        props[key]()
        console.log("end---------------------------------------------------------")
      }
    }
  );
}
main();

```
