# tingle-radio-field [![tnpm version](http://web.npm.alibaba-inc.com/badge/v/@ali/tingle-radio-field.svg?style=flat-square)](http://web.npm.alibaba-inc.com/package/@ali/tingle-radio-field)

单选框犹如人中之凤，万里挑一。  

![](http://gtms01.alicdn.com/tps/i1/TB1NxzWJFXXXXXiXVXXbLzyZVXX-320-194.png)

## Install

```
tnpm install @ali/tingle-radio-field --save
```

## Simple Usage
```javascript
let radioFieldProps = {
    data: [
    {
        value:"1",
        checked: true,
        text: (<div>你好</div>),
        disable: false
    }, 
    {
        value:"2",
        checked: false,
        text: "他好",
        disable: true
    }, 
    {
        value:"3",
        checked: false,
        text: "我也好",
        disable: false
    }, 
    {
        value:"4",
        checked: false,
        text: "大家都好",
        disable: false
    }
    ],
    onChange: function (value, index, data) {
        console.log(value, index, data);
    }
}
return <div>
    <RadioField {...radioFieldProps} />
</div>
```
## Props
#### className

描述：自定义的扩展样式名称

类型：String

默认：''

必填：否

#### data

描述：复选框所需数据

类型：Array

数组对象：
```javascript
{
    value: undefined, // 非必填，默认为undefined，当前复选框的value值，any
    checked:true, // 非必填，默认为false，是否选中，boolen
    text:"hello boys", // 非必填，默认空文本，文本域填充内容，String/jsx
    disable:true // 非必填，默认false，是否禁用，bollen
}    
```


默认：空数组

必填：否

#### onChange

描述：点击按钮的回调

类型：Function  

默认：空函数

必填：否

注入的参数:  
- value，当前复选框数据  
- index，当前复选框索引  
- data，所有复选框数据  

#### groupListFlag

描述：是否使用tingle-group来布局checkbox

类型：Boolen

默认：true

必填：否

#### label

描述：一个checkbox组的label

类型：String

默认：空字符串

必填：否

#### groupListArgument

描述：如果tingle-group为true，可以传入tingle-group相关参数。参考`http://gitlab.alibaba-inc.com/tingle-ui/tingle-group`

类型：Object

默认：  
```
{
    lineIndent:0,
    itemIndent:18
}
```


## APIs
#### getData(TO DO)

描述：获取复选框组数据

类型：Function

### 注意事项

1. 点击disable的复选框，不会触发用户注册的回调函数。
2. 单选框语义上你只能传入一个checked:true，如果你传入多个，我不阻止。

## Links

- [Issues](http://gitlab.alibaba-inc.com/tingle-ui/tingle-radio-field/issues)
- [README 标准写法](http://gitlab.alibaba-inc.com/tingle-ui/doc/blob/master/README%E6%A0%87%E5%87%86%E5%86%99%E6%B3%95.md)
