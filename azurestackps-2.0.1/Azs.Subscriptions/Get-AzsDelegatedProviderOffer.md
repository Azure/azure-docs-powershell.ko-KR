---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azsdelegatedprovideroffer
schema: 2.0.0
ms.openlocfilehash: 118834c020a198d355d3f3b9e6dc17699f88e0cc
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94045197"
---
# <span data-ttu-id="c14d0-101">Get-AzsDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="c14d0-101">Get-AzsDelegatedProviderOffer</span></span>

## <span data-ttu-id="c14d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c14d0-102">SYNOPSIS</span></span>
<span data-ttu-id="c14d0-103">위임 된 공급자에 대해 지정 된 제공을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c14d0-103">Get the specified offer for the delegated provider.</span></span>

## <span data-ttu-id="c14d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c14d0-104">SYNTAX</span></span>

### <span data-ttu-id="c14d0-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="c14d0-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c14d0-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="c14d0-106">Get</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> -OfferName <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c14d0-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c14d0-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProviderOffer -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c14d0-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c14d0-108">DESCRIPTION</span></span>
<span data-ttu-id="c14d0-109">위임 된 공급자에 대해 지정 된 제공을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c14d0-109">Get the specified offer for the delegated provider.</span></span>

## <span data-ttu-id="c14d0-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c14d0-110">EXAMPLES</span></span>

### <span data-ttu-id="c14d0-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c14d0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProviderOffer -DelegatedProviderId 4b763321-23f5-4a45-a44d-9ccfdd705a3d

{{ Add output here }}
```

<span data-ttu-id="c14d0-112">지정 된 위임 받은 공급자의 제안 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="c14d0-112">Get the list of offers for the specified delegated provider</span></span>

## <span data-ttu-id="c14d0-113">변수</span><span class="sxs-lookup"><span data-stu-id="c14d0-113">PARAMETERS</span></span>

### <span data-ttu-id="c14d0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c14d0-114">-DefaultProfile</span></span>
<span data-ttu-id="c14d0-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c14d0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c14d0-116">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="c14d0-116">-DelegatedProviderId</span></span>
<span data-ttu-id="c14d0-117">위임 된 공급자의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="c14d0-117">Id of the delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c14d0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c14d0-118">-InputObject</span></span>
<span data-ttu-id="c14d0-119">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c14d0-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c14d0-120">-OfferName</span><span class="sxs-lookup"><span data-stu-id="c14d0-120">-OfferName</span></span>
<span data-ttu-id="c14d0-121">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c14d0-121">Name of the offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c14d0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c14d0-122">CommonParameters</span></span>
<span data-ttu-id="c14d0-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c14d0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c14d0-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c14d0-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c14d0-125">입력</span><span class="sxs-lookup"><span data-stu-id="c14d0-125">INPUTS</span></span>

### <span data-ttu-id="c14d0-126">Microsoft. i d. PowerShell. ISubscriptionIdentity</span><span class="sxs-lookup"><span data-stu-id="c14d0-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="c14d0-127">출력</span><span class="sxs-lookup"><span data-stu-id="c14d0-127">OUTPUTS</span></span>

### <span data-ttu-id="c14d0-128">Api20151101를 통해 제공 되는 PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c14d0-128">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.IOffer</span></span>



## <span data-ttu-id="c14d0-129">상속자</span><span class="sxs-lookup"><span data-stu-id="c14d0-129">NOTES</span></span>

<span data-ttu-id="c14d0-130">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c14d0-130">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c14d0-131">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="c14d0-131">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c14d0-132">INPUTOBJECT <ISubscriptionIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c14d0-132">INPUTOBJECT <ISubscriptionIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c14d0-133">`[DelegatedProviderId <String>]`: 위임 된 공급자의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="c14d0-133">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="c14d0-134">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="c14d0-134">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c14d0-135">`[OfferName <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c14d0-135">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="c14d0-136">`[SubscriptionId <String>]`: 구독의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="c14d0-136">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="c14d0-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c14d0-137">RELATED LINKS</span></span>

