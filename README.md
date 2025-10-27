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
