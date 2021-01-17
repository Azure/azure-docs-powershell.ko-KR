---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverinitiatemove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
ms.openlocfilehash: c1942358ea438d596afc3f147e65a894b270f0d7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490652"
---
# <span data-ttu-id="ddb2b-101">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="ddb2b-101">Invoke-AzResourceMoverInitiateMove</span></span>

## <span data-ttu-id="ddb2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddb2b-102">SYNOPSIS</span></span>
<span data-ttu-id="ddb2b-103">요청 본문에 포함된 리소스 집합을 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-103">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="ddb2b-104">moveResources가 moveState 'MovePending' 또는 'MoveFailed'에 있는 후 이동 작업이 트리거됩니다. 성공적으로 완료되면 moveResource moveState가 커밋 보류로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-104">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="ddb2b-105">사용자가 작업을 전제로 하는 작업을 지원하기 위해 클라이언트는 validateOnly 속성이 true로 설정된 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="ddb2b-106">구문</span><span class="sxs-lookup"><span data-stu-id="ddb2b-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverInitiateMove -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ddb2b-107">설명</span><span class="sxs-lookup"><span data-stu-id="ddb2b-107">DESCRIPTION</span></span>
<span data-ttu-id="ddb2b-108">요청 본문에 포함된 리소스 집합을 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-108">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="ddb2b-109">moveResources가 moveState 'MovePending' 또는 'MoveFailed'에 있는 후 이동 작업이 트리거됩니다. 성공적으로 완료되면 moveResource moveState가 커밋 보류로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-109">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="ddb2b-110">사용자가 작업을 전제로 하는 작업을 지원하기 위해 클라이언트는 validateOnly 속성이 true로 설정된 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="ddb2b-111">예제</span><span class="sxs-lookup"><span data-stu-id="ddb2b-111">EXAMPLES</span></span>

### <span data-ttu-id="ddb2b-112">예제 1: 리소스에 대한 이동을 시작하기 전에 종속성의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-112">Example 1: Validate the dependecies before Initiate Move for the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg')  -ValidateOnly


AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:07:36 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/8d6fbc01-9e5f-4a62-9bd7-03c18bd770f2
Message        :
Name           : 8d6fbc01-9e5f-4a62-9bd7-03c18bd770f2
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:07:35 AM
Status         : Succeeded

```

<span data-ttu-id="ddb2b-113">리소스에 대한 이동을 시작하기 전에 종속성의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-113">Validate the dependecies before Initiate Move for the resources.</span></span>

### <span data-ttu-id="ddb2b-114">예제 2: 입력으로 "MoveResource Name"을 사용하여 Move 컬렉션의 리소스 집합에 대한 이동 시작</span><span class="sxs-lookup"><span data-stu-id="ddb2b-114">Example 2: Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg') 

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:24:21 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/bc30d933-c2b6-47c9-b583-240d375b5864
Message        :
Name           : bc30d933-c2b6-47c9-b583-240d375b5864
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:24:21 AM
Status         : Succeeded

```

<span data-ttu-id="ddb2b-115">입력으로 "MoveResource Name"을 사용하여 Move 컬렉션의 리소스 집합에 대해 이동을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-115">Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="ddb2b-116">예제 3: 입력으로 "SourceARMID"를 사용하여 이동 컬렉션의 리소스 집합에 대한 이동 시작</span><span class="sxs-lookup"><span data-stu-id="ddb2b-116">Example 3: Initiate Move for the set of resources in the Move Collection using "SourceARMID" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:38:33 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/cbc0f921-de9b-45d5-91da-60e36b841b10
Message        :
Name           : cbc0f921-de9b-45d5-91da-60e36b841b10
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:37:23 AM
Status         : Succeeded

```

<span data-ttu-id="ddb2b-117">입력으로 "SourceARMID"를 사용하여 이동 컬렉션의 리소스 집합에 대해 이동을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-117">Initiate Move for the set of resources in the Move collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="ddb2b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddb2b-118">PARAMETERS</span></span>

### <span data-ttu-id="ddb2b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddb2b-119">-AsJob</span></span>
<span data-ttu-id="ddb2b-120">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="ddb2b-120">Run the command as a job</span></span>

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

### <span data-ttu-id="ddb2b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddb2b-121">-DefaultProfile</span></span>
<span data-ttu-id="ddb2b-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddb2b-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="ddb2b-123">-MoveCollectionName</span></span>
<span data-ttu-id="ddb2b-124">컬렉션 이동 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="ddb2b-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="ddb2b-125">-MoveResource</span></span>
<span data-ttu-id="ddb2b-126">입력 형식이 moveResourceInputType 속성을 통해 전환되지 않는 한 기본적으로 리소스 ID의 목록을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="ddb2b-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="ddb2b-127">-MoveResourceInputType</span></span>
<span data-ttu-id="ddb2b-128">이동 리소스 입력 형식을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="ddb2b-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ddb2b-129">-NoWait</span></span>
<span data-ttu-id="ddb2b-130">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="ddb2b-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ddb2b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddb2b-131">-ResourceGroupName</span></span>
<span data-ttu-id="ddb2b-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="ddb2b-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ddb2b-133">-SubscriptionId</span></span>
<span data-ttu-id="ddb2b-134">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="ddb2b-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="ddb2b-135">-ValidateOnly</span></span>
<span data-ttu-id="ddb2b-136">작업이 사전 요구 사항을 실행해야 하는지 여부를 나타내는 값을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="ddb2b-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ddb2b-137">-Confirm</span></span>
<span data-ttu-id="ddb2b-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddb2b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddb2b-139">-WhatIf</span></span>
<span data-ttu-id="ddb2b-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ddb2b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddb2b-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddb2b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddb2b-142">CommonParameters</span></span>
<span data-ttu-id="ddb2b-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddb2b-144">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddb2b-145">입력</span><span class="sxs-lookup"><span data-stu-id="ddb2b-145">INPUTS</span></span>

## <span data-ttu-id="ddb2b-146">출력</span><span class="sxs-lookup"><span data-stu-id="ddb2b-146">OUTPUTS</span></span>

### <span data-ttu-id="ddb2b-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="ddb2b-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="ddb2b-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ddb2b-148">NOTES</span></span>

<span data-ttu-id="ddb2b-149">별칭</span><span class="sxs-lookup"><span data-stu-id="ddb2b-149">ALIASES</span></span>

## <span data-ttu-id="ddb2b-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ddb2b-150">RELATED LINKS</span></span>

