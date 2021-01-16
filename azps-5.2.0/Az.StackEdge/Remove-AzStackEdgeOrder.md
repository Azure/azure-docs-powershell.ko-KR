---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
ms.openlocfilehash: 5effec8ed39f9219bcecba23f6ca3cabaae5cec9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358744"
---
# <span data-ttu-id="f0b21-101">Remove-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="f0b21-101">Remove-AzStackEdgeOrder</span></span>

## <span data-ttu-id="f0b21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0b21-102">SYNOPSIS</span></span>
<span data-ttu-id="f0b21-103">디바이스의 순서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b21-103">Removes the order for a device.</span></span>

## <span data-ttu-id="f0b21-104">구문</span><span class="sxs-lookup"><span data-stu-id="f0b21-104">SYNTAX</span></span>

### <span data-ttu-id="f0b21-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f0b21-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0b21-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0b21-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0b21-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0b21-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeOrder -InputObject <PSStackEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0b21-108">설명</span><span class="sxs-lookup"><span data-stu-id="f0b21-108">DESCRIPTION</span></span>
<span data-ttu-id="f0b21-109">**Remove-AzStackEdgeOrder** cmdlet은 Stack Edge 디바이스에 대한 기존 순서를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b21-109">The **Remove-AzStackEdgeOrder** cmdlet deletes an existing order for a Stack Edge device.</span></span>

## <span data-ttu-id="f0b21-110">예제</span><span class="sxs-lookup"><span data-stu-id="f0b21-110">EXAMPLES</span></span>

### <span data-ttu-id="f0b21-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f0b21-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="f0b21-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0b21-112">PARAMETERS</span></span>

### <span data-ttu-id="f0b21-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0b21-113">-AsJob</span></span>
<span data-ttu-id="f0b21-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f0b21-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0b21-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0b21-115">-DefaultProfile</span></span>
<span data-ttu-id="f0b21-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f0b21-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0b21-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f0b21-117">-DeviceName</span></span>
<span data-ttu-id="f0b21-118">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="f0b21-118">Device Name</span></span>

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

### <span data-ttu-id="f0b21-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0b21-119">-InputObject</span></span>
<span data-ttu-id="f0b21-120">입력 개체</span><span class="sxs-lookup"><span data-stu-id="f0b21-120">Input Object</span></span>

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

### <span data-ttu-id="f0b21-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0b21-121">-PassThru</span></span>
<span data-ttu-id="f0b21-122">성공한 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b21-122">returns true if successful</span></span>

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

### <span data-ttu-id="f0b21-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0b21-123">-ResourceGroupName</span></span>
<span data-ttu-id="f0b21-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f0b21-124">Resource Group Name</span></span>

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

### <span data-ttu-id="f0b21-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0b21-125">-ResourceId</span></span>
<span data-ttu-id="f0b21-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0b21-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="f0b21-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0b21-127">-Confirm</span></span>
<span data-ttu-id="f0b21-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0b21-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0b21-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0b21-129">-WhatIf</span></span>
<span data-ttu-id="f0b21-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f0b21-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0b21-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0b21-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0b21-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0b21-132">CommonParameters</span></span>
<span data-ttu-id="f0b21-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f0b21-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0b21-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f0b21-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0b21-135">입력</span><span class="sxs-lookup"><span data-stu-id="f0b21-135">INPUTS</span></span>

### <span data-ttu-id="f0b21-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f0b21-136">System.String</span></span>

### <span data-ttu-id="f0b21-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="f0b21-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="f0b21-138">출력</span><span class="sxs-lookup"><span data-stu-id="f0b21-138">OUTPUTS</span></span>

### <span data-ttu-id="f0b21-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="f0b21-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="f0b21-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f0b21-140">NOTES</span></span>

## <span data-ttu-id="f0b21-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f0b21-141">RELATED LINKS</span></span>
