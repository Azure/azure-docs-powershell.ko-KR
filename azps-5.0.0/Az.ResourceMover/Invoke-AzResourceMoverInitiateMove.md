---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverinitiatemove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
ms.openlocfilehash: c1942358ea438d596afc3f147e65a894b270f0d7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309929"
---
# <span data-ttu-id="3a9ed-101">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="3a9ed-101">Invoke-AzResourceMoverInitiateMove</span></span>

## <span data-ttu-id="3a9ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a9ed-102">SYNOPSIS</span></span>
<span data-ttu-id="3a9ed-103">요청 본문에 포함 된 리소스 집합을 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a9ed-103">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="3a9ed-104">이동 작업은 moveResources이 moveState ' MovePending ' 또는 ' MoveFailed '에 있는 후에 트리거 되며 성공적으로 완료 되 면 moveResource moveState가 CommitPending으로 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a9ed-104">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="3a9ed-105">사용자가 작업을 필수 구성 요소에 사용 하는 데 도움이 되도록 클라이언트는 validateOnly 속성이 true로 설정 된 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a9ed-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="3a9ed-106">구문과</span><span class="sxs-lookup"><span data-stu-id="3a9ed-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverInitiateMove -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3a9ed-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3a9ed-107">DESCRIPTION</span></span>
<span data-ttu-id="3a9ed-108">요청 본문에 포함 된 리소스 집합을 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a9ed-108">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="3a9ed-109">이동 작업은 moveResources이 moveState ' MovePending ' 또는 ' MoveFailed '에 있는 후에 트리거 되며 성공적으로 완료 되 면 moveResource moveState가 CommitPending으로 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a9ed-109">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="3a9ed-110">사용자가 작업을 필수 구성 요소에 사용 하는 데 도움이 되도록 클라이언트는 validateOnly 속성이 true로 설정 된 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a9ed-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="3a9ed-111">예제의</span><span class="sxs-lookup"><span data-stu-id="3a9ed-111">EXAMPLES</span></span>

### <span data-ttu-id="3a9ed-112">예제 1: 리소스에 대 한 이동을 시작 하기 전에 dependecies의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a9ed-112">Example 1: Validate the dependecies before Initiate Move for the resources.</span></span>
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

<span data-ttu-id="3a9ed-113">리소스에 대 한 이동을 시작 하기 전에 dependecies의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a9ed-113">Validate the dependecies before Initiate Move for the resources.</span></span>

### <span data-ttu-id="3a9ed-114">예제 2: "MoveResource Name"을 입력으로 사용 하는 Move collection의 리소스 집합에 대해 이동 시작</span><span class="sxs-lookup"><span data-stu-id="3a9ed-114">Example 2: Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input</span></span>
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

<span data-ttu-id="3a9ed-115">"MoveResource Name"을 입력으로 사용 하 여 이동 모음의 리소스 집합에 대 한 이동을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a9ed-115">Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="3a9ed-116">예제 3: "Sourc? Mid"를 입력으로 사용 하 여 Move Collection의 리소스 집합에 대 한 이동 시작</span><span class="sxs-lookup"><span data-stu-id="3a9ed-116">Example 3: Initiate Move for the set of resources in the Move Collection using "SourceARMID" as input</span></span>
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

<span data-ttu-id="3a9ed-117">"Sourc? Mid"를 입력으로 사용 하 여 Move collection의 리소스 집합에 대 한 이동을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a9ed-117">Initiate Move for the set of resources in the Move collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="3a9ed-118">변수</span><span class="sxs-lookup"><span data-stu-id="3a9ed-118">PARAMETERS</span></span>

### <span data-ttu-id="3a9ed-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a9ed-119">-AsJob</span></span>
<span data-ttu-id="3a9ed-120">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="3a9ed-120">Run the command as a job</span></span>

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

### <span data-ttu-id="3a9ed-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a9ed-121">-DefaultProfile</span></span>
<span data-ttu-id="3a9ed-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3a9ed-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a9ed-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="3a9ed-123">-MoveCollectionName</span></span>
<span data-ttu-id="3a9ed-124">이동 컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3a9ed-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="3a9ed-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="3a9ed-125">-MoveResource</span></span>
<span data-ttu-id="3a9ed-126">리소스 Id의 목록을 가져오거나 설정 합니다. 기본적으로 입력 형식이 moveResourceInputType 속성을 통해 전환 되지 않는 한 리소스 id 이동을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a9ed-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="3a9ed-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="3a9ed-127">-MoveResourceInputType</span></span>
<span data-ttu-id="3a9ed-128">리소스 이동 입력 유형을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a9ed-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="3a9ed-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3a9ed-129">-NoWait</span></span>
<span data-ttu-id="3a9ed-130">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="3a9ed-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3a9ed-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a9ed-131">-ResourceGroupName</span></span>
<span data-ttu-id="3a9ed-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3a9ed-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="3a9ed-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3a9ed-133">-SubscriptionId</span></span>
<span data-ttu-id="3a9ed-134">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3a9ed-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="3a9ed-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="3a9ed-135">-ValidateOnly</span></span>
<span data-ttu-id="3a9ed-136">작업에서 필수 요소를 사전에만 실행 해야 하는지 여부를 나타내는 값을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a9ed-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="3a9ed-137">-확인</span><span class="sxs-lookup"><span data-stu-id="3a9ed-137">-Confirm</span></span>
<span data-ttu-id="3a9ed-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a9ed-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a9ed-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a9ed-139">-WhatIf</span></span>
<span data-ttu-id="3a9ed-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3a9ed-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a9ed-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a9ed-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a9ed-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a9ed-142">CommonParameters</span></span>
<span data-ttu-id="3a9ed-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a9ed-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a9ed-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3a9ed-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a9ed-145">입력</span><span class="sxs-lookup"><span data-stu-id="3a9ed-145">INPUTS</span></span>

## <span data-ttu-id="3a9ed-146">출력</span><span class="sxs-lookup"><span data-stu-id="3a9ed-146">OUTPUTS</span></span>

### <span data-ttu-id="3a9ed-147">Api20191001Preview를 통해. PowerShell. a. i. i a m-IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="3a9ed-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="3a9ed-148">상속자</span><span class="sxs-lookup"><span data-stu-id="3a9ed-148">NOTES</span></span>

<span data-ttu-id="3a9ed-149">별칭과</span><span class="sxs-lookup"><span data-stu-id="3a9ed-149">ALIASES</span></span>

## <span data-ttu-id="3a9ed-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a9ed-150">RELATED LINKS</span></span>

