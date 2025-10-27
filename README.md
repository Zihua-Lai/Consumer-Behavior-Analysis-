# Consumer-Behavior-Analysis

## Data 

### Data Introduction 
user_id:用户ID，order_dt:购买日期，order_products:购买产品数量,order_amount:购买金额
数据时间：1997年1月~1998年6月用户行为数据，约6万条

### Data Description 
1.用户平均每笔订单购买2.4个商品，标准差2.3，稍微有点波动，属于正常。然而75%分位数的时候，说明绝大多数订单的购买量都不多，围绕在2~3个产品左右；
2.购买金额，反映出大部分订单消费金额集中在中小额，30~45左右

## 1 Customer Behaviour Analysis -- First and Last Time Purchase Analysis 
### Analyse the consumers individually 
#### 1) Consumer order amount and purchase frequency 
从用户的角度：用户数量23570个，每个用户平均购买7个CD，但是中位数只有3，并且最大购买量为1033，平均值大于中位数，属于典型的右偏分布(替购买量<7的用户背锅)
从消费金额角度：平均用户消费106，中位数43，并且存在土豪用户13990，结合分位数和最大值来看，平均数与75%分位数几乎相等，属于典型的右偏分布，说明存在小部分用户（后面的25%）高额消费（这些用户需要给消费金额<106的用户背锅，只有这样才能使平均数维持在106）

#### 2) The contribution of consumers 
前20000名用户贡献总金额的40%，剩余3500名用户贡献了60%。（2/8原则）

### The first and last purchase time 
大多数用户最后一次购买时间集中在前3个月，说明缺少忠诚用户。
随着时间的推移，最后一次购买商品的用户量呈现上升趋势，猜测：这份数据选择是的前三个月消费的用户在后面18个月的跟踪记录


## 2 User Segmentation
Created an RFM model and did the data visualisation. 

## 3 New Customer, Active Customers, and Returning Customers Analysis 
新用户的定义是第一次消费。
活跃用户即老客，在某一个时间窗口内有过消费。
不活跃用户则是时间窗口内没有消费过的老客。
回流用户：相当于回头客的意思。
用户回流的动作可以分为自主回流与人工回流，自主回流指玩家自己回流了，而人工回流则是人为参与导致的。

回流用户：前五个月，回流用户上涨，过后呈现下降趋势，平均维持在5%比例
活跃用户：前三个月活跃用户大量增长，猜测由于活到新引来很多新用户所导致.5月份过后开始下降，平均维持在2.5%左右 . 网站运营稳定后，回流用户占比大于活跃用户


## 4 Customer Purchase cycle and Life Cycle 
### 1) Purchase Cycle 
平均消费周期为68天
大多数用户消费周期低于100天
呈现典型的长尾分布，只有小部分用户消费周期在200天以上（不积极消费的用户），可以在这批用户消费后3天左右进行电话回访后者短信
赠送优惠券等活动，增大消费频率

### 2) Life Cycle 
对比可知，第二幅图过滤掉了生命周期==0的用户，呈现双峰结构
虽然二图中还有一部分用户的生命周期趋于0天，但是比第一幅图好了很多，虽然进行了多次消费，但是不成长期来消费，属于普通用户，可针对性进行营销推广活动
少部分用户生命周期集中在300~500天，属于我们的忠诚客户，需要大力度维护此类客户


## 5 Repeated Purchase Rate and Repurchase Rate 
### 1) Repeated Purchase Rate 
计算方式：在自然月内，购买多次的用户在总消费人数中的占比（若客户在同一天消费了多次，也称之复购用户）
消费者有三种：消费记录>=2次的；消费中人数；本月无消费用户；
复购用户:1    非复购的消费用户：0   自然月没有消费记录的用户：NAN(不参与count计数)

### 2) Repurchase Rate 
计算方式：在一个时间窗口内进行了消费，在下一个窗口内又进行了消费






