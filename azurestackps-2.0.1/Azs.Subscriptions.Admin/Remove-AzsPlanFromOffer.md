---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsplanfromoffer
schema: 2.0.0
ms.openlocfilehash: c3a68c028abc9033cef9d9fd7e8fbd39e4066d2d
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94045200"
---
# <span data-ttu-id="bac50-101">Remove-AzsPlanFromOffer</span><span class="sxs-lookup"><span data-stu-id="bac50-101">Remove-AzsPlanFromOffer</span></span>

## <span data-ttu-id="bac50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bac50-102">SYNOPSIS</span></span>
<span data-ttu-id="bac50-103">제안에서 계획의 연결을 끊습니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-103">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="bac50-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bac50-104">SYNTAX</span></span>

### <span data-ttu-id="bac50-105">링크 해제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="bac50-105">UnlinkExpanded (Default)</span></span>
```
Remove-AzsPlanFromOffer -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaxAcquisitionCount <Int32>] [-PlanLinkType <PlanLinkType>] [-PlanName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bac50-106">끊어야</span><span class="sxs-lookup"><span data-stu-id="bac50-106">Unlink</span></span>
```
Remove-AzsPlanFromOffer -OfferName <String> -ResourceGroupName <String> -PlanLink <IPlanLinkDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bac50-107">UnlinkViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bac50-107">UnlinkViaIdentity</span></span>
```
Remove-AzsPlanFromOffer -InputObject <ISubscriptionsAdminIdentity> -PlanLink <IPlanLinkDefinition>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bac50-108">UnlinkViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="bac50-108">UnlinkViaIdentityExpanded</span></span>
```
Remove-AzsPlanFromOffer -InputObject <ISubscriptionsAdminIdentity> [-MaxAcquisitionCount <Int32>]
 [-PlanLinkType <PlanLinkType>] [-PlanName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="bac50-109">설명은</span><span class="sxs-lookup"><span data-stu-id="bac50-109">DESCRIPTION</span></span>
<span data-ttu-id="bac50-110">제안에서 계획의 연결을 끊습니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-110">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="bac50-111">예제의</span><span class="sxs-lookup"><span data-stu-id="bac50-111">EXAMPLES</span></span>

### <span data-ttu-id="bac50-112">예제 1:</span><span class="sxs-lookup"><span data-stu-id="bac50-112">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsPlanFromOffer -PlanName "testplan" -PlanLinkType Addon -OfferName "testoffer" -ResourceGroupName "testrg"

```

<span data-ttu-id="bac50-113">제안에서 계획의 연결을 끊습니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-113">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="bac50-114">변수</span><span class="sxs-lookup"><span data-stu-id="bac50-114">PARAMETERS</span></span>

### <span data-ttu-id="bac50-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bac50-115">-DefaultProfile</span></span>
<span data-ttu-id="bac50-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bac50-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bac50-117">-InputObject</span></span>
<span data-ttu-id="bac50-118">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: UnlinkViaIdentity, UnlinkViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="bac50-119">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="bac50-119">-MaxAcquisitionCount</span></span>
<span data-ttu-id="bac50-120">구독자 별 최대 획득 수</span><span class="sxs-lookup"><span data-stu-id="bac50-120">The maximum acquisition count by subscribers</span></span>

```yaml
Type: System.Int32
Parameter Sets: UnlinkExpanded, UnlinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bac50-121">-OfferName</span><span class="sxs-lookup"><span data-stu-id="bac50-121">-OfferName</span></span>
<span data-ttu-id="bac50-122">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-122">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Unlink, UnlinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bac50-123">-계획 링크</span><span class="sxs-lookup"><span data-stu-id="bac50-123">-PlanLink</span></span>
<span data-ttu-id="bac50-124">계획을 제공에 연결 하 고 연결을 끊는 방법에 대 한 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-124">Definition for linking and unlinking plans to offers.</span></span>
<span data-ttu-id="bac50-125">생성 하려면 계획 링크 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-125">To construct, see NOTES section for PLANLINK properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition
Parameter Sets: Unlink, UnlinkViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="bac50-126">-계획 Linktype</span><span class="sxs-lookup"><span data-stu-id="bac50-126">-PlanLinkType</span></span>
<span data-ttu-id="bac50-127">계획 링크의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-127">Type of the plan link.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.PlanLinkType
Parameter Sets: UnlinkExpanded, UnlinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bac50-128">-계획 이름</span><span class="sxs-lookup"><span data-stu-id="bac50-128">-PlanName</span></span>
<span data-ttu-id="bac50-129">계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-129">Name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: UnlinkExpanded, UnlinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bac50-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bac50-130">-ResourceGroupName</span></span>
<span data-ttu-id="bac50-131">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-131">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Unlink, UnlinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bac50-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bac50-132">-SubscriptionId</span></span>
<span data-ttu-id="bac50-133">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-133">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Unlink, UnlinkExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bac50-134">-확인</span><span class="sxs-lookup"><span data-stu-id="bac50-134">-Confirm</span></span>
<span data-ttu-id="bac50-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bac50-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bac50-136">-WhatIf</span></span>
<span data-ttu-id="bac50-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bac50-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bac50-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bac50-139">CommonParameters</span></span>
<span data-ttu-id="bac50-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bac50-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bac50-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bac50-142">입력</span><span class="sxs-lookup"><span data-stu-id="bac50-142">INPUTS</span></span>

### <span data-ttu-id="bac50-143">SubscriptionsAdmin. PowerShell. Api20151101. I계획 Linkdefinition</span><span class="sxs-lookup"><span data-stu-id="bac50-143">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition</span></span>

### <span data-ttu-id="bac50-144">SubscriptionsAdmin. ISubscriptionsAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="bac50-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="bac50-145">출력</span><span class="sxs-lookup"><span data-stu-id="bac50-145">OUTPUTS</span></span>

### <span data-ttu-id="bac50-146">SubscriptionsAdmin. Api20151101. i a i.</span><span class="sxs-lookup"><span data-stu-id="bac50-146">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="bac50-147">별칭과</span><span class="sxs-lookup"><span data-stu-id="bac50-147">ALIASES</span></span>

## <span data-ttu-id="bac50-148">상속자</span><span class="sxs-lookup"><span data-stu-id="bac50-148">NOTES</span></span>

<span data-ttu-id="bac50-149">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bac50-150">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="bac50-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="bac50-151">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="bac50-151">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bac50-152">`[DelegatedProvider <String>]`: DelegatedProvider 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-152">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="bac50-153">`[DelegatedProviderSubscriptionId <String>]`: 위임 된 공급자 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-153">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="bac50-154">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="bac50-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bac50-155">`[Location <String>]`: AzureStack 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-155">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="bac50-156">`[ManifestName <String>]`: 매니페스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-156">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="bac50-157">`[Offer <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-157">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="bac50-158">`[OfferDelegationName <String>]`: 제안 위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-158">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="bac50-159">`[OperationsStatusName <String>]`: 작업 상태 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-159">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="bac50-160">`[Plan <String>]`: 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-160">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="bac50-161">`[PlanAcquisitionId <String>]`: 계획 획득 식별자</span><span class="sxs-lookup"><span data-stu-id="bac50-161">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="bac50-162">`[Quota <String>]`: 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-162">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="bac50-163">`[ResourceGroupName <String>]`: 리소스 그룹이 아래에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-163">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="bac50-164">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-164">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="bac50-165">`[TargetSubscriptionId <String>]`: 대상 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-165">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="bac50-166">`[Tenant <String>]`: 디렉터리 테 넌 트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-166">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="bac50-167">계획 링크 <IPlanLinkDefinition> : 플랜을 제공에 연결 하 고 링크를 해제 하기 위한 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-167">PLANLINK <IPlanLinkDefinition>: Definition for linking and unlinking plans to offers.</span></span>
  - <span data-ttu-id="bac50-168">`[MaxAcquisitionCount <Int32?>]`: 구독자 별 최대 획득 수</span><span class="sxs-lookup"><span data-stu-id="bac50-168">`[MaxAcquisitionCount <Int32?>]`: The maximum acquisition count by subscribers</span></span>
  - <span data-ttu-id="bac50-169">`[PlanLinkType <PlanLinkType?>]`: 계획 링크의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-169">`[PlanLinkType <PlanLinkType?>]`: Type of the plan link.</span></span>
  - <span data-ttu-id="bac50-170">`[PlanName <String>]`: 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bac50-170">`[PlanName <String>]`: Name of the plan.</span></span>

## <span data-ttu-id="bac50-171">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bac50-171">RELATED LINKS</span></span>

