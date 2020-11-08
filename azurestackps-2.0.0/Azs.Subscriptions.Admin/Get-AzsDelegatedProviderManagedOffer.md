---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdelegatedprovidermanagedoffer
schema: 2.0.0
ms.openlocfilehash: 238fe2a9c3f0cf1d4fdefc5a09231066152cfe60
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/22/2020
ms.locfileid: "94045136"
---
# <span data-ttu-id="6b4dc-101">Get-AzsDelegatedProviderManagedOffer</span><span class="sxs-lookup"><span data-stu-id="6b4dc-101">Get-AzsDelegatedProviderManagedOffer</span></span>

## <span data-ttu-id="6b4dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b4dc-102">SYNOPSIS</span></span>
<span data-ttu-id="6b4dc-103">지정 된 위임 된 공급자 제안을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b4dc-103">Get the specified delegated provider offer.</span></span>

## <span data-ttu-id="6b4dc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6b4dc-104">SYNTAX</span></span>

### <span data-ttu-id="6b4dc-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="6b4dc-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6b4dc-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="6b4dc-106">Get</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId <String> -Name <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6b4dc-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6b4dc-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProviderManagedOffer -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b4dc-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6b4dc-108">DESCRIPTION</span></span>
<span data-ttu-id="6b4dc-109">지정 된 위임 된 공급자 제안을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b4dc-109">Get the specified delegated provider offer.</span></span>

## <span data-ttu-id="6b4dc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6b4dc-110">EXAMPLES</span></span>

### <span data-ttu-id="6b4dc-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6b4dc-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"

{{ Add output here }}
```

<span data-ttu-id="6b4dc-112">위임 된 공급자 제공 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="6b4dc-112">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="6b4dc-113">변수</span><span class="sxs-lookup"><span data-stu-id="6b4dc-113">PARAMETERS</span></span>

### <span data-ttu-id="6b4dc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b4dc-114">-DefaultProfile</span></span>
<span data-ttu-id="6b4dc-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6b4dc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b4dc-116">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6b4dc-116">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="6b4dc-117">위임 된 공급자 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="6b4dc-117">Delegated provider subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases: DelegatedProviderId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6b4dc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b4dc-118">-InputObject</span></span>
<span data-ttu-id="6b4dc-119">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6b4dc-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="6b4dc-120">-이름</span><span class="sxs-lookup"><span data-stu-id="6b4dc-120">-Name</span></span>
<span data-ttu-id="6b4dc-121">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b4dc-121">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6b4dc-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6b4dc-122">-SubscriptionId</span></span>
<span data-ttu-id="6b4dc-123">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b4dc-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6b4dc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b4dc-124">CommonParameters</span></span>
<span data-ttu-id="6b4dc-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b4dc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b4dc-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6b4dc-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b4dc-127">입력</span><span class="sxs-lookup"><span data-stu-id="6b4dc-127">INPUTS</span></span>

### <span data-ttu-id="6b4dc-128">SubscriptionsAdmin. ISubscriptionsAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="6b4dc-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="6b4dc-129">출력</span><span class="sxs-lookup"><span data-stu-id="6b4dc-129">OUTPUTS</span></span>

### <span data-ttu-id="6b4dc-130">SubscriptionsAdmin. Api20151101. IDelegatedProviderOffer에 대 한</span><span class="sxs-lookup"><span data-stu-id="6b4dc-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IDelegatedProviderOffer</span></span>

<span data-ttu-id="6b4dc-131">별칭과</span><span class="sxs-lookup"><span data-stu-id="6b4dc-131">ALIASES</span></span>

## <span data-ttu-id="6b4dc-132">상속자</span><span class="sxs-lookup"><span data-stu-id="6b4dc-132">NOTES</span></span>

<span data-ttu-id="6b4dc-133">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b4dc-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6b4dc-134">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="6b4dc-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="6b4dc-135">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6b4dc-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6b4dc-136">`[DelegatedProvider <String>]`: DelegatedProvider 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="6b4dc-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="6b4dc-137">`[DelegatedProviderSubscriptionId <String>]`: 위임 된 공급자 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="6b4dc-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="6b4dc-138">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="6b4dc-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6b4dc-139">`[Location <String>]`: AzureStack 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6b4dc-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="6b4dc-140">`[ManifestName <String>]`: 매니페스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b4dc-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="6b4dc-141">`[Offer <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b4dc-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="6b4dc-142">`[OfferDelegationName <String>]`: 제안 위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b4dc-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="6b4dc-143">`[OperationsStatusName <String>]`: 작업 상태 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b4dc-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="6b4dc-144">`[Plan <String>]`: 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b4dc-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="6b4dc-145">`[PlanAcquisitionId <String>]`: 계획 획득 식별자</span><span class="sxs-lookup"><span data-stu-id="6b4dc-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="6b4dc-146">`[Quota <String>]`: 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b4dc-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="6b4dc-147">`[ResourceGroupName <String>]`: 리소스 그룹이 아래에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b4dc-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="6b4dc-148">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b4dc-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="6b4dc-149">`[TargetSubscriptionId <String>]`: 대상 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6b4dc-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="6b4dc-150">`[Tenant <String>]`: 디렉터리 테 넌 트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b4dc-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="6b4dc-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b4dc-151">RELATED LINKS</span></span>

