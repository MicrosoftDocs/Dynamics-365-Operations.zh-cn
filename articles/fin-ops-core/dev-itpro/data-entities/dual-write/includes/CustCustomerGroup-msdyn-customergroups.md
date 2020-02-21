## <a name="customer-groups-to-msdyn_customergroups"></a>客户组到 msdyn_customergroups

此模板在 Finance and Operations 应用与 Common Data Service 之间同步数据。

Finance and Operations 字段 | 映射类型 | 其他 Dynamics 365 字段 | 默认值
---|---|---|---
CUSTOMERGROUPID | = | msdyn_groupid | 
DESCRIPTION | = | msdyn_description | 
ISSALESTAXINCLUDEDINPRICE | >< | msdyn_issalestaxincludedinprice | 
PAYMENTTERMID | = | msdyn_paymenttermid.msdyn_name | 
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn_clearingperiodpaymenttermname.msdyn_name | 
