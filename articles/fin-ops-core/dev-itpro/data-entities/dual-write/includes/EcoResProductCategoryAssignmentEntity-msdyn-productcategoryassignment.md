## <a name="product-category-assignments-to-msdyn_productcategoryassignments"></a>产品类别分配到 msdyn_productcategoryassignments

此模板在 Finance and Operations 应用与 Common Data Service 之间同步数据。

Finance and Operations 字段 | 映射类型 | 其他 Dynamics 365 字段 | 默认值
---|---|---|---
PRODUCTNUMBER | = | msdyn_globalproduct.msdyn_productnumber | 
PRODUCTCATEGORYNAME | = | msdyn_productcategory.msdyn_name | 
PRODUCTCATEGORYHIERARCHYNAME | = | msdyn_productcategory.msdyn_hierarchy.msdyn_name | 
PRODUCTNUMBER | >> | msdyn_name | 
