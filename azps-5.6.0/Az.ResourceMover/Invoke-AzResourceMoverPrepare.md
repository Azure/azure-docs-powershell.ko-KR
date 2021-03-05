---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverprepare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
ms.openlocfilehash: 95ad5dad6bd375595a452881e1dfe72a9f314207
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999936"
---
# <span data-ttu-id="4dc04-101">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="4dc04-101">Invoke-AzResourceMoverPrepare</span></span>

## <span data-ttu-id="4dc04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dc04-102">SYNOPSIS</span></span>
<span data-ttu-id="4dc04-103">시작은 요청 본문에 포함된 리소스 집합을 준비합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc04-103">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="4dc04-104">준비 작업은 moveState 'PreparePending' 또는 'PrepareFailed'에 있는 moveResources에 있습니다. 성공적으로 완료 시 moveResource moveState에서 MovePending으로 전환을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc04-104">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="4dc04-105">사용자가 유효성 검사로 작업을 호출할 수 있는 작업을 요구하도록 사용자를 지원하기 위해 유효성 검사 속성이 true로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dc04-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="4dc04-106">구문</span><span class="sxs-lookup"><span data-stu-id="4dc04-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverPrepare -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4dc04-107">설명</span><span class="sxs-lookup"><span data-stu-id="4dc04-107">DESCRIPTION</span></span>
<span data-ttu-id="4dc04-108">시작은 요청 본문에 포함된 리소스 집합을 준비합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc04-108">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="4dc04-109">준비 작업은 moveState 'PreparePending' 또는 'PrepareFailed'에 있는 moveResources에 있습니다. 성공적으로 완료 시 moveResource moveState에서 MovePending으로 전환을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc04-109">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="4dc04-110">사용자가 유효성 검사로 작업을 호출할 수 있는 작업을 요구하도록 사용자를 지원하기 위해 유효성 검사 속성이 true로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dc04-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="4dc04-111">예제</span><span class="sxs-lookup"><span data-stu-id="4dc04-111">EXAMPLES</span></span>

### <span data-ttu-id="4dc04-112">예제 1: 리소스를 준비하기 전에 종속성의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc04-112">Example 1: Validate the dependecies before prepare of the resources.</span></span> <span data-ttu-id="4dc04-113">준비해야 하는 필수 종속 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4dc04-113">Get the required dependent resources that also need to be prepared.</span></span>
```powershell
PS C:\> $resp = Invoke-AzResourceMoverPrepare -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemovm') -ValidateOnly

AdditionalInfo : {Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationErrorAdditionalInfo}
Code           : MoveCollectionMissingRequiredDependentResources
Detail         : {}
EndTime        : 2/9/2021 9:04:15 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RegionMoveRG-centralus-westcentralus/providers/Microsoft.Migr
                 ate/MoveCollections/PS-centralus-westcentralus-demoRMS/12d055bd-ac52-427f-8b05-b4b21c4b51e8
Message        : The operation has failed as required move resources are missing from the input.
                     Possible Causes: Dependent resources are missing from the input.
                     Recommended Action: Retry the operation with all required resources, if the issue persist contact support.

Name           : 12d055bd-ac52-427f-8b05-b4b21c4b51e8
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 9:04:14 AM
Status         : Failed

PS C:> $resp.Code
MoveCollectionMissingRequiredDependentResources

PS C:> $resp.AdditionalInfo[0].InfoMoveResource

SourceId                                                                                                                                  
--------                                                                                                                                  
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm111     
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet     
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg

```

<span data-ttu-id="4dc04-114">리소스를 준비하기 전에 종속성의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc04-114">Validate the dependecies before prepare of the resources.</span></span>
<span data-ttu-id="4dc04-115">준비해야 하는 필수 종속 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4dc04-115">Get the required dependent resources that also need to be prepared.</span></span>

### <span data-ttu-id="4dc04-116">예제 2: 입력으로 "MoveResource Name"을 사용하여 이동 컬렉션의 리소스 집합을 준비합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc04-116">Example 2: Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('PSDemoVM','psdemovm111', 'PSDemoRM-vnet','PSDemoVM-nsg')

AAdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/9/2021 11:25:13 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralus-demoRMS/operations/49e4429
                 4-24ac-4eac-93da-e7e1c815554d
Message        : 
Name           : 49e44294-24ac-4eac-93da-e7e1c815554d
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 10:55:53 AM
Status         : Succeeded
```

<span data-ttu-id="4dc04-117">입력으로 "MoveResource Name"을 사용하여 Move Collection의 리소스 집합을 준비합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc04-117">Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="4dc04-118">예제 3: "SourceARMID"를 사용하여 이동 컬렉션의 리소스 집합을 준비합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc04-118">Example 3: Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRMS/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 2/9/2021 11:09:30 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRMS/operations/c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Message        :
Name           : c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 11:05:27 AM
Status         : Succeeded

```

<span data-ttu-id="4dc04-119">"SourceARMID"를 사용하여 이동 컬렉션의 리소스 집합을 준비합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc04-119">Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>

## <span data-ttu-id="4dc04-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4dc04-120">PARAMETERS</span></span>

### <span data-ttu-id="4dc04-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4dc04-121">-AsJob</span></span>
<span data-ttu-id="4dc04-122">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc04-122">Run the command as a job</span></span>

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

### <span data-ttu-id="4dc04-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dc04-123">-DefaultProfile</span></span>
<span data-ttu-id="4dc04-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4dc04-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dc04-125">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="4dc04-125">-MoveCollectionName</span></span>
<span data-ttu-id="4dc04-126">이동 컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4dc04-126">The Move Collection Name.</span></span>

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

### <span data-ttu-id="4dc04-127">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="4dc04-127">-MoveResource</span></span>
<span data-ttu-id="4dc04-128">입력 형식이 moveResourceInputType 속성을 통해 전환되지 않는 한 리소스 ID의 목록을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc04-128">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dc04-129">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="4dc04-129">-MoveResourceInputType</span></span>
<span data-ttu-id="4dc04-130">이동 리소스 입력 유형을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc04-130">Defines the move resource input type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.MoveResourceInputType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dc04-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4dc04-131">-NoWait</span></span>
<span data-ttu-id="4dc04-132">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="4dc04-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4dc04-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dc04-133">-ResourceGroupName</span></span>
<span data-ttu-id="4dc04-134">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4dc04-134">The Resource Group Name.</span></span>

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

### <span data-ttu-id="4dc04-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4dc04-135">-SubscriptionId</span></span>
<span data-ttu-id="4dc04-136">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4dc04-136">The Subscription ID.</span></span>

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

### <span data-ttu-id="4dc04-137">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="4dc04-137">-ValidateOnly</span></span>
<span data-ttu-id="4dc04-138">작업이 전제 요구 사항을 실행해야 하는지 여부를 나타내는 값을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc04-138">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="4dc04-139">-확인</span><span class="sxs-lookup"><span data-stu-id="4dc04-139">-Confirm</span></span>
<span data-ttu-id="4dc04-140">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dc04-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dc04-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dc04-141">-WhatIf</span></span>
<span data-ttu-id="4dc04-142">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4dc04-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dc04-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4dc04-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dc04-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dc04-144">CommonParameters</span></span>
<span data-ttu-id="4dc04-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc04-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dc04-146">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4dc04-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dc04-147">입력</span><span class="sxs-lookup"><span data-stu-id="4dc04-147">INPUTS</span></span>

## <span data-ttu-id="4dc04-148">출력</span><span class="sxs-lookup"><span data-stu-id="4dc04-148">OUTPUTS</span></span>

### <span data-ttu-id="4dc04-149">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="4dc04-149">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="4dc04-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4dc04-150">NOTES</span></span>

<span data-ttu-id="4dc04-151">별칭</span><span class="sxs-lookup"><span data-stu-id="4dc04-151">ALIASES</span></span>

## <span data-ttu-id="4dc04-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4dc04-152">RELATED LINKS</span></span>

