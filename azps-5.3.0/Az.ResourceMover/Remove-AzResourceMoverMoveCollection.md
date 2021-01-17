---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
ms.openlocfilehash: ca39d93f8cafbdf5b8895b6978a7558e1fc5b2a6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490639"
---
# <span data-ttu-id="9de89-101">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="9de89-101">Remove-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="9de89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9de89-102">SYNOPSIS</span></span>
<span data-ttu-id="9de89-103">이동 컬렉션을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9de89-103">Deletes a move collection.</span></span>

## <span data-ttu-id="9de89-104">구문</span><span class="sxs-lookup"><span data-stu-id="9de89-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9de89-105">설명</span><span class="sxs-lookup"><span data-stu-id="9de89-105">DESCRIPTION</span></span>
<span data-ttu-id="9de89-106">이동 컬렉션을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9de89-106">Deletes a move collection.</span></span>

## <span data-ttu-id="9de89-107">예제</span><span class="sxs-lookup"><span data-stu-id="9de89-107">EXAMPLES</span></span>

### <span data-ttu-id="9de89-108">예제 1: 지정된 구독에서 컬렉션 이동 제거</span><span class="sxs-lookup"><span data-stu-id="9de89-108">Example 1: Remove the Move Collection from the specified subscription</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM"

    AdditionalInfo :
    Code           :
    Detail         :
    EndTime        : 8/12/2020 3:27:28 PM
    Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                    ections/PS-centralus-westcentralus-demoRM/operations/3c2aae83-0a05-432c-be8e-a156351866c5
    Message        :
    Name           : 3c2aae83-0a05-432c-be8e-a156351866d6
    Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
    StartTime      : 8/12/2020 3:27:27 PM
    Status         : Succeeded
```

<span data-ttu-id="9de89-109">지정된 구독에서 컬렉션 이동을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9de89-109">Remove the Move collection from the specified subscription.</span></span>

## <span data-ttu-id="9de89-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9de89-110">PARAMETERS</span></span>

### <span data-ttu-id="9de89-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9de89-111">-AsJob</span></span>
<span data-ttu-id="9de89-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="9de89-112">Run the command as a job</span></span>

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

### <span data-ttu-id="9de89-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9de89-113">-DefaultProfile</span></span>
<span data-ttu-id="9de89-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9de89-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9de89-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9de89-115">-Name</span></span>
<span data-ttu-id="9de89-116">컬렉션 이동 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9de89-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="9de89-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9de89-117">-NoWait</span></span>
<span data-ttu-id="9de89-118">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="9de89-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9de89-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9de89-119">-PassThru</span></span>
<span data-ttu-id="9de89-120">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9de89-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9de89-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9de89-121">-ResourceGroupName</span></span>
<span data-ttu-id="9de89-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9de89-122">The Resource Group Name.</span></span>

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

### <span data-ttu-id="9de89-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9de89-123">-SubscriptionId</span></span>
<span data-ttu-id="9de89-124">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9de89-124">The Subscription ID.</span></span>

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

### <span data-ttu-id="9de89-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9de89-125">-Confirm</span></span>
<span data-ttu-id="9de89-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9de89-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9de89-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9de89-127">-WhatIf</span></span>
<span data-ttu-id="9de89-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9de89-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9de89-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9de89-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9de89-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9de89-130">CommonParameters</span></span>
<span data-ttu-id="9de89-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9de89-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9de89-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9de89-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9de89-133">입력</span><span class="sxs-lookup"><span data-stu-id="9de89-133">INPUTS</span></span>

## <span data-ttu-id="9de89-134">출력</span><span class="sxs-lookup"><span data-stu-id="9de89-134">OUTPUTS</span></span>

### <span data-ttu-id="9de89-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="9de89-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="9de89-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9de89-136">NOTES</span></span>

<span data-ttu-id="9de89-137">별칭</span><span class="sxs-lookup"><span data-stu-id="9de89-137">ALIASES</span></span>

## <span data-ttu-id="9de89-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9de89-138">RELATED LINKS</span></span>

