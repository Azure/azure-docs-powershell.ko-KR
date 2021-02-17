---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/resolve-azresourcemovermovecollectiondependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
ms.openlocfilehash: c37ac4f5db2df62ecf1f76764f69e31f234708e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208533"
---
# <span data-ttu-id="2b897-101">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="2b897-101">Resolve-AzResourceMoverMoveCollectionDependency</span></span>

## <span data-ttu-id="2b897-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b897-102">SYNOPSIS</span></span>
<span data-ttu-id="2b897-103">이동 컬렉션에서 moveResources의 종속성 계산, 확인 및 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="2b897-103">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="2b897-104">구문</span><span class="sxs-lookup"><span data-stu-id="2b897-104">SYNTAX</span></span>

```
Resolve-AzResourceMoverMoveCollectionDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="2b897-105">설명</span><span class="sxs-lookup"><span data-stu-id="2b897-105">DESCRIPTION</span></span>
<span data-ttu-id="2b897-106">이동 컬렉션에서 moveResources의 종속성 계산, 확인 및 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="2b897-106">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="2b897-107">예제</span><span class="sxs-lookup"><span data-stu-id="2b897-107">EXAMPLES</span></span>

### <span data-ttu-id="2b897-108">예제 1: Move 컬렉션에서 moveresources의 종속성 계산, 해결 및 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="2b897-108">Example 1: Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>
```powershell
PS C:\> Resolve-AzResourceMoverMoveCollectionDependency -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM" 

AdditionalInfo : 
Code           : MoveCollectionResolveDependenciesOperationFailed
Detail         : {}
EndTime        : 8/16/2020 2:28:18 PM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveCollections/PS-ce
                 ntralus-westcentralus-demoRM/operations/bce85a10-1ff3-4815-a677-7b188f7b441a
Message        : The resolve dependencies operation of one ore more resources has failed. Check the move status of the resource for more details. 
Possible Causes: The resolve dependencies operation of one ore more resources has failed.
Recommended Action: Retry the operation after resolving errors if any. If issue persists, contact support.
                     
Name           : bce85a10-1ff3-4815-a677-7b188f7b441a
Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/16/2020 2:28:16 PM
Status         : Succeeded
```

<span data-ttu-id="2b897-109">Move 컬렉션에서 moveresources의 종속성에 대한 계산, 확인 및 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="2b897-109">Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>

## <span data-ttu-id="2b897-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b897-110">PARAMETERS</span></span>

### <span data-ttu-id="2b897-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b897-111">-AsJob</span></span>
<span data-ttu-id="2b897-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="2b897-112">Run the command as a job</span></span>

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

### <span data-ttu-id="2b897-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b897-113">-DefaultProfile</span></span>
<span data-ttu-id="2b897-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b897-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b897-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="2b897-115">-MoveCollectionName</span></span>
<span data-ttu-id="2b897-116">컬렉션 이동 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b897-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="2b897-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2b897-117">-NoWait</span></span>
<span data-ttu-id="2b897-118">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="2b897-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2b897-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b897-119">-ResourceGroupName</span></span>
<span data-ttu-id="2b897-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b897-120">The Resource Group Name.</span></span>

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

### <span data-ttu-id="2b897-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2b897-121">-SubscriptionId</span></span>
<span data-ttu-id="2b897-122">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2b897-122">The Subscription ID.</span></span>

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

### <span data-ttu-id="2b897-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b897-123">-Confirm</span></span>
<span data-ttu-id="2b897-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b897-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b897-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b897-125">-WhatIf</span></span>
<span data-ttu-id="2b897-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2b897-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b897-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2b897-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b897-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b897-128">CommonParameters</span></span>
<span data-ttu-id="2b897-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2b897-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b897-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2b897-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b897-131">입력</span><span class="sxs-lookup"><span data-stu-id="2b897-131">INPUTS</span></span>

## <span data-ttu-id="2b897-132">출력</span><span class="sxs-lookup"><span data-stu-id="2b897-132">OUTPUTS</span></span>

### <span data-ttu-id="2b897-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="2b897-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="2b897-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2b897-134">NOTES</span></span>

<span data-ttu-id="2b897-135">별칭</span><span class="sxs-lookup"><span data-stu-id="2b897-135">ALIASES</span></span>

## <span data-ttu-id="2b897-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b897-136">RELATED LINKS</span></span>

