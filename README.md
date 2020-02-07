# 合肥市冠状病毒期间口罩预约脚本
> 武汉加油！中国加油！

## 注意事项
1. 请勿高频请求！请勿高频请求！
2. 每人一段时间只可预约一次，请勿重复预约。
3. 切勿用于商用。
4. 如若违法侵权请告知，必删。
5. 所有数据均从合肥医保预约口罩页面获取。
6. 为啥不用ES6？因为我从网上抄的一段request请求方法，而且加密的也是ES5，于是就统一ES5，还兼容低版本Node。哈哈哈哈哈。。。。

### 使用帮助
1. `confg.js`中的`getDataInterval`参数是多长时间请求一次，默认是1000ms。
2. `userData.js`中，依次输入您的个人信息，其中`reservationNumber`为固定的**五个**，请勿改动。因为规定是预约只能预约5个且预约成功后，5天内不可在此预约。
3. 如果您不知道您要领取的药店的名称和编号，请点击`getPharmacy.js`，在第二行`pharmacyName`处输入您想查询的药房名称，然后执行`node getPharmacy.js`即可查阅到相关信息。药房数据格式请查阅`common/pharmacy.json`，其中每个数据的`name`值，即为药店名称，其`code`就是药店的编号ID。或者[在此查询](http://kzgm.bbshjz.cn:8000/ncms/mask/pharmacy-list)，其中编号ID可以通过审查元素或者接口信息中看到。
4. ![pharmacy](https://github.com/542154968/getHfMask/blob/master/images/pharmacy.jpg)

#### 开始
1. 首先您要有`Node`环境，如果没有，请百度`Node`安装一个 - -
2. 运行`npm install`
3. 在`userData.js`中，按照提示填好**个人信息**和**药店信息**
4. 运行`node index.js` 即可开始请求，请勿高频请求！每天17:00可预约第二日口罩。所以您每天16:59:50再启动该脚本吧~已经预约到的5天不能再预约了哦！

##### 题外
1. 就在刚才我预约到了口罩，很开心，自己写的脚本有用~嘻嘻
2. ![requestInfo](https://github.com/542154968/getHfMask/blob/master/images/requestInfo.png)
3. ![getMaskDetail](https://github.com/542154968/getHfMask/blob/master/images/getMaskDetail.jpg)