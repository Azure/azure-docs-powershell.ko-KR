---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverdiscard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
ms.openlocfilehash: c4af588c119cb819fcb87fbc7dbdd869540825ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492401"
---
# <span data-ttu-id="5979c-101">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="5979c-101">Invoke-AzResourceMoverDiscard</span></span>

## <span data-ttu-id="5979c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5979c-102">SYNOPSIS</span></span>
<span data-ttu-id="5979c-103">요청 본문에 포함된 리소스 집합을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="5979c-103">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="5979c-104">삭제 작업은 moveState 'CommitPending' 또는 'DiscardFailed'의 moveResources에서 트리거됩니다. 성공적으로 완료되면 moveResource moveState가 MovePending으로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="5979c-104">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="5979c-105">사용자가 작업을 전제로 하는 작업을 지원하기 위해 클라이언트는 validateOnly 속성이 true로 설정된 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5979c-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="5979c-106">구문</span><span class="sxs-lookup"><span data-stu-id="5979c-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverDiscard -Name <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5979c-107">설명</span><span class="sxs-lookup"><span data-stu-id="5979c-107">DESCRIPTION</span></span>
<span data-ttu-id="5979c-108">요청 본문에 포함된 리소스 집합을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="5979c-108">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="5979c-109">삭제 작업은 moveState 'CommitPending' 또는 'DiscardFailed'의 moveResources에서 트리거됩니다. 성공적으로 완료되면 moveResource moveState가 MovePending으로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="5979c-109">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="5979c-110">사용자가 작업을 전제로 하는 작업을 지원하기 위해 클라이언트는 validateOnly 속성이 true로 설정된 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5979c-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="5979c-111">예제</span><span class="sxs-lookup"><span data-stu-id="5979c-111">EXAMPLES</span></span>

### <span data-ttu-id="5979c-112">예제 1: 리소스를 삭제하기 전에 종속성의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="5979c-112">Example 1: Validate the dependecies before Discard of  the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverDiscard -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg') -ValidateOnly

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 9:44:54 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/62861ceb-28c9-4e0c-811b-84692a203181
Message        :
Name           : 62861ceb-28c9-4e0c-811b-84692a203181
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 9:44:54 AM
Status         : Succeeded

```

<span data-ttu-id="5979c-113">리소스를 삭제하기 전에 종속성의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="5979c-113">Validate the dependecies before Discard of  the resources.</span></span>

### <span data-ttu-id="5979c-114">예제 2: 입력으로 "MoveResource Name"을 사용하여 리소스 이동을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="5979c-114">Example 2: Discards the move of the resources using "MoveResource Name" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverDiscard -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:26:51 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/21f99cd3-89a4-4fcb-8b96-40d0572a6377
Message        :
Name           : 21f99cd3-89a4-4fcb-8b96-40d0572a6377
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:26:39 AM
Status         : Succeeded

```

<span data-ttu-id="5979c-115">입력으로 "MoveResource Name"을 사용하여 리소스의 이동을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="5979c-115">Discards the move of the resources using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="5979c-116">예제 3: 입력으로 "SourceARMID"를 사용하여 리소스 이동을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="5979c-116">Example 3: Discards the move of the resources using "SourceARMID" as input</span></span>
```powershell
PS C:\>  Invoke-AzResourceMoverDiscard -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:33:37 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/b842efcd-e5fd-42b0-a277-01ee8225deed
Message        :
Name           : b842efcd-e5fd-42b0-a277-01ee8225deed
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:33:23 AM
Status         : Succeeded


```

<span data-ttu-id="5979c-117">입력으로 "SourceARMID"를 사용하여 리소스의 이동을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="5979c-117">Discards the move of the resources using "SourceARMID" as input.</span></span>

## <span data-ttu-id="5979c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5979c-118">PARAMETERS</span></span>

### <span data-ttu-id="5979c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5979c-119">-AsJob</span></span>
<span data-ttu-id="5979c-120">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="5979c-120">Run the command as a job</span></span>

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

### <span data-ttu-id="5979c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5979c-121">-DefaultProfile</span></span>
<span data-ttu-id="5979c-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5979c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5979c-123">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="5979c-123">-MoveResource</span></span>
<span data-ttu-id="5979c-124">입력 형식이 moveResourceInputType 속성을 통해 전환되지 않는 한 기본적으로 리소스 ID의 목록을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5979c-124">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="5979c-125">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="5979c-125">-MoveResourceInputType</span></span>
<span data-ttu-id="5979c-126">이동 리소스 입력 형식을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="5979c-126">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="5979c-127">-Name</span><span class="sxs-lookup"><span data-stu-id="5979c-127">-Name</span></span>
<span data-ttu-id="5979c-128">컬렉션 이동 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5979c-128">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5979c-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5979c-129">-NoWait</span></span>
<span data-ttu-id="5979c-130">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="5979c-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5979c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5979c-131">-ResourceGroupName</span></span>
<span data-ttu-id="5979c-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5979c-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="5979c-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5979c-133">-SubscriptionId</span></span>
<span data-ttu-id="5979c-134">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5979c-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="5979c-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="5979c-135">-ValidateOnly</span></span>
<span data-ttu-id="5979c-136">작업이 사전 요구 사항을 실행해야 하는지 여부를 나타내는 값을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5979c-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="5979c-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5979c-137">-Confirm</span></span>
<span data-ttu-id="5979c-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5979c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5979c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5979c-139">-WhatIf</span></span>
<span data-ttu-id="5979c-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5979c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5979c-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5979c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5979c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5979c-142">CommonParameters</span></span>
<span data-ttu-id="5979c-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5979c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5979c-144">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5979c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5979c-145">입력</span><span class="sxs-lookup"><span data-stu-id="5979c-145">INPUTS</span></span>

## <span data-ttu-id="5979c-146">출력</span><span class="sxs-lookup"><span data-stu-id="5979c-146">OUTPUTS</span></span>

### <span data-ttu-id="5979c-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="5979c-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="5979c-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5979c-148">NOTES</span></span>

<span data-ttu-id="5979c-149">별칭</span><span class="sxs-lookup"><span data-stu-id="5979c-149">ALIASES</span></span>

## <span data-ttu-id="5979c-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5979c-150">RELATED LINKS</span></span>

