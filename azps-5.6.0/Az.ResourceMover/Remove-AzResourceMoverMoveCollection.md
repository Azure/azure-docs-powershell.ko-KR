---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/remove-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
ms.openlocfilehash: aa34a094631441c1ee13418d4d40306715c934b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999883"
---
# <span data-ttu-id="89c0a-101">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="89c0a-101">Remove-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="89c0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89c0a-102">SYNOPSIS</span></span>
<span data-ttu-id="89c0a-103">이동 컬렉션을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="89c0a-103">Deletes a move collection.</span></span>

## <span data-ttu-id="89c0a-104">구문</span><span class="sxs-lookup"><span data-stu-id="89c0a-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="89c0a-105">설명</span><span class="sxs-lookup"><span data-stu-id="89c0a-105">DESCRIPTION</span></span>
<span data-ttu-id="89c0a-106">이동 컬렉션을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="89c0a-106">Deletes a move collection.</span></span>

## <span data-ttu-id="89c0a-107">예제</span><span class="sxs-lookup"><span data-stu-id="89c0a-107">EXAMPLES</span></span>

### <span data-ttu-id="89c0a-108">예제 1: 이동 컬렉션을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="89c0a-108">Example 1: Remove the Move Collection.</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/ec788761-2f1b-46a2-97b7-f5056afd334d
Message        : 
Name           : 
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 
Status         : Succeeded
```

<span data-ttu-id="89c0a-109">이동 컬렉션을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="89c0a-109">Remove the Move Collection.</span></span>

## <span data-ttu-id="89c0a-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="89c0a-110">PARAMETERS</span></span>

### <span data-ttu-id="89c0a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89c0a-111">-AsJob</span></span>
<span data-ttu-id="89c0a-112">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="89c0a-112">Run the command as a job</span></span>

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

### <span data-ttu-id="89c0a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89c0a-113">-DefaultProfile</span></span>
<span data-ttu-id="89c0a-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="89c0a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89c0a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="89c0a-115">-Name</span></span>
<span data-ttu-id="89c0a-116">이동 컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="89c0a-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="89c0a-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="89c0a-117">-NoWait</span></span>
<span data-ttu-id="89c0a-118">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="89c0a-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="89c0a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89c0a-119">-PassThru</span></span>
<span data-ttu-id="89c0a-120">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="89c0a-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="89c0a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89c0a-121">-ResourceGroupName</span></span>
<span data-ttu-id="89c0a-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="89c0a-122">The Resource Group Name.</span></span>

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

### <span data-ttu-id="89c0a-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="89c0a-123">-SubscriptionId</span></span>
<span data-ttu-id="89c0a-124">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="89c0a-124">The Subscription ID.</span></span>

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

### <span data-ttu-id="89c0a-125">-확인</span><span class="sxs-lookup"><span data-stu-id="89c0a-125">-Confirm</span></span>
<span data-ttu-id="89c0a-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="89c0a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89c0a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89c0a-127">-WhatIf</span></span>
<span data-ttu-id="89c0a-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="89c0a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89c0a-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="89c0a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89c0a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89c0a-130">CommonParameters</span></span>
<span data-ttu-id="89c0a-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="89c0a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89c0a-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89c0a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89c0a-133">입력</span><span class="sxs-lookup"><span data-stu-id="89c0a-133">INPUTS</span></span>

## <span data-ttu-id="89c0a-134">출력</span><span class="sxs-lookup"><span data-stu-id="89c0a-134">OUTPUTS</span></span>

### <span data-ttu-id="89c0a-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="89c0a-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="89c0a-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="89c0a-136">NOTES</span></span>

<span data-ttu-id="89c0a-137">별칭</span><span class="sxs-lookup"><span data-stu-id="89c0a-137">ALIASES</span></span>

## <span data-ttu-id="89c0a-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89c0a-138">RELATED LINKS</span></span>

