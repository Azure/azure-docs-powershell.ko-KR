---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverdiscard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
ms.openlocfilehash: 5e54501e6337943561489a80adf4e8789a55a394
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999952"
---
# <span data-ttu-id="a5eb1-101">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="a5eb1-101">Invoke-AzResourceMoverDiscard</span></span>

## <span data-ttu-id="a5eb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5eb1-102">SYNOPSIS</span></span>
<span data-ttu-id="a5eb1-103">요청 본문에 포함된 리소스 집합을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a5eb1-103">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="a5eb1-104">삭제 작업은 moveState 'CommitPending' 또는 'DiscardFailed'의 moveResources에서 트리거됩니다. 성공적으로 완료되면 moveResource moveState가 MovePending으로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="a5eb1-104">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="a5eb1-105">사용자가 유효성 검사로 작업을 호출할 수 있는 작업을 요구하도록 사용자를 지원하기 위해 유효성 검사 속성이 true로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5eb1-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="a5eb1-106">구문</span><span class="sxs-lookup"><span data-stu-id="a5eb1-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverDiscard -Name <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a5eb1-107">설명</span><span class="sxs-lookup"><span data-stu-id="a5eb1-107">DESCRIPTION</span></span>
<span data-ttu-id="a5eb1-108">요청 본문에 포함된 리소스 집합을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a5eb1-108">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="a5eb1-109">삭제 작업은 moveState 'CommitPending' 또는 'DiscardFailed'의 moveResources에서 트리거됩니다. 성공적으로 완료되면 moveResource moveState가 MovePending으로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="a5eb1-109">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="a5eb1-110">사용자가 유효성 검사로 작업을 호출할 수 있는 작업을 요구하도록 사용자를 지원하기 위해 유효성 검사 속성이 true로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5eb1-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="a5eb1-111">예제</span><span class="sxs-lookup"><span data-stu-id="a5eb1-111">EXAMPLES</span></span>

### <span data-ttu-id="a5eb1-112">예제 1: 리소스를 삭제하기 전에 종속성의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="a5eb1-112">Example 1: Validate the dependecies before Discard of  the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId" -ValidateOnly

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:39:48 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralus-demoRMS/operations/095f3d5
                 1-ebd1-4c5b-9a65-d78ebe3ac345
Message        : 
Name           : 095f3d51-ebd1-4c5b-9a65-d78ebe3ac345
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:39:37 PM
Status         : Succeeded

```

<span data-ttu-id="a5eb1-113">리소스를 삭제하기 전에 종속성의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="a5eb1-113">Validate the dependecies before Discard of  the resources.</span></span>

### <span data-ttu-id="a5eb1-114">예제 2: 입력으로 "MoveResource Name"을 사용하여 리소스의 이동을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a5eb1-114">Example 2: Discards the move of the resources using "MoveResource Name" as input.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverDiscard -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:56:33 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/290472e3-c8de-4c55-aba1-3a34a7a4ab38
Message        : 
Name           : 290472e3-c8de-4c55-aba1-3a34a7a4ab38
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:55:21 PM
Status         : Succeeded

```

<span data-ttu-id="a5eb1-115">입력으로 "MoveResource Name"을 사용하여 리소스의 이동을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a5eb1-115">Discards the move of the resources using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="a5eb1-116">예제 3: 입력으로 "SourceARMID"를 사용하여 리소스의 이동을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a5eb1-116">Example 3: Discards the move of the resources using "SourceARMID" as input.</span></span>
```powershell
PS C:\>  Invoke-AzResourceMoverDiscard -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 1:01:32 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/955fd43c-10b6-481e-888b-d26d6ec42aea
Message        : 
Name           : 955fd43c-10b6-481e-888b-d26d6ec42aea
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 1:00:00 PM
Status         : Succeeded


```

<span data-ttu-id="a5eb1-117">입력으로 "SourceARMID"를 사용하여 리소스의 이동을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a5eb1-117">Discards the move of the resources using "SourceARMID" as input.</span></span>

## <span data-ttu-id="a5eb1-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a5eb1-118">PARAMETERS</span></span>

### <span data-ttu-id="a5eb1-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5eb1-119">-AsJob</span></span>
<span data-ttu-id="a5eb1-120">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a5eb1-120">Run the command as a job</span></span>

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

### <span data-ttu-id="a5eb1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5eb1-121">-DefaultProfile</span></span>
<span data-ttu-id="a5eb1-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5eb1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5eb1-123">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="a5eb1-123">-MoveResource</span></span>
<span data-ttu-id="a5eb1-124">입력 형식이 moveResourceInputType 속성을 통해 전환되지 않는 한 리소스 ID의 목록을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5eb1-124">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="a5eb1-125">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="a5eb1-125">-MoveResourceInputType</span></span>
<span data-ttu-id="a5eb1-126">이동 리소스 입력 유형을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="a5eb1-126">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="a5eb1-127">-Name</span><span class="sxs-lookup"><span data-stu-id="a5eb1-127">-Name</span></span>
<span data-ttu-id="a5eb1-128">이동 컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5eb1-128">The Move Collection Name.</span></span>

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

### <span data-ttu-id="a5eb1-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a5eb1-129">-NoWait</span></span>
<span data-ttu-id="a5eb1-130">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="a5eb1-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a5eb1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5eb1-131">-ResourceGroupName</span></span>
<span data-ttu-id="a5eb1-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5eb1-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="a5eb1-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5eb1-133">-SubscriptionId</span></span>
<span data-ttu-id="a5eb1-134">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a5eb1-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="a5eb1-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="a5eb1-135">-ValidateOnly</span></span>
<span data-ttu-id="a5eb1-136">작업이 전제 요구 사항을 실행해야 하는지 여부를 나타내는 값을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5eb1-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="a5eb1-137">-확인</span><span class="sxs-lookup"><span data-stu-id="a5eb1-137">-Confirm</span></span>
<span data-ttu-id="a5eb1-138">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5eb1-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5eb1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5eb1-139">-WhatIf</span></span>
<span data-ttu-id="a5eb1-140">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a5eb1-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5eb1-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5eb1-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5eb1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5eb1-142">CommonParameters</span></span>
<span data-ttu-id="a5eb1-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a5eb1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5eb1-144">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5eb1-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5eb1-145">입력</span><span class="sxs-lookup"><span data-stu-id="a5eb1-145">INPUTS</span></span>

## <span data-ttu-id="a5eb1-146">출력</span><span class="sxs-lookup"><span data-stu-id="a5eb1-146">OUTPUTS</span></span>

### <span data-ttu-id="a5eb1-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="a5eb1-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="a5eb1-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a5eb1-148">NOTES</span></span>

<span data-ttu-id="a5eb1-149">별칭</span><span class="sxs-lookup"><span data-stu-id="a5eb1-149">ALIASES</span></span>

## <span data-ttu-id="a5eb1-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5eb1-150">RELATED LINKS</span></span>

