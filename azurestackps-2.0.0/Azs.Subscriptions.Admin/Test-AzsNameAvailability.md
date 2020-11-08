---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/test-azsnameavailability
schema: 2.0.0
ms.openlocfilehash: d92c2558375a180c96ff20260977bdb38908fa61
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/22/2020
ms.locfileid: "94045098"
---
# <span data-ttu-id="452df-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="452df-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="452df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="452df-102">SYNOPSIS</span></span>
<span data-ttu-id="452df-103">구독 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="452df-103">Get the list of subscriptions.</span></span>

## <span data-ttu-id="452df-104">구문과</span><span class="sxs-lookup"><span data-stu-id="452df-104">SYNTAX</span></span>

### <span data-ttu-id="452df-105">CheckExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="452df-105">CheckExpanded (Default)</span></span>
```
Test-AzsNameAvailability [-SubscriptionId <String>] [-Name <String>] [-ResourceType <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="452df-106">검사가</span><span class="sxs-lookup"><span data-stu-id="452df-106">Check</span></span>
```
Test-AzsNameAvailability -NameAvailabilityDefinition <ICheckNameAvailabilityDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="452df-107">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="452df-107">CheckViaIdentity</span></span>
```
Test-AzsNameAvailability -InputObject <ISubscriptionsAdminIdentity>
 -NameAvailabilityDefinition <ICheckNameAvailabilityDefinition> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="452df-108">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="452df-108">CheckViaIdentityExpanded</span></span>
```
Test-AzsNameAvailability -InputObject <ISubscriptionsAdminIdentity> [-Name <String>] [-ResourceType <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="452df-109">설명은</span><span class="sxs-lookup"><span data-stu-id="452df-109">DESCRIPTION</span></span>
<span data-ttu-id="452df-110">구독 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="452df-110">Get the list of subscriptions.</span></span>

## <span data-ttu-id="452df-111">예제의</span><span class="sxs-lookup"><span data-stu-id="452df-111">EXAMPLES</span></span>

### <span data-ttu-id="452df-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="452df-112">Example 1</span></span>
```powershell
PS C:\> Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name "testoffer" | fl *

Message       : A resource of type 'Microsoft.Subscriptions.Admin/offers' with name 'testoffer' already exists. Please select a different name.
NameAvailable : False
Reason        : AlreadyExists
```

<span data-ttu-id="452df-113">지정 된 구독 리소스 종류 및 이름 사용 가능 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="452df-113">Returns the availability of the specified subscription resource type and name</span></span>

## <span data-ttu-id="452df-114">변수</span><span class="sxs-lookup"><span data-stu-id="452df-114">PARAMETERS</span></span>

### <span data-ttu-id="452df-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="452df-115">-DefaultProfile</span></span>
<span data-ttu-id="452df-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="452df-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="452df-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="452df-117">-InputObject</span></span>
<span data-ttu-id="452df-118">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="452df-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: CheckViaIdentity, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="452df-119">-이름</span><span class="sxs-lookup"><span data-stu-id="452df-119">-Name</span></span>
<span data-ttu-id="452df-120">확인할 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="452df-120">The resource name to verify.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="452df-121">-NameAvailabilityDefinition</span><span class="sxs-lookup"><span data-stu-id="452df-121">-NameAvailabilityDefinition</span></span>
<span data-ttu-id="452df-122">이름 사용 가능성 확인 작업 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="452df-122">The check name availability action definition.</span></span>
<span data-ttu-id="452df-123">생성 하려면 NAMEAVAILABILITYDEFINITION 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="452df-123">To construct, see NOTES section for NAMEAVAILABILITYDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityDefinition
Parameter Sets: Check, CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="452df-124">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="452df-124">-ResourceType</span></span>
<span data-ttu-id="452df-125">확인할 리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="452df-125">The resource type to verify.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="452df-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="452df-126">-SubscriptionId</span></span>
<span data-ttu-id="452df-127">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="452df-127">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="452df-128">-확인</span><span class="sxs-lookup"><span data-stu-id="452df-128">-Confirm</span></span>
<span data-ttu-id="452df-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="452df-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="452df-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="452df-130">-WhatIf</span></span>
<span data-ttu-id="452df-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="452df-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="452df-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="452df-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="452df-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="452df-133">CommonParameters</span></span>
<span data-ttu-id="452df-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="452df-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="452df-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="452df-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="452df-136">입력</span><span class="sxs-lookup"><span data-stu-id="452df-136">INPUTS</span></span>

### <span data-ttu-id="452df-137">SubscriptionsAdmin. Api20151101. ICheckNameAvailabilityDefinition에 대 한</span><span class="sxs-lookup"><span data-stu-id="452df-137">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityDefinition</span></span>

### <span data-ttu-id="452df-138">SubscriptionsAdmin. ISubscriptionsAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="452df-138">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="452df-139">출력</span><span class="sxs-lookup"><span data-stu-id="452df-139">OUTPUTS</span></span>

### <span data-ttu-id="452df-140">SubscriptionsAdmin. Api20151101. ICheckNameAvailabilityResponse에 대 한</span><span class="sxs-lookup"><span data-stu-id="452df-140">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityResponse</span></span>

<span data-ttu-id="452df-141">별칭과</span><span class="sxs-lookup"><span data-stu-id="452df-141">ALIASES</span></span>

## <span data-ttu-id="452df-142">상속자</span><span class="sxs-lookup"><span data-stu-id="452df-142">NOTES</span></span>

<span data-ttu-id="452df-143">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="452df-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="452df-144">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="452df-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="452df-145">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="452df-145">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="452df-146">`[DelegatedProvider <String>]`: DelegatedProvider 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="452df-146">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="452df-147">`[DelegatedProviderSubscriptionId <String>]`: 위임 된 공급자 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="452df-147">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="452df-148">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="452df-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="452df-149">`[Location <String>]`: AzureStack 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="452df-149">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="452df-150">`[ManifestName <String>]`: 매니페스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="452df-150">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="452df-151">`[Offer <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="452df-151">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="452df-152">`[OfferDelegationName <String>]`: 제안 위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="452df-152">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="452df-153">`[OperationsStatusName <String>]`: 작업 상태 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="452df-153">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="452df-154">`[Plan <String>]`: 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="452df-154">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="452df-155">`[PlanAcquisitionId <String>]`: 계획 획득 식별자</span><span class="sxs-lookup"><span data-stu-id="452df-155">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="452df-156">`[Quota <String>]`: 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="452df-156">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="452df-157">`[ResourceGroupName <String>]`: 리소스 그룹이 아래에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="452df-157">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="452df-158">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="452df-158">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="452df-159">`[TargetSubscriptionId <String>]`: 대상 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="452df-159">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="452df-160">`[Tenant <String>]`: 디렉터리 테 넌 트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="452df-160">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="452df-161">NAMEAVAILABILITYDEFINITION <ICheckNameAvailabilityDefinition> : 이름 사용 가능성 확인 작업 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="452df-161">NAMEAVAILABILITYDEFINITION <ICheckNameAvailabilityDefinition>: The check name availability action definition.</span></span>
  - <span data-ttu-id="452df-162">`[Name <String>]`: 확인할 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="452df-162">`[Name <String>]`: The resource name to verify.</span></span>
  - <span data-ttu-id="452df-163">`[ResourceType <String>]`: 확인할 리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="452df-163">`[ResourceType <String>]`: The resource type to verify.</span></span>

## <span data-ttu-id="452df-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="452df-164">RELATED LINKS</span></span>

