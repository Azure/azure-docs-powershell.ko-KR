---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: a36406499be15c53e9bfabd8aa9abf56b2afa1c7
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94045339"
---
# <span data-ttu-id="813e7-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="813e7-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="813e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="813e7-102">SYNOPSIS</span></span>
<span data-ttu-id="813e7-103">지정 된 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="813e7-103">Get a specified subscription.</span></span>

## <span data-ttu-id="813e7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="813e7-104">SYNTAX</span></span>

### <span data-ttu-id="813e7-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="813e7-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="813e7-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="813e7-106">Get</span></span>
```
Get-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="813e7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="813e7-107">GetViaIdentity</span></span>
```
Get-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="813e7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="813e7-108">DESCRIPTION</span></span>
<span data-ttu-id="813e7-109">지정 된 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="813e7-109">Get a specified subscription.</span></span>

## <span data-ttu-id="813e7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="813e7-110">EXAMPLES</span></span>

### <span data-ttu-id="813e7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="813e7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsUserSubscription | Select-Object -First 1 | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : DRPTestffbffbe5-test-test-test-test-test-test
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ffbffbe5-8905-4f51-b2ed-4717049de782
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Owner                           : user@microsoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ffbffbe5-8905-4f51-b2ed-4717049de782
TenantId                        : 76440dfb-c97c-4fee-8f6c-dff8ddbe816f
```

<span data-ttu-id="813e7-112">사용자 구독 목록을 교환원으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="813e7-112">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="813e7-113">변수</span><span class="sxs-lookup"><span data-stu-id="813e7-113">PARAMETERS</span></span>

### <span data-ttu-id="813e7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="813e7-114">-DefaultProfile</span></span>
<span data-ttu-id="813e7-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="813e7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="813e7-116">-필터</span><span class="sxs-lookup"><span data-stu-id="813e7-116">-Filter</span></span>
<span data-ttu-id="813e7-117">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="813e7-117">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="813e7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="813e7-118">-InputObject</span></span>
<span data-ttu-id="813e7-119">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="813e7-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="813e7-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="813e7-120">-SubscriptionId</span></span>
<span data-ttu-id="813e7-121">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="813e7-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="813e7-122">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="813e7-122">-TargetSubscriptionId</span></span>
<span data-ttu-id="813e7-123">대상 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="813e7-123">The target subscription ID.</span></span>

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

### <span data-ttu-id="813e7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="813e7-124">CommonParameters</span></span>
<span data-ttu-id="813e7-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="813e7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="813e7-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="813e7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="813e7-127">입력</span><span class="sxs-lookup"><span data-stu-id="813e7-127">INPUTS</span></span>

### <span data-ttu-id="813e7-128">SubscriptionsAdmin. ISubscriptionsAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="813e7-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="813e7-129">출력</span><span class="sxs-lookup"><span data-stu-id="813e7-129">OUTPUTS</span></span>

### <span data-ttu-id="813e7-130">SubscriptionsAdmin. Api20151101. i a PowerShell. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="813e7-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="813e7-131">별칭과</span><span class="sxs-lookup"><span data-stu-id="813e7-131">ALIASES</span></span>

## <span data-ttu-id="813e7-132">상속자</span><span class="sxs-lookup"><span data-stu-id="813e7-132">NOTES</span></span>

<span data-ttu-id="813e7-133">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="813e7-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="813e7-134">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="813e7-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="813e7-135">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="813e7-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="813e7-136">`[DelegatedProvider <String>]`: DelegatedProvider 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="813e7-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="813e7-137">`[DelegatedProviderSubscriptionId <String>]`: 위임 된 공급자 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="813e7-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="813e7-138">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="813e7-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="813e7-139">`[Location <String>]`: AzureStack 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="813e7-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="813e7-140">`[ManifestName <String>]`: 매니페스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="813e7-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="813e7-141">`[Offer <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="813e7-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="813e7-142">`[OfferDelegationName <String>]`: 제안 위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="813e7-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="813e7-143">`[OperationsStatusName <String>]`: 작업 상태 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="813e7-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="813e7-144">`[Plan <String>]`: 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="813e7-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="813e7-145">`[PlanAcquisitionId <String>]`: 계획 획득 식별자</span><span class="sxs-lookup"><span data-stu-id="813e7-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="813e7-146">`[Quota <String>]`: 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="813e7-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="813e7-147">`[ResourceGroupName <String>]`: 리소스 그룹이 아래에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="813e7-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="813e7-148">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="813e7-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="813e7-149">`[TargetSubscriptionId <String>]`: 대상 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="813e7-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="813e7-150">`[Tenant <String>]`: 디렉터리 테 넌 트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="813e7-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="813e7-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="813e7-151">RELATED LINKS</span></span>

