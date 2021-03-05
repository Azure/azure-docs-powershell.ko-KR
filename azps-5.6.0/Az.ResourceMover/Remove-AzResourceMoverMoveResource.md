---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/remove-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
ms.openlocfilehash: fc146f4d7581db84b79df82055faf2cdd8b000e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999856"
---
# <span data-ttu-id="15d43-101">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="15d43-101">Remove-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="15d43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15d43-102">SYNOPSIS</span></span>
<span data-ttu-id="15d43-103">이동 컬렉션에서 리소스 이동을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="15d43-103">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="15d43-104">구문</span><span class="sxs-lookup"><span data-stu-id="15d43-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="15d43-105">설명</span><span class="sxs-lookup"><span data-stu-id="15d43-105">DESCRIPTION</span></span>
<span data-ttu-id="15d43-106">이동 컬렉션에서 리소스 이동을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="15d43-106">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="15d43-107">예제</span><span class="sxs-lookup"><span data-stu-id="15d43-107">EXAMPLES</span></span>

### <span data-ttu-id="15d43-108">예제 1: 이동 컬렉션에서 Rresource 이동 하나를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="15d43-108">Example 1: Remove one Move Rresource from the Move Collection.</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveResource -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -Name "psdemorm-vnet"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 1:08:49 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/bee69758-c7cb-4160-b3e0-8e4b69ec3731
Message        : 
Name           : bee69758-c7cb-4160-b3e0-8e4b69ec3731
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 1:08:47 PM
Status         : Succeeded

```

<span data-ttu-id="15d43-109">이동 컬렉션에서 Rresource 이동 하나를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="15d43-109">Remove one Move Rresource from the Move Collection.</span></span>

## <span data-ttu-id="15d43-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="15d43-110">PARAMETERS</span></span>

### <span data-ttu-id="15d43-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15d43-111">-AsJob</span></span>
<span data-ttu-id="15d43-112">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="15d43-112">Run the command as a job</span></span>

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

### <span data-ttu-id="15d43-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15d43-113">-DefaultProfile</span></span>
<span data-ttu-id="15d43-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="15d43-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15d43-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="15d43-115">-MoveCollectionName</span></span>
<span data-ttu-id="15d43-116">이동 컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15d43-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="15d43-117">-Name</span><span class="sxs-lookup"><span data-stu-id="15d43-117">-Name</span></span>
<span data-ttu-id="15d43-118">리소스 이름 이동.</span><span class="sxs-lookup"><span data-stu-id="15d43-118">The Move Resource Name.</span></span>

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

### <span data-ttu-id="15d43-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="15d43-119">-NoWait</span></span>
<span data-ttu-id="15d43-120">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="15d43-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="15d43-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15d43-121">-PassThru</span></span>
<span data-ttu-id="15d43-122">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="15d43-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="15d43-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15d43-123">-ResourceGroupName</span></span>
<span data-ttu-id="15d43-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15d43-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="15d43-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="15d43-125">-SubscriptionId</span></span>
<span data-ttu-id="15d43-126">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="15d43-126">The Subscription ID.</span></span>

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

### <span data-ttu-id="15d43-127">-확인</span><span class="sxs-lookup"><span data-stu-id="15d43-127">-Confirm</span></span>
<span data-ttu-id="15d43-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="15d43-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15d43-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15d43-129">-WhatIf</span></span>
<span data-ttu-id="15d43-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="15d43-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15d43-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15d43-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15d43-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15d43-132">CommonParameters</span></span>
<span data-ttu-id="15d43-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="15d43-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15d43-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15d43-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15d43-135">입력</span><span class="sxs-lookup"><span data-stu-id="15d43-135">INPUTS</span></span>

## <span data-ttu-id="15d43-136">출력</span><span class="sxs-lookup"><span data-stu-id="15d43-136">OUTPUTS</span></span>

### <span data-ttu-id="15d43-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="15d43-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="15d43-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="15d43-138">NOTES</span></span>

<span data-ttu-id="15d43-139">별칭</span><span class="sxs-lookup"><span data-stu-id="15d43-139">ALIASES</span></span>

## <span data-ttu-id="15d43-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="15d43-140">RELATED LINKS</span></span>

