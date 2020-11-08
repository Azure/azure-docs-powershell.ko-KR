---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: 0db0f7ae4358e49ff62f94132701be1f4bd4d0b7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046822"
---
# <span data-ttu-id="51909-101">New-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="51909-101">New-AzsAcquiredPlan</span></span>

## <span data-ttu-id="51909-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51909-102">SYNOPSIS</span></span>


## <span data-ttu-id="51909-103">구문과</span><span class="sxs-lookup"><span data-stu-id="51909-103">SYNTAX</span></span>

### <span data-ttu-id="51909-104">CreateExpanded (기본값)</span><span class="sxs-lookup"><span data-stu-id="51909-104">CreateExpanded (Default)</span></span>
```
New-AzsAcquiredPlan -TargetSubscriptionId <String> [-PlanAcquisitionId <String>] [-SubscriptionId <String>]
 [-AcquisitionTime <DateTime>] [-ExternalReferenceId <String>] [-Id <String>] [-PlanId <String>]
 [-ProvisioningState <ProvisioningState>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="51909-105">만드는</span><span class="sxs-lookup"><span data-stu-id="51909-105">Create</span></span>
```
New-AzsAcquiredPlan -TargetSubscriptionId <String> -AcquiredPlanDefinition <IPlanAcquisition>
 [-PlanAcquisitionId <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="51909-106">설명은</span><span class="sxs-lookup"><span data-stu-id="51909-106">DESCRIPTION</span></span>


## <span data-ttu-id="51909-107">예제의</span><span class="sxs-lookup"><span data-stu-id="51909-107">EXAMPLES</span></span>

### <span data-ttu-id="51909-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="51909-108">Example 1</span></span>
```powershell
PS C:\> New-AzsAcquiredPlan -PlanAcquisitionId $([Guid]::NewGuid()) -PlanId "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan" -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

AcquisitionId       : 718c7f7c-4868-479a-98ce-5caaa8f158c1
AcquisitionTime     : 3/12/2020 11:16:08 PM
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/acquiredPlan
                      s/718c7f7c-4868-479a-98ce-5caaa8f158c1
PlanId              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/plans/testplan
ProvisioningState   : Succeeded
```

<span data-ttu-id="51909-109">구독 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51909-109">Create a subscription plan.</span></span>

## <span data-ttu-id="51909-110">변수</span><span class="sxs-lookup"><span data-stu-id="51909-110">PARAMETERS</span></span>

### <span data-ttu-id="51909-111">-AcquiredPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="51909-111">-AcquiredPlanDefinition</span></span>
<span data-ttu-id="51909-112">생성 하려면 ACQUIREDPLANDEFINITION 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51909-112">To construct, see NOTES section for ACQUIREDPLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="51909-113">-AcquisitionTime</span><span class="sxs-lookup"><span data-stu-id="51909-113">-AcquisitionTime</span></span>


```yaml
Type: System.DateTime
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="51909-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51909-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="51909-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="51909-115">-ExternalReferenceId</span></span>


```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="51909-116">-Id</span><span class="sxs-lookup"><span data-stu-id="51909-116">-Id</span></span>


```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="51909-117">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="51909-117">-PlanAcquisitionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="51909-118">-PlanId</span><span class="sxs-lookup"><span data-stu-id="51909-118">-PlanId</span></span>


```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="51909-119">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="51909-119">-ProvisioningState</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ProvisioningState
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="51909-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="51909-120">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="51909-121">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="51909-121">-TargetSubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="51909-122">-확인</span><span class="sxs-lookup"><span data-stu-id="51909-122">-Confirm</span></span>
<span data-ttu-id="51909-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="51909-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51909-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51909-124">-WhatIf</span></span>
<span data-ttu-id="51909-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="51909-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51909-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="51909-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51909-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51909-127">CommonParameters</span></span>
<span data-ttu-id="51909-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="51909-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51909-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="51909-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51909-130">입력</span><span class="sxs-lookup"><span data-stu-id="51909-130">INPUTS</span></span>

### <span data-ttu-id="51909-131">SubscriptionsAdmin. PowerShell. Api20151101. I계획 취득</span><span class="sxs-lookup"><span data-stu-id="51909-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

## <span data-ttu-id="51909-132">출력</span><span class="sxs-lookup"><span data-stu-id="51909-132">OUTPUTS</span></span>

### <span data-ttu-id="51909-133">SubscriptionsAdmin. PowerShell. Api20151101. I계획 취득</span><span class="sxs-lookup"><span data-stu-id="51909-133">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

<span data-ttu-id="51909-134">별칭과</span><span class="sxs-lookup"><span data-stu-id="51909-134">ALIASES</span></span>

<span data-ttu-id="51909-135">New-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="51909-135">New-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="51909-136">상속자</span><span class="sxs-lookup"><span data-stu-id="51909-136">NOTES</span></span>

<span data-ttu-id="51909-137">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="51909-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="51909-138">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="51909-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="51909-139">ACQUIREDPLANDEFINITION <IPlanAcquisition> :</span><span class="sxs-lookup"><span data-stu-id="51909-139">ACQUIREDPLANDEFINITION <IPlanAcquisition>:</span></span> 
  - <span data-ttu-id="51909-140">`[AcquisitionId <String>]`: 인식 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="51909-140">`[AcquisitionId <String>]`: Acquisition identifier.</span></span>
  - <span data-ttu-id="51909-141">`[AcquisitionTime <DateTime?>]`: 취득 시간.</span><span class="sxs-lookup"><span data-stu-id="51909-141">`[AcquisitionTime <DateTime?>]`: Acquisition time.</span></span>
  - <span data-ttu-id="51909-142">`[ExternalReferenceId <String>]`: 외부 참조 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="51909-142">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="51909-143">`[Id <String>]`: 테 넌 트 구독 컨텍스트의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="51909-143">`[Id <String>]`: Identifier in the tenant subscription context.</span></span>
  - <span data-ttu-id="51909-144">`[PlanId <String>]`: 테 넌 트 구독 컨텍스트에서 id를 계획 합니다.</span><span class="sxs-lookup"><span data-stu-id="51909-144">`[PlanId <String>]`: Plan identifier in the tenant subscription context.</span></span>
  - <span data-ttu-id="51909-145">`[ProvisioningState <ProvisioningState?>]`: 프로비저닝 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="51909-145">`[ProvisioningState <ProvisioningState?>]`: State of the provisioning.</span></span>

## <span data-ttu-id="51909-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51909-146">RELATED LINKS</span></span>

