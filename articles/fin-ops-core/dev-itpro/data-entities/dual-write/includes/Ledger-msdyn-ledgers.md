## <a name="ledger-to-msdyn_ledgers"></a>分类账到 msdyn_ledgers

此模板在 Finance and Operations 应用与 Common Data Service 之间同步数据。

Finance and Operations 字段 | 映射类型 | 其他 Dynamics 365 字段 | 默认值
---|---|---|---
LEGALENTITYID | >> | msdyn_company.cdm_companycode | 
DESCRIPTION | >> | msdyn_description | 
ACCOUNTINGCURRENCY | >> | msdyn_accountingcurrency.isocurrencycode | 
ISBUDGETCONTROLENABLED | >> | msdyn_isbudgetcontrolenabled | 
NAME | >> | msdyn_name | 
REPORTINGCURRENCY | >> | msdyn_reportingcurrency.isocurrencycode | 
BUDGETEXCHANGERATETYPE | >> | msdyn_budgetexchangeratetype.msdyn_name | 
CHARTOFACCOUNTS | >> | msdyn_chartofaccounts.msdyn_name | 
EXCHANGERATETYPE | >> | msdyn_exchangeratetype.msdyn_name | 
FISCALCALENDAR | >> | msdyn_fiscalcalendar.msdyn_calendar | 
REPORTINGCURRENCYEXCHANGERATETYPE | >> | msdyn_reportingcurrencyexchangeratetype.msdyn_name | 
