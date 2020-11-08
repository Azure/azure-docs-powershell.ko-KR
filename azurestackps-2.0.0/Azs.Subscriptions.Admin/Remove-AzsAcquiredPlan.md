---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: 80a4353497d0c7894a8c0ac4d95e57e56a6211a1
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/22/2020
ms.locfileid: "94045113"
---
# <span data-ttu-id="7efa0-101">Remove-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="7efa0-101">Remove-AzsAcquiredPlan</span></span>

## <span data-ttu-id="7efa0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7efa0-102">SYNOPSIS</span></span>
<span data-ttu-id="7efa0-103">확보 된 계획을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7efa0-103">Deletes an acquired plan.</span></span>

## <span data-ttu-id="7efa0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7efa0-104">SYNTAX</span></span>

### <span data-ttu-id="7efa0-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="7efa0-105">Delete (Default)</span></span>
```
Remove-AzsAcquiredPlan -PlanAcquisitionId <String> -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7efa0-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7efa0-106">DeleteViaIdentity</span></span>
```
Remove-AzsAcquiredPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7efa0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7efa0-107">DESCRIPTION</span></span>
<span data-ttu-id="7efa0-108">확보 된 계획을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7efa0-108">Deletes an acquired plan.</span></span>

## <span data-ttu-id="7efa0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7efa0-109">EXAMPLES</span></span>

### <span data-ttu-id="7efa0-110">예제 1:</span><span class="sxs-lookup"><span data-stu-id="7efa0-110">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsAcquiredPlan -PlanAcquisitionId "718c7f7c-4868-479a-98ce-5caaa8f158c2" -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

```

<span data-ttu-id="7efa0-111">확보 된 계획을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7efa0-111">Delete an acquired plan.</span></span>

## <span data-ttu-id="7efa0-112">변수</span><span class="sxs-lookup"><span data-stu-id="7efa0-112">PARAMETERS</span></span>

### <span data-ttu-id="7efa0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7efa0-113">-DefaultProfile</span></span>
<span data-ttu-id="7efa0-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7efa0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7efa0-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7efa0-115">-InputObject</span></span>
<span data-ttu-id="7efa0-116">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7efa0-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="7efa0-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7efa0-117">-PassThru</span></span>
<span data-ttu-id="7efa0-118">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7efa0-118">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7efa0-119">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="7efa0-119">-PlanAcquisitionId</span></span>
<span data-ttu-id="7efa0-120">계획 획득 식별자</span><span class="sxs-lookup"><span data-stu-id="7efa0-120">The plan acquisition Identifier</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7efa0-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7efa0-121">-SubscriptionId</span></span>
<span data-ttu-id="7efa0-122">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7efa0-122">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7efa0-123">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7efa0-123">-TargetSubscriptionId</span></span>
<span data-ttu-id="7efa0-124">대상 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7efa0-124">The target subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7efa0-125">-확인</span><span class="sxs-lookup"><span data-stu-id="7efa0-125">-Confirm</span></span>
<span data-ttu-id="7efa0-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7efa0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7efa0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7efa0-127">-WhatIf</span></span>
<span data-ttu-id="7efa0-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7efa0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7efa0-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7efa0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7efa0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7efa0-130">CommonParameters</span></span>
<span data-ttu-id="7efa0-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7efa0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7efa0-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7efa0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7efa0-133">입력</span><span class="sxs-lookup"><span data-stu-id="7efa0-133">INPUTS</span></span>

### <span data-ttu-id="7efa0-134">SubscriptionsAdmin. ISubscriptionsAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="7efa0-134">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="7efa0-135">출력</span><span class="sxs-lookup"><span data-stu-id="7efa0-135">OUTPUTS</span></span>

### <span data-ttu-id="7efa0-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="7efa0-136">System.Boolean</span></span>

<span data-ttu-id="7efa0-137">별칭과</span><span class="sxs-lookup"><span data-stu-id="7efa0-137">ALIASES</span></span>

### <span data-ttu-id="7efa0-138">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="7efa0-138">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="7efa0-139">상속자</span><span class="sxs-lookup"><span data-stu-id="7efa0-139">NOTES</span></span>

<span data-ttu-id="7efa0-140">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7efa0-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7efa0-141">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="7efa0-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="7efa0-142">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7efa0-142">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7efa0-143">`[DelegatedProvider <String>]`: DelegatedProvider 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7efa0-143">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="7efa0-144">`[DelegatedProviderSubscriptionId <String>]`: 위임 된 공급자 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7efa0-144">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="7efa0-145">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="7efa0-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7efa0-146">`[Location <String>]`: AzureStack 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="7efa0-146">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="7efa0-147">`[ManifestName <String>]`: 매니페스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7efa0-147">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="7efa0-148">`[Offer <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7efa0-148">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="7efa0-149">`[OfferDelegationName <String>]`: 제안 위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7efa0-149">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="7efa0-150">`[OperationsStatusName <String>]`: 작업 상태 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7efa0-150">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="7efa0-151">`[Plan <String>]`: 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7efa0-151">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="7efa0-152">`[PlanAcquisitionId <String>]`: 계획 획득 식별자</span><span class="sxs-lookup"><span data-stu-id="7efa0-152">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="7efa0-153">`[Quota <String>]`: 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7efa0-153">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="7efa0-154">`[ResourceGroupName <String>]`: 리소스 그룹이 아래에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7efa0-154">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="7efa0-155">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7efa0-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="7efa0-156">`[TargetSubscriptionId <String>]`: 대상 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7efa0-156">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="7efa0-157">`[Tenant <String>]`: 디렉터리 테 넌 트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7efa0-157">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="7efa0-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7efa0-158">RELATED LINKS</span></span>

