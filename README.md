# Android接口回调

[版权所有，转载注明]()

>回调方法一直是弱项，记录一下以后免得翻车。如有问题还请大佬们在评论出指出，谢谢。

### 1.在发送界面的步骤
#### 1.1 定义一个接口
```
public DemoInterface mDemoInterface;
```

#### 1.2 创建这个接口并新建一个方法
``` 
public interface DemoInterface {
        void demoMethod(String demoParameter);
    }
```

#### 1.3 实现该接口的Set方法
```
public void setmDemoInterface(DemoInterface demoInterface) {
        mDemoInterface= demoInterface;
    }
```

#### 1.4给接口的方法内的参数赋值
```
mDemoInterface.demoMethod("输入你想发送的参数");
```

### 2.在接收界面的步骤
#### 2.1 定义你创建的接口
- 直接输入接口名称就会自动弹出接口所在的界面前缀
```
DemoActivity.DemoInterface mDemoInterface;
```

#### 2.2 实例化接口并赋值
```
mDemoInterface=new DemoActivity.DemoInterface () {
            @Override
            public void demoMethod(String demoParameter) {
                String receivedParameter= demoParameter;
            }
        };
```
