---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemovercommit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
ms.openlocfilehash: 9c205354b68def88b00fb67959669633d5ba1fc1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999979"
---
# <span data-ttu-id="3018d-101">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="3018d-101">Invoke-AzResourceMoverCommit</span></span>

## <span data-ttu-id="3018d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3018d-102">SYNOPSIS</span></span>
<span data-ttu-id="3018d-103">요청 본문에 포함된 리소스 집합을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="3018d-103">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="3018d-104">커밋 작업은 moveState 'CommitPending' 또는 'CommitFailed'의 moveResources에서 트리거됩니다. 완료 시 moveResource moveState가 커밋으로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="3018d-104">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="3018d-105">사용자가 유효성 검사로 작업을 호출할 수 있는 작업을 요구하도록 사용자를 지원하기 위해 유효성 검사 속성이 true로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="3018d-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="3018d-106">구문</span><span class="sxs-lookup"><span data-stu-id="3018d-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverCommit -MoveCollectionName <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3018d-107">설명</span><span class="sxs-lookup"><span data-stu-id="3018d-107">DESCRIPTION</span></span>
<span data-ttu-id="3018d-108">요청 본문에 포함된 리소스 집합을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="3018d-108">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="3018d-109">커밋 작업은 moveState 'CommitPending' 또는 'CommitFailed'의 moveResources에서 트리거됩니다. 완료 시 moveResource moveState가 커밋으로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="3018d-109">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="3018d-110">사용자가 유효성 검사로 작업을 호출할 수 있는 작업을 요구하도록 사용자를 지원하기 위해 유효성 검사 속성이 true로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="3018d-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="3018d-111">예제</span><span class="sxs-lookup"><span data-stu-id="3018d-111">EXAMPLES</span></span>

### <span data-ttu-id="3018d-112">예제 1: 리소스를 커밋하기 전에 종속성의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="3018d-112">Example 1: Validate the dependecies before commit of the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId" -ValidateOnly

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:38:26 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/c194298b-b2eb-4aab-80b4-129d1473b75c
Message        : 
Name           : c194298b-b2eb-4aab-80b4-129d1473b75c
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:38:25 PM
Status         : Succeeded

```

<span data-ttu-id="3018d-113">리소스를 커밋하기 전에 종속성의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="3018d-113">Validate the dependecies before commit of the resources.</span></span>

### <span data-ttu-id="3018d-114">예제 2: "MoveResource Name"을 입력으로 사용하여 이동 컬렉션에서 리소스 집합을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="3018d-114">Example 2: Commit the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverCommit -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:41:13 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/80c04850-7f3f-4e9c-aa68-b868978b59f3
Message        : 
Name           : 80c04850-7f3f-4e9c-aa68-b868978b59f3
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:41:05 PM
Status         : Succeeded


```

<span data-ttu-id="3018d-115">"MoveResource Name"을 입력으로 사용하여 이동 컬렉션의 리소스 집합을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="3018d-115">Commit the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="3018d-116">예제 3: 입력으로 "SourceARMID"를 사용하여 이동 컬렉션에서 리소스 집합을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="3018d-116">Example 3: Commit the set of resources in the Move Collection using "SourceARMID" as input.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:42:46 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/d36ca519-8ced-48c9-a968-cb5e9c4db731
Message        : 
Name           : d36ca519-8ced-48c9-a968-cb5e9c4db731
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:42:41 PM
Status         : Succeeded


```

<span data-ttu-id="3018d-117">"SourceARMID"를 입력으로 사용하여 이동 컬렉션의 리소스 집합을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="3018d-117">Commit the set of resources in the Move Collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="3018d-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3018d-118">PARAMETERS</span></span>

### <span data-ttu-id="3018d-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3018d-119">-AsJob</span></span>
<span data-ttu-id="3018d-120">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="3018d-120">Run the command as a job</span></span>

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

### <span data-ttu-id="3018d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3018d-121">-DefaultProfile</span></span>
<span data-ttu-id="3018d-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3018d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3018d-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="3018d-123">-MoveCollectionName</span></span>
<span data-ttu-id="3018d-124">이동 컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3018d-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="3018d-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="3018d-125">-MoveResource</span></span>
<span data-ttu-id="3018d-126">입력 형식이 moveResourceInputType 속성을 통해 전환되지 않는 한 리소스 ID의 목록을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3018d-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="3018d-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="3018d-127">-MoveResourceInputType</span></span>
<span data-ttu-id="3018d-128">이동 리소스 입력 유형을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="3018d-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="3018d-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3018d-129">-NoWait</span></span>
<span data-ttu-id="3018d-130">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="3018d-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3018d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3018d-131">-ResourceGroupName</span></span>
<span data-ttu-id="3018d-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3018d-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="3018d-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3018d-133">-SubscriptionId</span></span>
<span data-ttu-id="3018d-134">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3018d-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="3018d-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="3018d-135">-ValidateOnly</span></span>
<span data-ttu-id="3018d-136">작업이 전제 요구 사항을 실행해야 하는지 여부를 나타내는 값을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3018d-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="3018d-137">-확인</span><span class="sxs-lookup"><span data-stu-id="3018d-137">-Confirm</span></span>
<span data-ttu-id="3018d-138">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3018d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3018d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3018d-139">-WhatIf</span></span>
<span data-ttu-id="3018d-140">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3018d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3018d-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3018d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3018d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3018d-142">CommonParameters</span></span>
<span data-ttu-id="3018d-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3018d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3018d-144">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3018d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3018d-145">입력</span><span class="sxs-lookup"><span data-stu-id="3018d-145">INPUTS</span></span>

## <span data-ttu-id="3018d-146">출력</span><span class="sxs-lookup"><span data-stu-id="3018d-146">OUTPUTS</span></span>

### <span data-ttu-id="3018d-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="3018d-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="3018d-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3018d-148">NOTES</span></span>

<span data-ttu-id="3018d-149">별칭</span><span class="sxs-lookup"><span data-stu-id="3018d-149">ALIASES</span></span>

## <span data-ttu-id="3018d-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3018d-150">RELATED LINKS</span></span>

