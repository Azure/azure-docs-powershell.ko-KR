---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdirectorytenant
schema: 2.0.0
ms.openlocfilehash: f516562b6bc4a136c64a15fa1f128cd1bda502d9
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/22/2020
ms.locfileid: "94045132"
---
# <span data-ttu-id="627d2-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="627d2-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="627d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="627d2-102">SYNOPSIS</span></span>
<span data-ttu-id="627d2-103">이름으로 디렉터리 테 넌 트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="627d2-103">Get a directory tenant by name.</span></span>

## <span data-ttu-id="627d2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="627d2-104">SYNTAX</span></span>

### <span data-ttu-id="627d2-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="627d2-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="627d2-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="627d2-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="627d2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="627d2-107">GetViaIdentity</span></span>
```
Get-AzsDirectoryTenant -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="627d2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="627d2-108">DESCRIPTION</span></span>
<span data-ttu-id="627d2-109">이름으로 디렉터리 테 넌 트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="627d2-109">Get a directory tenant by name.</span></span>

## <span data-ttu-id="627d2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="627d2-110">EXAMPLES</span></span>

### <span data-ttu-id="627d2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="627d2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDirectoryTenant -ResourceGroupName 'system.redmond'

Location Name                           Type                                          
-------- ----                           ----                                          
redmond  azurestack01.onmicrosoft.com Microsoft.Subscriptions.Admin/directoryTenants
redmond  azurestack02.onmicrosoft.com Microsoft.Subscriptions.Admin/directoryTenants
```

<span data-ttu-id="627d2-112">현재 구독 및 지정 된 리소스 그룹 이름 아래에 있는 모든 디렉터리 테 넌 트를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="627d2-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="627d2-113">변수</span><span class="sxs-lookup"><span data-stu-id="627d2-113">PARAMETERS</span></span>

### <span data-ttu-id="627d2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="627d2-114">-DefaultProfile</span></span>
<span data-ttu-id="627d2-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="627d2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="627d2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="627d2-116">-InputObject</span></span>
<span data-ttu-id="627d2-117">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="627d2-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="627d2-118">-이름</span><span class="sxs-lookup"><span data-stu-id="627d2-118">-Name</span></span>
<span data-ttu-id="627d2-119">디렉터리 테 넌 트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="627d2-119">Directory tenant name.</span></span>

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

### <span data-ttu-id="627d2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="627d2-120">-ResourceGroupName</span></span>
<span data-ttu-id="627d2-121">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="627d2-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="627d2-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="627d2-122">-SubscriptionId</span></span>
<span data-ttu-id="627d2-123">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="627d2-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="627d2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="627d2-124">CommonParameters</span></span>
<span data-ttu-id="627d2-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="627d2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="627d2-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="627d2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="627d2-127">입력</span><span class="sxs-lookup"><span data-stu-id="627d2-127">INPUTS</span></span>

### <span data-ttu-id="627d2-128">SubscriptionsAdmin. ISubscriptionsAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="627d2-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="627d2-129">출력</span><span class="sxs-lookup"><span data-stu-id="627d2-129">OUTPUTS</span></span>

### <span data-ttu-id="627d2-130">SubscriptionsAdmin. PowerShell. Api20151101. IDirectoryTenant 넌 트</span><span class="sxs-lookup"><span data-stu-id="627d2-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IDirectoryTenant</span></span>

<span data-ttu-id="627d2-131">별칭과</span><span class="sxs-lookup"><span data-stu-id="627d2-131">ALIASES</span></span>

## <span data-ttu-id="627d2-132">상속자</span><span class="sxs-lookup"><span data-stu-id="627d2-132">NOTES</span></span>

<span data-ttu-id="627d2-133">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="627d2-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="627d2-134">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="627d2-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="627d2-135">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="627d2-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="627d2-136">`[DelegatedProvider <String>]`: DelegatedProvider 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="627d2-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="627d2-137">`[DelegatedProviderSubscriptionId <String>]`: 위임 된 공급자 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="627d2-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="627d2-138">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="627d2-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="627d2-139">`[Location <String>]`: AzureStack 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="627d2-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="627d2-140">`[ManifestName <String>]`: 매니페스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="627d2-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="627d2-141">`[Offer <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="627d2-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="627d2-142">`[OfferDelegationName <String>]`: 제안 위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="627d2-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="627d2-143">`[OperationsStatusName <String>]`: 작업 상태 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="627d2-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="627d2-144">`[Plan <String>]`: 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="627d2-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="627d2-145">`[PlanAcquisitionId <String>]`: 계획 획득 식별자</span><span class="sxs-lookup"><span data-stu-id="627d2-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="627d2-146">`[Quota <String>]`: 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="627d2-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="627d2-147">`[ResourceGroupName <String>]`: 리소스 그룹이 아래에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="627d2-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="627d2-148">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="627d2-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="627d2-149">`[TargetSubscriptionId <String>]`: 대상 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="627d2-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="627d2-150">`[Tenant <String>]`: 디렉터리 테 넌 트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="627d2-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="627d2-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="627d2-151">RELATED LINKS</span></span>

