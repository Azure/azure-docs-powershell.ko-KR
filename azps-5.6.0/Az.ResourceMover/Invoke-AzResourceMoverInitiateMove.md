---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverinitiatemove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
ms.openlocfilehash: e075da17009c863e8c564eb5379495a1bdaff505
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999947"
---
# <span data-ttu-id="c749f-101">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="c749f-101">Invoke-AzResourceMoverInitiateMove</span></span>

## <span data-ttu-id="c749f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c749f-102">SYNOPSIS</span></span>
<span data-ttu-id="c749f-103">요청 본문에 포함된 리소스 집합을 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="c749f-103">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="c749f-104">moveResources가 moveState 'MovePending' 또는 'MoveFailed'에 있는 후에 이동 작업이 트리거됩니다. 성공적으로 완료되면 moveResource moveState가 커밋 보류로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="c749f-104">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="c749f-105">사용자가 유효성 검사로 작업을 호출할 수 있는 작업을 요구하도록 사용자를 지원하기 위해 유효성 검사 속성이 true로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="c749f-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="c749f-106">구문</span><span class="sxs-lookup"><span data-stu-id="c749f-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverInitiateMove -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c749f-107">설명</span><span class="sxs-lookup"><span data-stu-id="c749f-107">DESCRIPTION</span></span>
<span data-ttu-id="c749f-108">요청 본문에 포함된 리소스 집합을 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="c749f-108">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="c749f-109">moveResources가 moveState 'MovePending' 또는 'MoveFailed'에 있는 후에 이동 작업이 트리거됩니다. 성공적으로 완료되면 moveResource moveState가 커밋 보류로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="c749f-109">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="c749f-110">사용자가 유효성 검사로 작업을 호출할 수 있는 작업을 요구하도록 사용자를 지원하기 위해 유효성 검사 속성이 true로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="c749f-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="c749f-111">예제</span><span class="sxs-lookup"><span data-stu-id="c749f-111">EXAMPLES</span></span>

### <span data-ttu-id="c749f-112">예제 1: 리소스에 대해 이동을 시작하기 전에 종속성의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="c749f-112">Example 1: Validate the dependecies before Initiate Move for the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId" -ValidateOnly


AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 9:39:37 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralus-demoRMS/operations/095f3d5
                 1-ebd1-4c5b-9a65-d78ebe3ac345
Message        : 
Name           : 095f3d51-ebd1-4c5b-9a65-d78ebe3ac345
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 9:39:37 AM
Status         : Succeeded

```

<span data-ttu-id="c749f-113">리소스에 대해 이동을 시작하기 전에 종속성의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="c749f-113">Validate the dependecies before Initiate Move for the resources.</span></span>

### <span data-ttu-id="c749f-114">예제 2: 입력으로 "MoveResource Name"을 사용하여 Move 컬렉션의 리소스 집합에 대해 이동을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="c749f-114">Example 2: Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input.</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverInitiateMove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId" 

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 11:56:33 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/290472e3-c8de-4c55-aba1-3a34a7a4ab38
Message        : 
Name           : 290472e3-c8de-4c55-aba1-3a34a7a4ab38
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 11:55:21 AM
Status         : Succeeded

```

<span data-ttu-id="c749f-115">입력으로 "MoveResource Name"을 사용하여 Move 컬렉션의 리소스 집합에 대해 이동을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="c749f-115">Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="c749f-116">예제 3: 입력으로 "SourceARMID"를 사용하여 이동 컬렉션의 리소스 집합에 대해 이동을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="c749f-116">Example 3: Initiate Move for the set of resources in the Move Collection using "SourceARMID" as input.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:01:35 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/955fd43c-10b6-481e-888b-d26d6ec42aea
Message        : 
Name           : 955fd43c-10b6-481e-888b-d26d6ec42aea
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:00:21 PM
Status         : Succeeded

```

<span data-ttu-id="c749f-117">입력으로 "SourceARMID"를 사용하여 이동 컬렉션의 리소스 집합에 대해 이동을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="c749f-117">Initiate Move for the set of resources in the Move collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="c749f-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c749f-118">PARAMETERS</span></span>

### <span data-ttu-id="c749f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c749f-119">-AsJob</span></span>
<span data-ttu-id="c749f-120">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c749f-120">Run the command as a job</span></span>

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

### <span data-ttu-id="c749f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c749f-121">-DefaultProfile</span></span>
<span data-ttu-id="c749f-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c749f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c749f-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="c749f-123">-MoveCollectionName</span></span>
<span data-ttu-id="c749f-124">이동 컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c749f-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="c749f-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="c749f-125">-MoveResource</span></span>
<span data-ttu-id="c749f-126">입력 형식이 moveResourceInputType 속성을 통해 전환되지 않는 한 리소스 ID의 목록을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c749f-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="c749f-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="c749f-127">-MoveResourceInputType</span></span>
<span data-ttu-id="c749f-128">이동 리소스 입력 유형을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="c749f-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="c749f-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c749f-129">-NoWait</span></span>
<span data-ttu-id="c749f-130">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="c749f-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c749f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c749f-131">-ResourceGroupName</span></span>
<span data-ttu-id="c749f-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c749f-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="c749f-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c749f-133">-SubscriptionId</span></span>
<span data-ttu-id="c749f-134">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c749f-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="c749f-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="c749f-135">-ValidateOnly</span></span>
<span data-ttu-id="c749f-136">작업이 전제 요구 사항을 실행해야 하는지 여부를 나타내는 값을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c749f-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="c749f-137">-확인</span><span class="sxs-lookup"><span data-stu-id="c749f-137">-Confirm</span></span>
<span data-ttu-id="c749f-138">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c749f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c749f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c749f-139">-WhatIf</span></span>
<span data-ttu-id="c749f-140">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c749f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c749f-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c749f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c749f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c749f-142">CommonParameters</span></span>
<span data-ttu-id="c749f-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c749f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c749f-144">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c749f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c749f-145">입력</span><span class="sxs-lookup"><span data-stu-id="c749f-145">INPUTS</span></span>

## <span data-ttu-id="c749f-146">출력</span><span class="sxs-lookup"><span data-stu-id="c749f-146">OUTPUTS</span></span>

### <span data-ttu-id="c749f-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="c749f-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="c749f-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c749f-148">NOTES</span></span>

<span data-ttu-id="c749f-149">별칭</span><span class="sxs-lookup"><span data-stu-id="c749f-149">ALIASES</span></span>

## <span data-ttu-id="c749f-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c749f-150">RELATED LINKS</span></span>

