---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azssubscription
schema: 2.0.0
ms.openlocfilehash: 7dce95be9a936d341e0f063fd6d89701b18c2ce7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877137"
---
# <span data-ttu-id="db136-101">Get-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="db136-101">Get-AzsSubscription</span></span>

## <span data-ttu-id="db136-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db136-102">SYNOPSIS</span></span>
<span data-ttu-id="db136-103">특정 구독에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="db136-103">Gets details about particular subscription.</span></span>

## <span data-ttu-id="db136-104">구문과</span><span class="sxs-lookup"><span data-stu-id="db136-104">SYNTAX</span></span>

### <span data-ttu-id="db136-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="db136-105">List (Default)</span></span>
```
Get-AzsSubscription [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="db136-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="db136-106">Get</span></span>
```
Get-AzsSubscription -SubscriptionId <String[]> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="db136-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="db136-107">GetViaIdentity</span></span>
```
Get-AzsSubscription -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="db136-108">설명은</span><span class="sxs-lookup"><span data-stu-id="db136-108">DESCRIPTION</span></span>
<span data-ttu-id="db136-109">특정 구독에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="db136-109">Gets details about particular subscription.</span></span>

## <span data-ttu-id="db136-110">예제의</span><span class="sxs-lookup"><span data-stu-id="db136-110">EXAMPLES</span></span>

### <span data-ttu-id="db136-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="db136-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsSubscription | fl *

DisplayName    : Test User
Id             : /subscriptions/97d84f7a-bef7-4f2d-b651-c553be472311
OfferId        : /delegatedProviders/default/offers/TestOffer-590376ac-c8dd-4b3d-9674-b5b8fcde095b
State          : Enabled
SubscriptionId : 97d84f7a-bef7-4f2d-b651-c553be472311
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb

DisplayName    : cnur
Id             : /subscriptions/ed3e275b-87d1-4e94-9962-b3700287bdbc
OfferId        : /delegatedProviders/default/offers/cnur4866tenantsubsvcoffer843
State          : Enabled
SubscriptionId : ed3e275b-87d1-4e94-9962-b3700287bdbc
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="db136-112">구독 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="db136-112">Get the list of subscriptions.</span></span>

## <span data-ttu-id="db136-113">변수</span><span class="sxs-lookup"><span data-stu-id="db136-113">PARAMETERS</span></span>

### <span data-ttu-id="db136-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db136-114">-DefaultProfile</span></span>
<span data-ttu-id="db136-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="db136-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="db136-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db136-116">-InputObject</span></span>
<span data-ttu-id="db136-117">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="db136-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="db136-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="db136-118">-SubscriptionId</span></span>
<span data-ttu-id="db136-119">구독의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="db136-119">Id of the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="db136-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db136-120">CommonParameters</span></span>
<span data-ttu-id="db136-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="db136-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db136-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="db136-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db136-123">입력</span><span class="sxs-lookup"><span data-stu-id="db136-123">INPUTS</span></span>

### <span data-ttu-id="db136-124">Microsoft. i d. PowerShell. ISubscriptionIdentity</span><span class="sxs-lookup"><span data-stu-id="db136-124">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="db136-125">출력</span><span class="sxs-lookup"><span data-stu-id="db136-125">OUTPUTS</span></span>

### <span data-ttu-id="db136-126">Api20151101 (Microsoft. PowerShell. i i i 구독</span><span class="sxs-lookup"><span data-stu-id="db136-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="db136-127">상속자</span><span class="sxs-lookup"><span data-stu-id="db136-127">NOTES</span></span>

<span data-ttu-id="db136-128">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="db136-128">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="db136-129">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="db136-129">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="db136-130">INPUTOBJECT <ISubscriptionIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="db136-130">INPUTOBJECT <ISubscriptionIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="db136-131">`[DelegatedProviderId <String>]`: 위임 된 공급자의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="db136-131">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="db136-132">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="db136-132">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="db136-133">`[OfferName <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db136-133">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="db136-134">`[SubscriptionId <String>]`: 구독의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="db136-134">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="db136-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="db136-135">RELATED LINKS</span></span>

