---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
ms.openlocfilehash: ca39d93f8cafbdf5b8895b6978a7558e1fc5b2a6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214007"
---
# <span data-ttu-id="4536b-101">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="4536b-101">Remove-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="4536b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4536b-102">SYNOPSIS</span></span>
<span data-ttu-id="4536b-103">이동 모음을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="4536b-103">Deletes a move collection.</span></span>

## <span data-ttu-id="4536b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4536b-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4536b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4536b-105">DESCRIPTION</span></span>
<span data-ttu-id="4536b-106">이동 모음을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="4536b-106">Deletes a move collection.</span></span>

## <span data-ttu-id="4536b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4536b-107">EXAMPLES</span></span>

### <span data-ttu-id="4536b-108">예제 1: 지정 된 구독에서 이동 컬렉션 제거</span><span class="sxs-lookup"><span data-stu-id="4536b-108">Example 1: Remove the Move Collection from the specified subscription</span></span>
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

<span data-ttu-id="4536b-109">지정 된 구독에서 이동 컬렉션을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4536b-109">Remove the Move collection from the specified subscription.</span></span>

## <span data-ttu-id="4536b-110">변수</span><span class="sxs-lookup"><span data-stu-id="4536b-110">PARAMETERS</span></span>

### <span data-ttu-id="4536b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4536b-111">-AsJob</span></span>
<span data-ttu-id="4536b-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="4536b-112">Run the command as a job</span></span>

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

### <span data-ttu-id="4536b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4536b-113">-DefaultProfile</span></span>
<span data-ttu-id="4536b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4536b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4536b-115">-이름</span><span class="sxs-lookup"><span data-stu-id="4536b-115">-Name</span></span>
<span data-ttu-id="4536b-116">이동 컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4536b-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="4536b-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4536b-117">-NoWait</span></span>
<span data-ttu-id="4536b-118">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="4536b-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4536b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4536b-119">-PassThru</span></span>
<span data-ttu-id="4536b-120">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4536b-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4536b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4536b-121">-ResourceGroupName</span></span>
<span data-ttu-id="4536b-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4536b-122">The Resource Group Name.</span></span>

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

### <span data-ttu-id="4536b-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4536b-123">-SubscriptionId</span></span>
<span data-ttu-id="4536b-124">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4536b-124">The Subscription ID.</span></span>

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

### <span data-ttu-id="4536b-125">-확인</span><span class="sxs-lookup"><span data-stu-id="4536b-125">-Confirm</span></span>
<span data-ttu-id="4536b-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4536b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4536b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4536b-127">-WhatIf</span></span>
<span data-ttu-id="4536b-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4536b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4536b-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4536b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4536b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4536b-130">CommonParameters</span></span>
<span data-ttu-id="4536b-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4536b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4536b-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4536b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4536b-133">입력</span><span class="sxs-lookup"><span data-stu-id="4536b-133">INPUTS</span></span>

## <span data-ttu-id="4536b-134">출력</span><span class="sxs-lookup"><span data-stu-id="4536b-134">OUTPUTS</span></span>

### <span data-ttu-id="4536b-135">Api20191001Preview를 통해. PowerShell. a. i. i a m-IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="4536b-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="4536b-136">상속자</span><span class="sxs-lookup"><span data-stu-id="4536b-136">NOTES</span></span>

<span data-ttu-id="4536b-137">별칭과</span><span class="sxs-lookup"><span data-stu-id="4536b-137">ALIASES</span></span>

## <span data-ttu-id="4536b-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4536b-138">RELATED LINKS</span></span>

