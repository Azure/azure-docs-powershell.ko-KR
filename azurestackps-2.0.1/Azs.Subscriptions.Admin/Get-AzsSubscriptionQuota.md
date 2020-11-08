---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azssubscriptionquota
schema: 2.0.0
ms.openlocfilehash: 8e1c03393c1d276f5c93425250bf7202e49022d8
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94045257"
---
# <span data-ttu-id="73062-101">Get-AzsSubscriptionQuota</span><span class="sxs-lookup"><span data-stu-id="73062-101">Get-AzsSubscriptionQuota</span></span>

## <span data-ttu-id="73062-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73062-102">SYNOPSIS</span></span>
<span data-ttu-id="73062-103">할당량을 이름별로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="73062-103">Gets a quota by name.</span></span>

## <span data-ttu-id="73062-104">구문과</span><span class="sxs-lookup"><span data-stu-id="73062-104">SYNTAX</span></span>

### <span data-ttu-id="73062-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="73062-105">List (Default)</span></span>
```
Get-AzsSubscriptionQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="73062-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="73062-106">Get</span></span>
```
Get-AzsSubscriptionQuota -Quota <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="73062-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="73062-107">GetViaIdentity</span></span>
```
Get-AzsSubscriptionQuota -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="73062-108">설명은</span><span class="sxs-lookup"><span data-stu-id="73062-108">DESCRIPTION</span></span>
<span data-ttu-id="73062-109">할당량을 이름별로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="73062-109">Gets a quota by name.</span></span>

## <span data-ttu-id="73062-110">예제의</span><span class="sxs-lookup"><span data-stu-id="73062-110">EXAMPLES</span></span>

### <span data-ttu-id="73062-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="73062-111">Example 1</span></span>
```powershell

```

<span data-ttu-id="73062-112">구독 리소스 공급자 할당량 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="73062-112">Get the list of subscription resource provider quotas.</span></span>

## <span data-ttu-id="73062-113">변수</span><span class="sxs-lookup"><span data-stu-id="73062-113">PARAMETERS</span></span>

### <span data-ttu-id="73062-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73062-114">-DefaultProfile</span></span>
<span data-ttu-id="73062-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="73062-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73062-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73062-116">-InputObject</span></span>
<span data-ttu-id="73062-117">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73062-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="73062-118">-위치</span><span class="sxs-lookup"><span data-stu-id="73062-118">-Location</span></span>
<span data-ttu-id="73062-119">AzureStack 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="73062-119">The AzureStack location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="73062-120">-할당량</span><span class="sxs-lookup"><span data-stu-id="73062-120">-Quota</span></span>
<span data-ttu-id="73062-121">할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73062-121">Name of the quota.</span></span>

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

### <span data-ttu-id="73062-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="73062-122">-SubscriptionId</span></span>
<span data-ttu-id="73062-123">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="73062-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="73062-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73062-124">CommonParameters</span></span>
<span data-ttu-id="73062-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="73062-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73062-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="73062-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73062-127">입력</span><span class="sxs-lookup"><span data-stu-id="73062-127">INPUTS</span></span>

### <span data-ttu-id="73062-128">SubscriptionsAdmin. ISubscriptionsAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="73062-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="73062-129">출력</span><span class="sxs-lookup"><span data-stu-id="73062-129">OUTPUTS</span></span>

### <span data-ttu-id="73062-130">SubscriptionsAdmin (Api20151101)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73062-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IQuota</span></span>

<span data-ttu-id="73062-131">별칭과</span><span class="sxs-lookup"><span data-stu-id="73062-131">ALIASES</span></span>

<span data-ttu-id="73062-132">Get-AzsSubscriptionsQuota</span><span class="sxs-lookup"><span data-stu-id="73062-132">Get-AzsSubscriptionsQuota</span></span>

## <span data-ttu-id="73062-133">상속자</span><span class="sxs-lookup"><span data-stu-id="73062-133">NOTES</span></span>

<span data-ttu-id="73062-134">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="73062-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="73062-135">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="73062-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="73062-136">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="73062-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="73062-137">`[DelegatedProvider <String>]`: DelegatedProvider 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="73062-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="73062-138">`[DelegatedProviderSubscriptionId <String>]`: 위임 된 공급자 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="73062-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="73062-139">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="73062-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="73062-140">`[Location <String>]`: AzureStack 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="73062-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="73062-141">`[ManifestName <String>]`: 매니페스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73062-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="73062-142">`[Offer <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73062-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="73062-143">`[OfferDelegationName <String>]`: 제안 위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73062-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="73062-144">`[OperationsStatusName <String>]`: 작업 상태 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73062-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="73062-145">`[Plan <String>]`: 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73062-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="73062-146">`[PlanAcquisitionId <String>]`: 계획 획득 식별자</span><span class="sxs-lookup"><span data-stu-id="73062-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="73062-147">`[Quota <String>]`: 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73062-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="73062-148">`[ResourceGroupName <String>]`: 리소스 그룹이 아래에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73062-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="73062-149">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="73062-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="73062-150">`[TargetSubscriptionId <String>]`: 대상 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="73062-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="73062-151">`[Tenant <String>]`: 디렉터리 테 넌 트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73062-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="73062-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="73062-152">RELATED LINKS</span></span>

