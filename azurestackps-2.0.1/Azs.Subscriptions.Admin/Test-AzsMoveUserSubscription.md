---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/test-azsmoveusersubscription
schema: 2.0.0
ms.openlocfilehash: c0e80b7d0f17bf505c0b3bb8d22539afffea851a
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94045280"
---
# <span data-ttu-id="9e2c2-101">Test-AzsMoveUserSubscription</span><span class="sxs-lookup"><span data-stu-id="9e2c2-101">Test-AzsMoveUserSubscription</span></span>

## <span data-ttu-id="9e2c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e2c2-102">SYNOPSIS</span></span>
<span data-ttu-id="9e2c2-103">위임 된 공급자 제공 간에 사용자 구독을 이동할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-103">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="9e2c2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9e2c2-104">SYNTAX</span></span>

### <span data-ttu-id="9e2c2-105">ValidateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="9e2c2-105">ValidateExpanded (Default)</span></span>
```
Test-AzsMoveUserSubscription -ResourceId <String[]> [-SubscriptionId <String>]
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9e2c2-106">Validate</span><span class="sxs-lookup"><span data-stu-id="9e2c2-106">Validate</span></span>
```
Test-AzsMoveUserSubscription -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9e2c2-107">ValidateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9e2c2-107">ValidateViaIdentity</span></span>
```
Test-AzsMoveUserSubscription -InputObject <ISubscriptionsAdminIdentity>
 -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9e2c2-108">ValidateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9e2c2-108">ValidateViaIdentityExpanded</span></span>
```
Test-AzsMoveUserSubscription -InputObject <ISubscriptionsAdminIdentity> -ResourceId <String[]>
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9e2c2-109">설명은</span><span class="sxs-lookup"><span data-stu-id="9e2c2-109">DESCRIPTION</span></span>
<span data-ttu-id="9e2c2-110">위임 된 공급자 제공 간에 사용자 구독을 이동할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-110">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="9e2c2-111">예제의</span><span class="sxs-lookup"><span data-stu-id="9e2c2-111">EXAMPLES</span></span>

### <span data-ttu-id="9e2c2-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="9e2c2-112">Example 1</span></span>
```powershell
PS C:\> Test-MoveUserSubscription \`
    -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1"
    -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"

```

<span data-ttu-id="9e2c2-113">사용자 구독을 위임 된 공급자 제공으로 이동할 수 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-113">Test that user subscriptions can be moved to a delegated provider offer.</span></span>

### <span data-ttu-id="9e2c2-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="9e2c2-114">Example 2</span></span>
```powershell
PS C:\> $resourceIds = Get-AzsUserSubscription | where Displayname -eq "testsubscription" | Select -ExpandProperty Id
Test-MoveUserSubscription -ResourceId $resourceIds

```

<span data-ttu-id="9e2c2-115">위임 된 공급자에서 기본 공급자로 사용자 구독을 이동할 수 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-115">Test that user subscriptions can be moved from a delegated provider to the Default Provider.</span></span>

## <span data-ttu-id="9e2c2-116">변수</span><span class="sxs-lookup"><span data-stu-id="9e2c2-116">PARAMETERS</span></span>

### <span data-ttu-id="9e2c2-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e2c2-117">-AsJob</span></span>
<span data-ttu-id="9e2c2-118">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="9e2c2-118">Run the command as a job</span></span>

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

### <span data-ttu-id="9e2c2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e2c2-119">-DefaultProfile</span></span>
<span data-ttu-id="9e2c2-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e2c2-121">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="9e2c2-121">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="9e2c2-122">위임 된 공급자가 관리 컨텍스트에서 구독이 이동할 식별자를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-122">The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

```yaml
Type: System.String
Parameter Sets: ValidateExpanded, ValidateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9e2c2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e2c2-123">-InputObject</span></span>
<span data-ttu-id="9e2c2-124">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: ValidateViaIdentity, ValidateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="9e2c2-125">-MoveSubscriptionsDefinition</span><span class="sxs-lookup"><span data-stu-id="9e2c2-125">-MoveSubscriptionsDefinition</span></span>
<span data-ttu-id="9e2c2-126">만들기로 구독 이동 작업 정의, MOVESUB, TIONSDEFINITION 속성에 대 한 참고 섹션 및 해시 테이블 만들기를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-126">The move subscriptions action definition To construct, see NOTES section for MOVESUBSCRIPTIONSDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition
Parameter Sets: Validate, ValidateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="9e2c2-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9e2c2-127">-NoWait</span></span>
<span data-ttu-id="9e2c2-128">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="9e2c2-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9e2c2-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e2c2-129">-PassThru</span></span>
<span data-ttu-id="9e2c2-130">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9e2c2-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e2c2-131">-ResourceId</span></span>
<span data-ttu-id="9e2c2-132">위임 된 대상 공급자 제공으로 이동할 구독의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-132">A collection of subscriptions to move to the target delegated provider offer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ValidateExpanded, ValidateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9e2c2-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9e2c2-133">-SubscriptionId</span></span>
<span data-ttu-id="9e2c2-134">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-134">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Validate, ValidateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9e2c2-135">-확인</span><span class="sxs-lookup"><span data-stu-id="9e2c2-135">-Confirm</span></span>
<span data-ttu-id="9e2c2-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e2c2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e2c2-137">-WhatIf</span></span>
<span data-ttu-id="9e2c2-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e2c2-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e2c2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e2c2-140">CommonParameters</span></span>
<span data-ttu-id="9e2c2-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e2c2-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e2c2-143">입력</span><span class="sxs-lookup"><span data-stu-id="9e2c2-143">INPUTS</span></span>

### <span data-ttu-id="9e2c2-144">SubscriptionsAdmin. PowerShell. Api20151101. Imovesub\ Tionsdefinition</span><span class="sxs-lookup"><span data-stu-id="9e2c2-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition</span></span>

### <span data-ttu-id="9e2c2-145">SubscriptionsAdmin. ISubscriptionsAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="9e2c2-145">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="9e2c2-146">출력</span><span class="sxs-lookup"><span data-stu-id="9e2c2-146">OUTPUTS</span></span>

### <span data-ttu-id="9e2c2-147">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="9e2c2-147">System.Boolean</span></span>

<span data-ttu-id="9e2c2-148">별칭과</span><span class="sxs-lookup"><span data-stu-id="9e2c2-148">ALIASES</span></span>

### <span data-ttu-id="9e2c2-149">Test-AzsMoveSubscription</span><span class="sxs-lookup"><span data-stu-id="9e2c2-149">Test-AzsMoveSubscription</span></span>

## <span data-ttu-id="9e2c2-150">상속자</span><span class="sxs-lookup"><span data-stu-id="9e2c2-150">NOTES</span></span>

<span data-ttu-id="9e2c2-151">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-151">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9e2c2-152">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9e2c2-153">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="9e2c2-153">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9e2c2-154">`[DelegatedProvider <String>]`: DelegatedProvider 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-154">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="9e2c2-155">`[DelegatedProviderSubscriptionId <String>]`: 위임 된 공급자 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-155">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="9e2c2-156">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="9e2c2-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9e2c2-157">`[Location <String>]`: AzureStack 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-157">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="9e2c2-158">`[ManifestName <String>]`: 매니페스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-158">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="9e2c2-159">`[Offer <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-159">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="9e2c2-160">`[OfferDelegationName <String>]`: 제안 위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-160">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="9e2c2-161">`[OperationsStatusName <String>]`: 작업 상태 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-161">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="9e2c2-162">`[Plan <String>]`: 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-162">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="9e2c2-163">`[PlanAcquisitionId <String>]`: 계획 획득 식별자</span><span class="sxs-lookup"><span data-stu-id="9e2c2-163">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="9e2c2-164">`[Quota <String>]`: 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-164">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="9e2c2-165">`[ResourceGroupName <String>]`: 리소스 그룹이 아래에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-165">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="9e2c2-166">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-166">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9e2c2-167">`[TargetSubscriptionId <String>]`: 대상 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-167">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="9e2c2-168">`[Tenant <String>]`: 디렉터리 테 넌 트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-168">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="9e2c2-169">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition> : 구독 이동 작업 정의</span><span class="sxs-lookup"><span data-stu-id="9e2c2-169">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition>: The move subscriptions action definition</span></span>
  - <span data-ttu-id="9e2c2-170">`Resources <String[]>`: 대상 위임 된 공급자 제공으로 이동할 구독의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-170">`Resources <String[]>`: A collection of subscriptions to move to the target delegated provider offer.</span></span>
  - <span data-ttu-id="9e2c2-171">`[TargetDelegatedProviderOffer <String>]`: 위임 된 공급자가 관리 컨텍스트에서 구독으로 이동할 식별자를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c2-171">`[TargetDelegatedProviderOffer <String>]`: The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

## <span data-ttu-id="9e2c2-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e2c2-172">RELATED LINKS</span></span>

