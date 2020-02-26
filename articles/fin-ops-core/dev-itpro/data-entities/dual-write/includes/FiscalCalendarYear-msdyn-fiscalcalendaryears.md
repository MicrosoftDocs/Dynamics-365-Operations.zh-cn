## <a name="fiscal-calendar-year-integration-entity-to-msdyn_fiscalcalendaryears"></a>会计日历年度集成实体到 msdyn_fiscalcalendaryears

此模板在 Finance and Operations 应用与 Common Data Service 之间同步数据。

Finance and Operations 字段 | 映射类型 | 其他 Dynamics 365 字段 | 默认值
---|---|---|---
FISCALCALENDAR_CALENDARID | = | msdyn_fiscalcalendarname | 
NAME | = | msdyn_name | 
STARTDATE | = | msdyn_startdate | 
ENDDATE | = | msdyn_enddate | 
FISCALCALENDAR_CALENDARID | = | msdyn_calendar.msdyn_calendar | 
