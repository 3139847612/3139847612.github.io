label 标签用来将文字和单选按钮进行绑定
当用户单击文字时，等于点击了单选按钮 ，`在HTML5中直接使用 label 标签包裹 单选按钮和文字 即可`
```
性别：
<label> <input type="radio" name="sex" /> 男 </label>
<label> <input type="radio" name="sex" /> 女 </label>
<label> <input type="radio" name="sex" checked /> 保密 </label>
```


在html4中label 标签是通过 for 属性和单选按钮的 id 属性进行绑定的
```
所在城市：
<input type="radio" name="city" id="beijing" />
<label for="beijing">北京市</label>

<input type="radio" name="city" id="shanghai" />
<label for="shanghai">上海市</label>

<input type="radio" name="city" id="shenzhen" />
<label for="shenzhen">深圳市</label>
```

