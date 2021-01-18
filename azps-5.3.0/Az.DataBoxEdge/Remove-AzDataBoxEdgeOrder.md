---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 84e17ac36e446d784715c2de38944f7b44d1337d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495682"
---
# <span data-ttu-id="8db8e-101">Remove-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="8db8e-101">Remove-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="8db8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8db8e-102">SYNOPSIS</span></span>
<span data-ttu-id="8db8e-103">디바이스의 순서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8db8e-103">Removes the order for a device.</span></span>

## <span data-ttu-id="8db8e-104">구문</span><span class="sxs-lookup"><span data-stu-id="8db8e-104">SYNTAX</span></span>

### <span data-ttu-id="8db8e-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="8db8e-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8db8e-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8db8e-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8db8e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8db8e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -InputObject <PSDataBoxEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8db8e-108">설명</span><span class="sxs-lookup"><span data-stu-id="8db8e-108">DESCRIPTION</span></span>
<span data-ttu-id="8db8e-109">**Remove-AzDataBoxEdgeOrder** cmdlet은 Data Box Edge 디바이스에 대한 기존 주문을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8db8e-109">The **Remove-AzDataBoxEdgeOrder** cmdlet deletes an existing order for a Data Box Edge device.</span></span>

## <span data-ttu-id="8db8e-110">예제</span><span class="sxs-lookup"><span data-stu-id="8db8e-110">EXAMPLES</span></span>

### <span data-ttu-id="8db8e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8db8e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="8db8e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8db8e-112">PARAMETERS</span></span>

### <span data-ttu-id="8db8e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8db8e-113">-AsJob</span></span>
<span data-ttu-id="8db8e-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8db8e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8db8e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8db8e-115">-DefaultProfile</span></span>
<span data-ttu-id="8db8e-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8db8e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8db8e-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8db8e-117">-DeviceName</span></span>
<span data-ttu-id="8db8e-118">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="8db8e-118">Device Name</span></span>

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

### <span data-ttu-id="8db8e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8db8e-119">-InputObject</span></span>
<span data-ttu-id="8db8e-120">입력 개체</span><span class="sxs-lookup"><span data-stu-id="8db8e-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8db8e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8db8e-121">-PassThru</span></span>
<span data-ttu-id="8db8e-122">성공한 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8db8e-122">returns true if successful</span></span>

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

### <span data-ttu-id="8db8e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8db8e-123">-ResourceGroupName</span></span>
<span data-ttu-id="8db8e-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8db8e-124">Resource Group Name</span></span>

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

### <span data-ttu-id="8db8e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8db8e-125">-ResourceId</span></span>
<span data-ttu-id="8db8e-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8db8e-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="8db8e-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8db8e-127">-Confirm</span></span>
<span data-ttu-id="8db8e-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8db8e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8db8e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8db8e-129">-WhatIf</span></span>
<span data-ttu-id="8db8e-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8db8e-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8db8e-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8db8e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8db8e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8db8e-132">CommonParameters</span></span>
<span data-ttu-id="8db8e-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8db8e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8db8e-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8db8e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8db8e-135">입력</span><span class="sxs-lookup"><span data-stu-id="8db8e-135">INPUTS</span></span>

### <span data-ttu-id="8db8e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8db8e-136">System.String</span></span>

### <span data-ttu-id="8db8e-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="8db8e-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="8db8e-138">출력</span><span class="sxs-lookup"><span data-stu-id="8db8e-138">OUTPUTS</span></span>

### <span data-ttu-id="8db8e-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="8db8e-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="8db8e-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8db8e-140">NOTES</span></span>

## <span data-ttu-id="8db8e-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8db8e-141">RELATED LINKS</span></span>
