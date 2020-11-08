---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 03fbbc38582bf301052074e674fa86abe97d6b61
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/22/2020
ms.locfileid: "94045109"
---
# <span data-ttu-id="81a87-101">Remove-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="81a87-101">Remove-AzsUserSubscription</span></span>

## <span data-ttu-id="81a87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81a87-102">SYNOPSIS</span></span>


## <span data-ttu-id="81a87-103">구문과</span><span class="sxs-lookup"><span data-stu-id="81a87-103">SYNTAX</span></span>

### <span data-ttu-id="81a87-104">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="81a87-104">Delete (Default)</span></span>
```
Remove-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Force] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="81a87-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="81a87-105">DeleteViaIdentity</span></span>
```
Remove-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-Force]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="81a87-106">설명은</span><span class="sxs-lookup"><span data-stu-id="81a87-106">DESCRIPTION</span></span>


## <span data-ttu-id="81a87-107">예제의</span><span class="sxs-lookup"><span data-stu-id="81a87-107">EXAMPLES</span></span>

### <span data-ttu-id="81a87-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="81a87-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzsUserSubscription -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"

```

<span data-ttu-id="81a87-109">지정 된 테 넌 트 구독을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a87-109">Delete the specified tenant subscription.</span></span>

## <span data-ttu-id="81a87-110">변수</span><span class="sxs-lookup"><span data-stu-id="81a87-110">PARAMETERS</span></span>

### <span data-ttu-id="81a87-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81a87-111">-DefaultProfile</span></span>


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

### <span data-ttu-id="81a87-112">-Force</span><span class="sxs-lookup"><span data-stu-id="81a87-112">-Force</span></span>


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

### <span data-ttu-id="81a87-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81a87-113">-InputObject</span></span>
<span data-ttu-id="81a87-114">생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="81a87-114">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="81a87-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81a87-115">-PassThru</span></span>


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

### <span data-ttu-id="81a87-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="81a87-116">-SubscriptionId</span></span>


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

### <span data-ttu-id="81a87-117">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="81a87-117">-TargetSubscriptionId</span></span>


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

### <span data-ttu-id="81a87-118">-확인</span><span class="sxs-lookup"><span data-stu-id="81a87-118">-Confirm</span></span>
<span data-ttu-id="81a87-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a87-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81a87-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81a87-120">-WhatIf</span></span>
<span data-ttu-id="81a87-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="81a87-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81a87-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="81a87-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81a87-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81a87-123">CommonParameters</span></span>
<span data-ttu-id="81a87-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a87-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81a87-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="81a87-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81a87-126">입력</span><span class="sxs-lookup"><span data-stu-id="81a87-126">INPUTS</span></span>

### <span data-ttu-id="81a87-127">SubscriptionsAdmin. ISubscriptionsAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="81a87-127">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="81a87-128">출력</span><span class="sxs-lookup"><span data-stu-id="81a87-128">OUTPUTS</span></span>

### <span data-ttu-id="81a87-129">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="81a87-129">System.Boolean</span></span>

<span data-ttu-id="81a87-130">별칭과</span><span class="sxs-lookup"><span data-stu-id="81a87-130">ALIASES</span></span>

## <span data-ttu-id="81a87-131">상속자</span><span class="sxs-lookup"><span data-stu-id="81a87-131">NOTES</span></span>

<span data-ttu-id="81a87-132">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a87-132">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="81a87-133">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="81a87-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="81a87-134">INPUTOBJECT <ISubscriptionsAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="81a87-134">INPUTOBJECT <ISubscriptionsAdminIdentity>:</span></span> 
  - <span data-ttu-id="81a87-135">`[DelegatedProvider <String>]`: DelegatedProvider 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="81a87-135">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="81a87-136">`[DelegatedProviderSubscriptionId <String>]`: 위임 된 공급자 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="81a87-136">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="81a87-137">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="81a87-137">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="81a87-138">`[Location <String>]`: AzureStack 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="81a87-138">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="81a87-139">`[ManifestName <String>]`: 매니페스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81a87-139">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="81a87-140">`[Offer <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81a87-140">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="81a87-141">`[OfferDelegationName <String>]`: 제안 위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81a87-141">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="81a87-142">`[OperationsStatusName <String>]`: 작업 상태 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81a87-142">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="81a87-143">`[Plan <String>]`: 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81a87-143">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="81a87-144">`[PlanAcquisitionId <String>]`: 계획 획득 식별자</span><span class="sxs-lookup"><span data-stu-id="81a87-144">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="81a87-145">`[Quota <String>]`: 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81a87-145">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="81a87-146">`[ResourceGroupName <String>]`: 리소스 그룹이 아래에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81a87-146">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="81a87-147">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a87-147">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="81a87-148">`[TargetSubscriptionId <String>]`: 대상 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="81a87-148">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="81a87-149">`[Tenant <String>]`: 디렉터리 테 넌 트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81a87-149">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="81a87-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="81a87-150">RELATED LINKS</span></span>

