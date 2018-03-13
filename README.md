# Combobox
基于 jQueryUI的 Combobox组件


使用：

```js
var address = $('.input-combobox').combobox({
    placeholder: 'Please Select',
    editable: false,
    dataSource: [{
        name: '南京', value: '0'
    }, {
        name: '徐州', value: '1'
    }, {
        name: '苏州', value: '2', disabled: true
    }, {
        name: '连云港', value: '3', selected: true
    }, {
        name: '常州', value: '4',
    }, {
        name: '无锡', value: '5'
    }],
    change: function(e, selectedItem) {
        console.log('--- change event ---');
        console.log(selectedItem);
    }
});

// 设置值选中
address.combobox('value', '1');

// 取值
var value = address.combobox('value');

// 获取选中项的键值对
var item = address.combobox('getSelectedItem');

// 设置控件不可用
address.combobox('disable');

// 设置控件可用
address.combobox('enable');

// 设置控件可编辑
address.combobox('setEditable', true);

// 设置控件不可编辑
address.combobox('setEditable', false);

// 向控件中追加项
address.combobox('append', [{
    name: '淮安',
    value: '6',
    selected: true
}, {
    name: '宿迁',
    value: '7',
    disabled: true
}]);

// 从控件中移除项
address.combobox('remove', [{
    name: '无锡',
    value: '5'
}]);

// 清空
address.combobox('clear');

// 销毁
address.combobox('destroy');

// 重新初始化
address.combobox(options);
```