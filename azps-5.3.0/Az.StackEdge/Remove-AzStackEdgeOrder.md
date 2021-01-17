---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
ms.openlocfilehash: 5effec8ed39f9219bcecba23f6ca3cabaae5cec9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492091"
---
# <span data-ttu-id="71390-101">Remove-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="71390-101">Remove-AzStackEdgeOrder</span></span>

## <span data-ttu-id="71390-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71390-102">SYNOPSIS</span></span>
<span data-ttu-id="71390-103">디바이스의 순서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="71390-103">Removes the order for a device.</span></span>

## <span data-ttu-id="71390-104">구문</span><span class="sxs-lookup"><span data-stu-id="71390-104">SYNTAX</span></span>

### <span data-ttu-id="71390-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="71390-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71390-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="71390-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71390-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="71390-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeOrder -InputObject <PSStackEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71390-108">설명</span><span class="sxs-lookup"><span data-stu-id="71390-108">DESCRIPTION</span></span>
<span data-ttu-id="71390-109">**Remove-AzStackEdgeOrder** cmdlet은 Stack Edge 디바이스에 대한 기존 순서를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="71390-109">The **Remove-AzStackEdgeOrder** cmdlet deletes an existing order for a Stack Edge device.</span></span>

## <span data-ttu-id="71390-110">예제</span><span class="sxs-lookup"><span data-stu-id="71390-110">EXAMPLES</span></span>

### <span data-ttu-id="71390-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="71390-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="71390-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71390-112">PARAMETERS</span></span>

### <span data-ttu-id="71390-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71390-113">-AsJob</span></span>
<span data-ttu-id="71390-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="71390-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71390-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71390-115">-DefaultProfile</span></span>
<span data-ttu-id="71390-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="71390-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71390-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="71390-117">-DeviceName</span></span>
<span data-ttu-id="71390-118">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="71390-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71390-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71390-119">-InputObject</span></span>
<span data-ttu-id="71390-120">입력 개체</span><span class="sxs-lookup"><span data-stu-id="71390-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71390-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71390-121">-PassThru</span></span>
<span data-ttu-id="71390-122">성공한 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="71390-122">returns true if successful</span></span>

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

### <span data-ttu-id="71390-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71390-123">-ResourceGroupName</span></span>
<span data-ttu-id="71390-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="71390-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71390-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71390-125">-ResourceId</span></span>
<span data-ttu-id="71390-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="71390-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71390-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71390-127">-Confirm</span></span>
<span data-ttu-id="71390-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="71390-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71390-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71390-129">-WhatIf</span></span>
<span data-ttu-id="71390-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="71390-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71390-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71390-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71390-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71390-132">CommonParameters</span></span>
<span data-ttu-id="71390-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="71390-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71390-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="71390-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71390-135">입력</span><span class="sxs-lookup"><span data-stu-id="71390-135">INPUTS</span></span>

### <span data-ttu-id="71390-136">System.String</span><span class="sxs-lookup"><span data-stu-id="71390-136">System.String</span></span>

### <span data-ttu-id="71390-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="71390-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="71390-138">출력</span><span class="sxs-lookup"><span data-stu-id="71390-138">OUTPUTS</span></span>

### <span data-ttu-id="71390-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="71390-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="71390-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="71390-140">NOTES</span></span>

## <span data-ttu-id="71390-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71390-141">RELATED LINKS</span></span>
