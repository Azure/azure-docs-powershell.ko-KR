---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemovercommit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
ms.openlocfilehash: 9c0ee11b728c3fd8b1ed2b73e8b144728255a009
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204900"
---
# <span data-ttu-id="3ae70-101">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="3ae70-101">Invoke-AzResourceMoverCommit</span></span>

## <span data-ttu-id="3ae70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ae70-102">SYNOPSIS</span></span>
<span data-ttu-id="3ae70-103">요청 본문에 포함 된 리소스 집합을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="3ae70-103">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="3ae70-104">커밋 작업은 moveState ' CommitPending ' 또는 ' Commitpending '의 moveResources에 대해 트리거 되며 성공적으로 완료 되 면 moveResource moveState가 커밋으로 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3ae70-104">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="3ae70-105">사용자가 작업을 필수 구성 요소에 사용 하는 데 도움이 되도록 클라이언트는 validateOnly 속성이 true로 설정 된 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3ae70-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="3ae70-106">구문과</span><span class="sxs-lookup"><span data-stu-id="3ae70-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverCommit -MoveCollectionName <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3ae70-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3ae70-107">DESCRIPTION</span></span>
<span data-ttu-id="3ae70-108">요청 본문에 포함 된 리소스 집합을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="3ae70-108">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="3ae70-109">커밋 작업은 moveState ' CommitPending ' 또는 ' Commitpending '의 moveResources에 대해 트리거 되며 성공적으로 완료 되 면 moveResource moveState가 커밋으로 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3ae70-109">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="3ae70-110">사용자가 작업을 필수 구성 요소에 사용 하는 데 도움이 되도록 클라이언트는 validateOnly 속성이 true로 설정 된 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3ae70-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="3ae70-111">예제의</span><span class="sxs-lookup"><span data-stu-id="3ae70-111">EXAMPLES</span></span>

### <span data-ttu-id="3ae70-112">예제 1: 리소스를 커밋하기 전에 dependecies의 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="3ae70-112">Example 1: Validate the dependecies before commit of the resources</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResource $('psdemorm') -ValidateOnly


AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:17:00 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Message        :
Name           : 5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:16:59 AM
Status         : Succeeded

```

<span data-ttu-id="3ae70-113">리소스를 커밋하기 전에 dependecies의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ae70-113">Validate the dependecies before commit of the resources.</span></span>

### <span data-ttu-id="3ae70-114">예제 2: "MoveResource Name"을 입력으로 사용 하 여 Move Collection의 리소스 집합 커밋</span><span class="sxs-lookup"><span data-stu-id="3ae70-114">Example 2: Commit the set of resources in the Move Collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverCommit -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResource $('psdemorm')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:17:00 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Message        :
Name           : 5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:16:59 AM
Status         : Succeeded


```

<span data-ttu-id="3ae70-115">"MoveResource Name"을 입력으로 사용 하 여 Move Collection의 리소스 집합을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="3ae70-115">Commit the set of resources in the Move Collection using "MoveResource Name" as input</span></span>

### <span data-ttu-id="3ae70-116">예제 3: "Sourc? Mid"를 입력으로 사용 하 여 Move Collection의 리소스 집합 커밋</span><span class="sxs-lookup"><span data-stu-id="3ae70-116">Example 3: Commit the set of resources in the Move Collection using "SourceARMID" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:19:29 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/aa9e2c4d-2160-4e36-b6fa-7465a3829ae9
Message        :
Name           : aa9e2c4d-2160-4e36-b6fa-7465a3829ae9
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:19:28 AM
Status         : Succeeded


```

<span data-ttu-id="3ae70-117">"Sourc? Mid"를 입력으로 사용 하 여 Move Collection의 리소스 집합을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="3ae70-117">Commit the set of resources in the Move Collection using "SourceARMID" as input</span></span>

## <span data-ttu-id="3ae70-118">변수</span><span class="sxs-lookup"><span data-stu-id="3ae70-118">PARAMETERS</span></span>

### <span data-ttu-id="3ae70-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ae70-119">-AsJob</span></span>
<span data-ttu-id="3ae70-120">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="3ae70-120">Run the command as a job</span></span>

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

### <span data-ttu-id="3ae70-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ae70-121">-DefaultProfile</span></span>
<span data-ttu-id="3ae70-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3ae70-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ae70-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="3ae70-123">-MoveCollectionName</span></span>
<span data-ttu-id="3ae70-124">이동 컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3ae70-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="3ae70-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="3ae70-125">-MoveResource</span></span>
<span data-ttu-id="3ae70-126">리소스 Id의 목록을 가져오거나 설정 합니다. 기본적으로 입력 형식이 moveResourceInputType 속성을 통해 전환 되지 않는 한 리소스 id 이동을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ae70-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="3ae70-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="3ae70-127">-MoveResourceInputType</span></span>
<span data-ttu-id="3ae70-128">리소스 이동 입력 유형을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ae70-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="3ae70-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3ae70-129">-NoWait</span></span>
<span data-ttu-id="3ae70-130">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="3ae70-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3ae70-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ae70-131">-ResourceGroupName</span></span>
<span data-ttu-id="3ae70-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3ae70-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="3ae70-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3ae70-133">-SubscriptionId</span></span>
<span data-ttu-id="3ae70-134">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3ae70-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="3ae70-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="3ae70-135">-ValidateOnly</span></span>
<span data-ttu-id="3ae70-136">작업에서 필수 요소를 사전에만 실행 해야 하는지 여부를 나타내는 값을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ae70-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="3ae70-137">-확인</span><span class="sxs-lookup"><span data-stu-id="3ae70-137">-Confirm</span></span>
<span data-ttu-id="3ae70-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ae70-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ae70-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ae70-139">-WhatIf</span></span>
<span data-ttu-id="3ae70-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3ae70-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ae70-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ae70-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ae70-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ae70-142">CommonParameters</span></span>
<span data-ttu-id="3ae70-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ae70-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ae70-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3ae70-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ae70-145">입력</span><span class="sxs-lookup"><span data-stu-id="3ae70-145">INPUTS</span></span>

## <span data-ttu-id="3ae70-146">출력</span><span class="sxs-lookup"><span data-stu-id="3ae70-146">OUTPUTS</span></span>

### <span data-ttu-id="3ae70-147">Api20191001Preview를 통해. PowerShell. a. i. i a m-IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="3ae70-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="3ae70-148">상속자</span><span class="sxs-lookup"><span data-stu-id="3ae70-148">NOTES</span></span>

<span data-ttu-id="3ae70-149">별칭과</span><span class="sxs-lookup"><span data-stu-id="3ae70-149">ALIASES</span></span>

## <span data-ttu-id="3ae70-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ae70-150">RELATED LINKS</span></span>

