## <a name="currencies-to-transactioncurrencies"></a><span data-ttu-id="70f6a-101">币种到交易币种</span><span class="sxs-lookup"><span data-stu-id="70f6a-101">Currencies to transactioncurrencies</span></span>

<span data-ttu-id="70f6a-102">此模板在 Finance and Operations 应用与 Common Data Service 之间同步数据。</span><span class="sxs-lookup"><span data-stu-id="70f6a-102">This template synchronizes data between Finance and Operations apps and Common Data Service.</span></span>

<span data-ttu-id="70f6a-103">源筛选器：((CURRENCYCODE != "999"))</span><span class="sxs-lookup"><span data-stu-id="70f6a-103">Source filter: ((CURRENCYCODE != "999"))</span></span>

<span data-ttu-id="70f6a-104">Finance and Operations 字段</span><span class="sxs-lookup"><span data-stu-id="70f6a-104">Finance and Operations field</span></span> | <span data-ttu-id="70f6a-105">映射类型</span><span class="sxs-lookup"><span data-stu-id="70f6a-105">Map type</span></span> | <span data-ttu-id="70f6a-106">其他 Dynamics 365 字段</span><span class="sxs-lookup"><span data-stu-id="70f6a-106">Other Dynamics 365 field</span></span> | <span data-ttu-id="70f6a-107">默认值</span><span class="sxs-lookup"><span data-stu-id="70f6a-107">Default value</span></span>
---|---|---|---
<span data-ttu-id="70f6a-108">CURRENCYCODE</span><span class="sxs-lookup"><span data-stu-id="70f6a-108">CURRENCYCODE</span></span> | = | <span data-ttu-id="70f6a-109">isocurrencycode</span><span class="sxs-lookup"><span data-stu-id="70f6a-109">isocurrencycode</span></span> | 
<span data-ttu-id="70f6a-110">NAME</span><span class="sxs-lookup"><span data-stu-id="70f6a-110">NAME</span></span> | = | <span data-ttu-id="70f6a-111">currencyname</span><span class="sxs-lookup"><span data-stu-id="70f6a-111">currencyname</span></span> | 
<span data-ttu-id="70f6a-112">SYMBOL</span><span class="sxs-lookup"><span data-stu-id="70f6a-112">SYMBOL</span></span> | = | <span data-ttu-id="70f6a-113">currencysymbol</span><span class="sxs-lookup"><span data-stu-id="70f6a-113">currencysymbol</span></span> | 
<span data-ttu-id="70f6a-114">none</span><span class="sxs-lookup"><span data-stu-id="70f6a-114">none</span></span> | >> | <span data-ttu-id="70f6a-115">exchangerate</span><span class="sxs-lookup"><span data-stu-id="70f6a-115">exchangerate</span></span> | <span data-ttu-id="70f6a-116">1</span><span class="sxs-lookup"><span data-stu-id="70f6a-116">1</span></span>
