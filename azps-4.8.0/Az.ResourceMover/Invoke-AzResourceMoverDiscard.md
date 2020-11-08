---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverdiscard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
ms.openlocfilehash: c4af588c119cb819fcb87fbc7dbdd869540825ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212690"
---
# <span data-ttu-id="9cb3e-101">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="9cb3e-101">Invoke-AzResourceMoverDiscard</span></span>

## <span data-ttu-id="9cb3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cb3e-102">SYNOPSIS</span></span>
<span data-ttu-id="9cb3e-103">요청 본문에 포함 된 리소스 집합을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cb3e-103">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="9cb3e-104">취소 작업은 moveState ' CommitPending ' 또는 ' DiscardFailed '의 moveResources에 대해 트리거 되며 성공적으로 완료 되 면 moveResource moveState는 MovePending으로 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9cb3e-104">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="9cb3e-105">사용자가 작업을 필수 구성 요소에 사용 하는 데 도움이 되도록 클라이언트는 validateOnly 속성이 true로 설정 된 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9cb3e-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="9cb3e-106">구문과</span><span class="sxs-lookup"><span data-stu-id="9cb3e-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverDiscard -Name <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9cb3e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9cb3e-107">DESCRIPTION</span></span>
<span data-ttu-id="9cb3e-108">요청 본문에 포함 된 리소스 집합을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cb3e-108">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="9cb3e-109">취소 작업은 moveState ' CommitPending ' 또는 ' DiscardFailed '의 moveResources에 대해 트리거 되며 성공적으로 완료 되 면 moveResource moveState는 MovePending으로 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9cb3e-109">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="9cb3e-110">사용자가 작업을 필수 구성 요소에 사용 하는 데 도움이 되도록 클라이언트는 validateOnly 속성이 true로 설정 된 작업을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9cb3e-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="9cb3e-111">예제의</span><span class="sxs-lookup"><span data-stu-id="9cb3e-111">EXAMPLES</span></span>

### <span data-ttu-id="9cb3e-112">예제 1: 리소스를 삭제 하기 전에 dependecies의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cb3e-112">Example 1: Validate the dependecies before Discard of  the resources.</span></span>
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

<span data-ttu-id="9cb3e-113">리소스를 삭제 하기 전에 dependecies의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cb3e-113">Validate the dependecies before Discard of  the resources.</span></span>

### <span data-ttu-id="9cb3e-114">예제 2: "MoveResource Name"을 입력으로 사용 하 여 리소스의 이동을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cb3e-114">Example 2: Discards the move of the resources using "MoveResource Name" as input</span></span>
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

<span data-ttu-id="9cb3e-115">"MoveResource Name"을 입력으로 사용 하 여 리소스의 이동을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cb3e-115">Discards the move of the resources using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="9cb3e-116">예제 3: 입력으로 "Sourc? Mid"를 사용 하 여 리소스의 이동을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cb3e-116">Example 3: Discards the move of the resources using "SourceARMID" as input</span></span>
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

<span data-ttu-id="9cb3e-117">"Sourc? Mid"를 입력으로 사용 하 여 리소스의 이동을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cb3e-117">Discards the move of the resources using "SourceARMID" as input.</span></span>

## <span data-ttu-id="9cb3e-118">변수</span><span class="sxs-lookup"><span data-stu-id="9cb3e-118">PARAMETERS</span></span>

### <span data-ttu-id="9cb3e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9cb3e-119">-AsJob</span></span>
<span data-ttu-id="9cb3e-120">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="9cb3e-120">Run the command as a job</span></span>

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

### <span data-ttu-id="9cb3e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cb3e-121">-DefaultProfile</span></span>
<span data-ttu-id="9cb3e-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9cb3e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cb3e-123">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="9cb3e-123">-MoveResource</span></span>
<span data-ttu-id="9cb3e-124">리소스 Id의 목록을 가져오거나 설정 합니다. 기본적으로 입력 형식이 moveResourceInputType 속성을 통해 전환 되지 않는 한 리소스 id 이동을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cb3e-124">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="9cb3e-125">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="9cb3e-125">-MoveResourceInputType</span></span>
<span data-ttu-id="9cb3e-126">리소스 이동 입력 유형을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cb3e-126">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="9cb3e-127">-이름</span><span class="sxs-lookup"><span data-stu-id="9cb3e-127">-Name</span></span>
<span data-ttu-id="9cb3e-128">이동 컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9cb3e-128">The Move Collection Name.</span></span>

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

### <span data-ttu-id="9cb3e-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9cb3e-129">-NoWait</span></span>
<span data-ttu-id="9cb3e-130">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="9cb3e-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9cb3e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cb3e-131">-ResourceGroupName</span></span>
<span data-ttu-id="9cb3e-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9cb3e-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="9cb3e-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9cb3e-133">-SubscriptionId</span></span>
<span data-ttu-id="9cb3e-134">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9cb3e-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="9cb3e-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="9cb3e-135">-ValidateOnly</span></span>
<span data-ttu-id="9cb3e-136">작업에서 필수 요소를 사전에만 실행 해야 하는지 여부를 나타내는 값을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cb3e-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="9cb3e-137">-확인</span><span class="sxs-lookup"><span data-stu-id="9cb3e-137">-Confirm</span></span>
<span data-ttu-id="9cb3e-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cb3e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cb3e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cb3e-139">-WhatIf</span></span>
<span data-ttu-id="9cb3e-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9cb3e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cb3e-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9cb3e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cb3e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cb3e-142">CommonParameters</span></span>
<span data-ttu-id="9cb3e-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cb3e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cb3e-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9cb3e-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cb3e-145">입력</span><span class="sxs-lookup"><span data-stu-id="9cb3e-145">INPUTS</span></span>

## <span data-ttu-id="9cb3e-146">출력</span><span class="sxs-lookup"><span data-stu-id="9cb3e-146">OUTPUTS</span></span>

### <span data-ttu-id="9cb3e-147">Api20191001Preview를 통해. PowerShell. a. i. i a m-IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="9cb3e-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="9cb3e-148">상속자</span><span class="sxs-lookup"><span data-stu-id="9cb3e-148">NOTES</span></span>

<span data-ttu-id="9cb3e-149">별칭과</span><span class="sxs-lookup"><span data-stu-id="9cb3e-149">ALIASES</span></span>

## <span data-ttu-id="9cb3e-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9cb3e-150">RELATED LINKS</span></span>

