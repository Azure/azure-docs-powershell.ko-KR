---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
ms.openlocfilehash: f718f3c133f25a8b7fb401bfb9a390724090ccc4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490635"
---
# <span data-ttu-id="ad546-101">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="ad546-101">Remove-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="ad546-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad546-102">SYNOPSIS</span></span>
<span data-ttu-id="ad546-103">이동 컬렉션에서 리소스 이동을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ad546-103">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="ad546-104">구문</span><span class="sxs-lookup"><span data-stu-id="ad546-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ad546-105">설명</span><span class="sxs-lookup"><span data-stu-id="ad546-105">DESCRIPTION</span></span>
<span data-ttu-id="ad546-106">이동 컬렉션에서 리소스 이동을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ad546-106">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="ad546-107">예제</span><span class="sxs-lookup"><span data-stu-id="ad546-107">EXAMPLES</span></span>

### <span data-ttu-id="ad546-108">예제 1: 이동 컬렉션에서 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="ad546-108">Example 1: Remove the resource from the Move collection</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveResource -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -Name "psdemorm"

    AdditionalInfo :
    Code           :
    Detail         :
    EndTime        : 8/11/2020 3:27:28 PM
    Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                     ections/PS-centralus-westcentralus-demoRM/operations/3c2aae83-0a05-432c-be8e-a156351866c5
    Message        :
    Name           : 3c2aae83-0a05-432c-be8e-a156351866c5
    Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
    StartTime      : 8/11/2020 3:27:27 PM
    Status         : Succeeded

```

<span data-ttu-id="ad546-109">지정된 구독 내에서 이동 컬렉션에서 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ad546-109">Remove the resource from the Move collection within the specified subscription.</span></span>

## <span data-ttu-id="ad546-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad546-110">PARAMETERS</span></span>

### <span data-ttu-id="ad546-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad546-111">-AsJob</span></span>
<span data-ttu-id="ad546-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="ad546-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ad546-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad546-113">-DefaultProfile</span></span>
<span data-ttu-id="ad546-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ad546-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad546-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="ad546-115">-MoveCollectionName</span></span>
<span data-ttu-id="ad546-116">컬렉션 이동 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad546-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="ad546-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ad546-117">-Name</span></span>
<span data-ttu-id="ad546-118">리소스 이름 이동</span><span class="sxs-lookup"><span data-stu-id="ad546-118">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad546-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ad546-119">-NoWait</span></span>
<span data-ttu-id="ad546-120">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="ad546-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ad546-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad546-121">-PassThru</span></span>
<span data-ttu-id="ad546-122">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ad546-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ad546-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad546-123">-ResourceGroupName</span></span>
<span data-ttu-id="ad546-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad546-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="ad546-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ad546-125">-SubscriptionId</span></span>
<span data-ttu-id="ad546-126">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ad546-126">The Subscription ID.</span></span>

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

### <span data-ttu-id="ad546-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad546-127">-Confirm</span></span>
<span data-ttu-id="ad546-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad546-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad546-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad546-129">-WhatIf</span></span>
<span data-ttu-id="ad546-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ad546-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad546-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad546-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad546-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad546-132">CommonParameters</span></span>
<span data-ttu-id="ad546-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ad546-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad546-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ad546-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad546-135">입력</span><span class="sxs-lookup"><span data-stu-id="ad546-135">INPUTS</span></span>

## <span data-ttu-id="ad546-136">출력</span><span class="sxs-lookup"><span data-stu-id="ad546-136">OUTPUTS</span></span>

### <span data-ttu-id="ad546-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="ad546-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="ad546-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ad546-138">NOTES</span></span>

<span data-ttu-id="ad546-139">별칭</span><span class="sxs-lookup"><span data-stu-id="ad546-139">ALIASES</span></span>

## <span data-ttu-id="ad546-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad546-140">RELATED LINKS</span></span>

