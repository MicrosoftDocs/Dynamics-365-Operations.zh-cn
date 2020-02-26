## <a name="currencies-to-transactioncurrencies"></a>币种到交易币种

此模板在 Finance and Operations 应用与 Common Data Service 之间同步数据。

源筛选器：((CURRENCYCODE != "999"))

Finance and Operations 字段 | 映射类型 | 其他 Dynamics 365 字段 | 默认值
---|---|---|---
CURRENCYCODE | = | isocurrencycode | 
NAME | = | currencyname | 
SYMBOL | = | currencysymbol | 
none | >> | exchangerate | 1
