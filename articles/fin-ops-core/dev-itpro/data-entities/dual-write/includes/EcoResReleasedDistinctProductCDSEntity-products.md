## <a name="cds-released-distinct-products-to-products"></a><span data-ttu-id="a240e-101">CDS 发放的独特产品到产品</span><span class="sxs-lookup"><span data-stu-id="a240e-101">CDS released distinct products to products</span></span>

<span data-ttu-id="a240e-102">此模板在 Finance and Operations 应用与 Common Data Service 之间同步数据。</span><span class="sxs-lookup"><span data-stu-id="a240e-102">This template synchronizes data between Finance and Operations apps and Common Data Service.</span></span>

<span data-ttu-id="a240e-103">Finance and Operations 字段</span><span class="sxs-lookup"><span data-stu-id="a240e-103">Finance and Operations field</span></span> | <span data-ttu-id="a240e-104">映射类型</span><span class="sxs-lookup"><span data-stu-id="a240e-104">Map type</span></span> | <span data-ttu-id="a240e-105">其他 Dynamics 365 字段</span><span class="sxs-lookup"><span data-stu-id="a240e-105">Other Dynamics 365 field</span></span> | <span data-ttu-id="a240e-106">默认值</span><span class="sxs-lookup"><span data-stu-id="a240e-106">Default value</span></span>
---|---|---|---
<span data-ttu-id="a240e-107">PRODUCTNUMBER</span><span class="sxs-lookup"><span data-stu-id="a240e-107">PRODUCTNUMBER</span></span> | >> | <span data-ttu-id="a240e-108">msdyn_productnumber</span><span class="sxs-lookup"><span data-stu-id="a240e-108">msdyn_productnumber</span></span> | 
<span data-ttu-id="a240e-109">PRODUCTNAME</span><span class="sxs-lookup"><span data-stu-id="a240e-109">PRODUCTNAME</span></span> | >> | <span data-ttu-id="a240e-110">name</span><span class="sxs-lookup"><span data-stu-id="a240e-110">name</span></span> | 
<span data-ttu-id="a240e-111">PRODUCTDESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a240e-111">PRODUCTDESCRIPTION</span></span> | >> | <span data-ttu-id="a240e-112">description</span><span class="sxs-lookup"><span data-stu-id="a240e-112">description</span></span> | 
<span data-ttu-id="a240e-113">ITEMNUMBER</span><span class="sxs-lookup"><span data-stu-id="a240e-113">ITEMNUMBER</span></span> | >> | <span data-ttu-id="a240e-114">msdyn_itemnumber</span><span class="sxs-lookup"><span data-stu-id="a240e-114">msdyn_itemnumber</span></span> | 
<span data-ttu-id="a240e-115">CURRENCYCODE</span><span class="sxs-lookup"><span data-stu-id="a240e-115">CURRENCYCODE</span></span> | >> | <span data-ttu-id="a240e-116">transactioncurrencyid.isocurrencycode</span><span class="sxs-lookup"><span data-stu-id="a240e-116">transactioncurrencyid.isocurrencycode</span></span> | 
<span data-ttu-id="a240e-117">SALESUNITSYMBOL</span><span class="sxs-lookup"><span data-stu-id="a240e-117">SALESUNITSYMBOL</span></span> | >> | <span data-ttu-id="a240e-118">defaultuomid.msdyn_symbol</span><span class="sxs-lookup"><span data-stu-id="a240e-118">defaultuomid.msdyn_symbol</span></span> | 
<span data-ttu-id="a240e-119">SALESPRICE</span><span class="sxs-lookup"><span data-stu-id="a240e-119">SALESPRICE</span></span> | >> | <span data-ttu-id="a240e-120">price</span><span class="sxs-lookup"><span data-stu-id="a240e-120">price</span></span> | 
<span data-ttu-id="a240e-121">UNITCOST</span><span class="sxs-lookup"><span data-stu-id="a240e-121">UNITCOST</span></span> | >> | <span data-ttu-id="a240e-122">currentcost</span><span class="sxs-lookup"><span data-stu-id="a240e-122">currentcost</span></span> | 
<span data-ttu-id="a240e-123">PRODUCTTYPE</span><span class="sxs-lookup"><span data-stu-id="a240e-123">PRODUCTTYPE</span></span> | >> | <span data-ttu-id="a240e-124">producttypecode</span><span class="sxs-lookup"><span data-stu-id="a240e-124">producttypecode</span></span> | 
<span data-ttu-id="a240e-125">SALESUNITDECIMALPRECISION</span><span class="sxs-lookup"><span data-stu-id="a240e-125">SALESUNITDECIMALPRECISION</span></span> | >> | <span data-ttu-id="a240e-126">quantitydecimal</span><span class="sxs-lookup"><span data-stu-id="a240e-126">quantitydecimal</span></span> | <span data-ttu-id="a240e-127">0</span><span class="sxs-lookup"><span data-stu-id="a240e-127">0</span></span>
<span data-ttu-id="a240e-128">ISCATCHWEIGHTPRODUCT</span><span class="sxs-lookup"><span data-stu-id="a240e-128">ISCATCHWEIGHTPRODUCT</span></span> | >> | <span data-ttu-id="a240e-129">msdyn_iscatchweight</span><span class="sxs-lookup"><span data-stu-id="a240e-129">msdyn_iscatchweight</span></span> | 
<span data-ttu-id="a240e-130">PRODUCTCOLORID</span><span class="sxs-lookup"><span data-stu-id="a240e-130">PRODUCTCOLORID</span></span> | >> | <span data-ttu-id="a240e-131">msdyn_productcolor.msdyn_productcolorname</span><span class="sxs-lookup"><span data-stu-id="a240e-131">msdyn_productcolor.msdyn_productcolorname</span></span> | 
<span data-ttu-id="a240e-132">PRODUCTCONFIGURATIONID</span><span class="sxs-lookup"><span data-stu-id="a240e-132">PRODUCTCONFIGURATIONID</span></span> | >> | <span data-ttu-id="a240e-133">msdyn_productconfiguration.msdyn_productconfiguration</span><span class="sxs-lookup"><span data-stu-id="a240e-133">msdyn_productconfiguration.msdyn_productconfiguration</span></span> | 
<span data-ttu-id="a240e-134">PRODUCTSIZEID</span><span class="sxs-lookup"><span data-stu-id="a240e-134">PRODUCTSIZEID</span></span> | >> | <span data-ttu-id="a240e-135">msdyn_productsize.msdyn_productsize</span><span class="sxs-lookup"><span data-stu-id="a240e-135">msdyn_productsize.msdyn_productsize</span></span> | 
<span data-ttu-id="a240e-136">PRODUCTSTYLEID</span><span class="sxs-lookup"><span data-stu-id="a240e-136">PRODUCTSTYLEID</span></span> | >> | <span data-ttu-id="a240e-137">msdyn_productstyle.msdyn_productstyle</span><span class="sxs-lookup"><span data-stu-id="a240e-137">msdyn_productstyle.msdyn_productstyle</span></span> | 