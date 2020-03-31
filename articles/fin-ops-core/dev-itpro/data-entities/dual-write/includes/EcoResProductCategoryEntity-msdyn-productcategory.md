## <a name="product-categories-to-msdyn_productcategories"></a><span data-ttu-id="e3f21-101">产品类别到 msdyn_productcategories</span><span class="sxs-lookup"><span data-stu-id="e3f21-101">Product categories to msdyn_productcategories</span></span>

<span data-ttu-id="e3f21-102">此模板在 Finance and Operations 应用与 Common Data Service 之间同步数据。</span><span class="sxs-lookup"><span data-stu-id="e3f21-102">This template synchronizes data between Finance and Operations apps and Common Data Service.</span></span>

<span data-ttu-id="e3f21-103">Finance and Operations 字段</span><span class="sxs-lookup"><span data-stu-id="e3f21-103">Finance and Operations field</span></span> | <span data-ttu-id="e3f21-104">映射类型</span><span class="sxs-lookup"><span data-stu-id="e3f21-104">Map type</span></span> | <span data-ttu-id="e3f21-105">其他 Dynamics 365 字段</span><span class="sxs-lookup"><span data-stu-id="e3f21-105">Other Dynamics 365 field</span></span> | <span data-ttu-id="e3f21-106">默认值</span><span class="sxs-lookup"><span data-stu-id="e3f21-106">Default value</span></span>
---|---|---|---
<span data-ttu-id="e3f21-107">PRODUCTCATEGORYHIERARCHYNAME</span><span class="sxs-lookup"><span data-stu-id="e3f21-107">PRODUCTCATEGORYHIERARCHYNAME</span></span> | = | <span data-ttu-id="e3f21-108">msdyn_hierarchy.msdyn_name</span><span class="sxs-lookup"><span data-stu-id="e3f21-108">msdyn_hierarchy.msdyn_name</span></span> | 
<span data-ttu-id="e3f21-109">ISCATEGORYINHERITINGPARENTPRODUCTATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="e3f21-109">ISCATEGORYINHERITINGPARENTPRODUCTATTRIBUTES</span></span> | >< | <span data-ttu-id="e3f21-110">msdyn_isinheritingparentproductattributes</span><span class="sxs-lookup"><span data-stu-id="e3f21-110">msdyn_isinheritingparentproductattributes</span></span> | 
<span data-ttu-id="e3f21-111">PROJECTCATEGORYNAME</span><span class="sxs-lookup"><span data-stu-id="e3f21-111">PROJECTCATEGORYNAME</span></span> | = | <span data-ttu-id="e3f21-112">msdyn_projectcategoryname</span><span class="sxs-lookup"><span data-stu-id="e3f21-112">msdyn_projectcategoryname</span></span> | 
<span data-ttu-id="e3f21-113">ISTANGIBLEPRODUCT</span><span class="sxs-lookup"><span data-stu-id="e3f21-113">ISTANGIBLEPRODUCT</span></span> | >< | <span data-ttu-id="e3f21-114">msdyn_istangibleproduct</span><span class="sxs-lookup"><span data-stu-id="e3f21-114">msdyn_istangibleproduct</span></span> | 
<span data-ttu-id="e3f21-115">ISCATEGORYINHERITINGPARENTCATEGORYATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="e3f21-115">ISCATEGORYINHERITINGPARENTCATEGORYATTRIBUTES</span></span> | >< | <span data-ttu-id="e3f21-116">msdyn_isinheritingparentcategoryattributes</span><span class="sxs-lookup"><span data-stu-id="e3f21-116">msdyn_isinheritingparentcategoryattributes</span></span> | 
<span data-ttu-id="e3f21-117">CATEGORYCODE</span><span class="sxs-lookup"><span data-stu-id="e3f21-117">CATEGORYCODE</span></span> | = | <span data-ttu-id="e3f21-118">msdyn_code</span><span class="sxs-lookup"><span data-stu-id="e3f21-118">msdyn_code</span></span> | 
<span data-ttu-id="e3f21-119">CATEGORYDESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e3f21-119">CATEGORYDESCRIPTION</span></span> | = | <span data-ttu-id="e3f21-120">msdyn_description</span><span class="sxs-lookup"><span data-stu-id="e3f21-120">msdyn_description</span></span> | 
<span data-ttu-id="e3f21-121">CATEGORYKEYWORDS</span><span class="sxs-lookup"><span data-stu-id="e3f21-121">CATEGORYKEYWORDS</span></span> | = | <span data-ttu-id="e3f21-122">msdyn_keywords</span><span class="sxs-lookup"><span data-stu-id="e3f21-122">msdyn_keywords</span></span> | 
<span data-ttu-id="e3f21-123">CATEGORYNAME</span><span class="sxs-lookup"><span data-stu-id="e3f21-123">CATEGORYNAME</span></span> | = | <span data-ttu-id="e3f21-124">msdyn_name</span><span class="sxs-lookup"><span data-stu-id="e3f21-124">msdyn_name</span></span> | 
<span data-ttu-id="e3f21-125">FRIENDLYCATEGORYNAME</span><span class="sxs-lookup"><span data-stu-id="e3f21-125">FRIENDLYCATEGORYNAME</span></span> | = | <span data-ttu-id="e3f21-126">msdyn_friendlycategoryname</span><span class="sxs-lookup"><span data-stu-id="e3f21-126">msdyn_friendlycategoryname</span></span> | 
<span data-ttu-id="e3f21-127">PARENTPRODUCTCATEGORYNAME</span><span class="sxs-lookup"><span data-stu-id="e3f21-127">PARENTPRODUCTCATEGORYNAME</span></span> | = | <span data-ttu-id="e3f21-128">msdyn_parentproductcategory.msdyn_name</span><span class="sxs-lookup"><span data-stu-id="e3f21-128">msdyn_parentproductcategory.msdyn_name</span></span> | 
<span data-ttu-id="e3f21-129">PRODUCTCATEGORYHIERARCHYNAME</span><span class="sxs-lookup"><span data-stu-id="e3f21-129">PRODUCTCATEGORYHIERARCHYNAME</span></span> | >> | <span data-ttu-id="e3f21-130">msdyn_parentproductcategory.msdyn_hierarchy.msdyn_name</span><span class="sxs-lookup"><span data-stu-id="e3f21-130">msdyn_parentproductcategory.msdyn_hierarchy.msdyn_name</span></span> | 