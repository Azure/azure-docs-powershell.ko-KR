---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: c73a4c4bcc482b7e6e1281d0bc4ee6c29921b745
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94047156"
---
# <span data-ttu-id="12bff-101">Get-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="12bff-101">Get-AzsAcquiredPlan</span></span>

## <span data-ttu-id="12bff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12bff-102">SYNOPSIS</span></span>
<span data-ttu-id="12bff-103">제안을 소모 하는 구독에서 획득 한 지정 된 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="12bff-103">Gets the specified plan acquired by a subscription consuming the offer.</span></span>

## <span data-ttu-id="12bff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="12bff-104">SYNTAX</span></span>

### <span data-ttu-id="12bff-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="12bff-105">List (Default)</span></span>
```
Get-AzsAcquiredPlan -TargetSubscriptionId <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="12bff-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="12bff-106">Get</span></span>
```
Get-AzsAcquiredPlan -PlanAcquisitionId <String> -TargetSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="12bff-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="12bff-107">GetViaIdentity</span></span>
```
Get-AzsAcquiredPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="12bff-108">설명은</span><span class="sxs-lookup"><span data-stu-id="12bff-108">DESCRIPTION</span></span>
<span data-ttu-id="12bff-109">제안을 소모 하는 구독에서 획득 한 지정 된 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="12bff-109">Gets the specified plan acquired by a subscription consuming the offer.</span></span>

## <span data-ttu-id="12bff-110">예제의</span><span class="sxs-lookup"><span data-stu-id="12bff-110">EXAMPLES</span></span>

### <span data-ttu-id="12bff-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="12bff-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsAcquiredPlan -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

AcquisitionId       : 718c7f7c-4868-479a-98ce-5caaa8f158c1
AcquisitionTime     : 3/12/2020 11:16:08 PM
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/acquiredPlan
                      s/718c7f7c-4868-479a-98ce-5caaa8f158c1
PlanId              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/plans/testplan
ProvisioningState   : Succeeded
```

<span data-ttu-id="12bff-112">구독에서 액세스할 수 있는 모든 확보 된 계획의 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="12bff-112">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="12bff-113">변수</span><span class="sxs-lookup"><span data-stu-id="12bff-113">PARAMETERS</span></span>

### <span data-ttu-id="12bff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12bff-114">-DefaultProfile</span></span>
<span data-ttu-id="12bff-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="12bff-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12bff-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12bff-116">-InputObject</span></span>
<span data-ttu-id="12bff-117">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="12bff-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="12bff-118">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="12bff-118">-PlanAcquisitionId</span></span>
<span data-ttu-id="12bff-119">계획 획득 식별자</span><span class="sxs-lookup"><span data-stu-id="12bff-119">The plan acquisition Identifier</span></span>

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

### <span data-ttu-id="12bff-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="12bff-120">-SubscriptionId</span></span>
<span data-ttu-id="12bff-121">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="12bff-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="12bff-122">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="12bff-122">-TargetSubscriptionId</span></span>
<span data-ttu-id="12bff-123">대상 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="12bff-123">The target subscription ID.</span></span>

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

### <span data-ttu-id="12bff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12bff-124">CommonParameters</span></span>
<span data-ttu-id="12bff-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="12bff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12bff-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="12bff-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12bff-127">입력</span><span class="sxs-lookup"><span data-stu-id="12bff-127">INPUTS</span></span>

### <span data-ttu-id="12bff-128">SubscriptionsAdmin. ISubscriptionsAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="12bff-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="12bff-129">출력</span><span class="sxs-lookup"><span data-stu-id="12bff-129">OUTPUTS</span></span>

### <span data-ttu-id="12bff-130">SubscriptionsAdmin. PowerShell. Api20151101. I계획 취득</span><span class="sxs-lookup"><span data-stu-id="12bff-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

<span data-ttu-id="12bff-131">별칭과</span><span class="sxs-lookup"><span data-stu-id="12bff-131">ALIASES</span></span>

<span data-ttu-id="12bff-132">Get-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="12bff-132">Get-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="12bff-133">상속자</span><span class="sxs-lookup"><span data-stu-id="12bff-133">NOTES</span></span>

<span data-ttu-id="12bff-134">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="12bff-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="12bff-135">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="12bff-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="12bff-136">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="12bff-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="12bff-137">`[DelegatedProvider <String>]`: DelegatedProvider 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="12bff-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="12bff-138">`[DelegatedProviderSubscriptionId <String>]`: 위임 된 공급자 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="12bff-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="12bff-139">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="12bff-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="12bff-140">`[Location <String>]`: AzureStack 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="12bff-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="12bff-141">`[ManifestName <String>]`: 매니페스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="12bff-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="12bff-142">`[Offer <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="12bff-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="12bff-143">`[OfferDelegationName <String>]`: 제안 위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="12bff-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="12bff-144">`[OperationsStatusName <String>]`: 작업 상태 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="12bff-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="12bff-145">`[Plan <String>]`: 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="12bff-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="12bff-146">`[PlanAcquisitionId <String>]`: 계획 획득 식별자</span><span class="sxs-lookup"><span data-stu-id="12bff-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="12bff-147">`[Quota <String>]`: 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="12bff-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="12bff-148">`[ResourceGroupName <String>]`: 리소스 그룹이 아래에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="12bff-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="12bff-149">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="12bff-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="12bff-150">`[TargetSubscriptionId <String>]`: 대상 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="12bff-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="12bff-151">`[Tenant <String>]`: 디렉터리 테 넌 트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="12bff-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="12bff-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="12bff-152">RELATED LINKS</span></span>

