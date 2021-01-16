---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeRole.md
ms.openlocfilehash: b3a99d286c0efcf76dee0c71d8d3b5f4e704ca40
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338493"
---
# <span data-ttu-id="8e562-101">Remove-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="8e562-101">Remove-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="8e562-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e562-102">SYNOPSIS</span></span>
<span data-ttu-id="8e562-103">디바이스에 대한 연결된 IoT 역할을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8e562-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="8e562-104">구문</span><span class="sxs-lookup"><span data-stu-id="8e562-104">SYNTAX</span></span>

### <span data-ttu-id="8e562-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="8e562-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e562-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e562-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e562-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e562-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeRole -InputObject <PSDataBoxEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e562-108">설명</span><span class="sxs-lookup"><span data-stu-id="8e562-108">DESCRIPTION</span></span>
<span data-ttu-id="8e562-109">**Remove-AzDataBoxEdgeRole** cmdlet은 Data Box Edge 디바이스에 대한 연결된 IoT 역할을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8e562-109">The **Remove-AzDataBoxEdgeRole** cmdlet removes the associated IoT role for a Data Box Edge device.</span></span>

## <span data-ttu-id="8e562-110">예제</span><span class="sxs-lookup"><span data-stu-id="8e562-110">EXAMPLES</span></span>

### <span data-ttu-id="8e562-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8e562-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="8e562-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e562-112">PARAMETERS</span></span>

### <span data-ttu-id="8e562-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e562-113">-AsJob</span></span>
<span data-ttu-id="8e562-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8e562-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e562-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e562-115">-DefaultProfile</span></span>
<span data-ttu-id="8e562-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8e562-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e562-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8e562-117">-DeviceName</span></span>
<span data-ttu-id="8e562-118">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="8e562-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e562-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e562-119">-InputObject</span></span>
<span data-ttu-id="8e562-120">입력 개체</span><span class="sxs-lookup"><span data-stu-id="8e562-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e562-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8e562-121">-Name</span></span>
<span data-ttu-id="8e562-122">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="8e562-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e562-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e562-123">-PassThru</span></span>
<span data-ttu-id="8e562-124">성공한 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8e562-124">returns true if successful</span></span>

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

### <span data-ttu-id="8e562-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e562-125">-ResourceGroupName</span></span>
<span data-ttu-id="8e562-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8e562-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e562-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e562-127">-ResourceId</span></span>
<span data-ttu-id="8e562-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e562-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="8e562-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e562-129">-Confirm</span></span>
<span data-ttu-id="8e562-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e562-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e562-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e562-131">-WhatIf</span></span>
<span data-ttu-id="8e562-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8e562-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e562-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e562-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e562-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e562-134">CommonParameters</span></span>
<span data-ttu-id="8e562-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8e562-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e562-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8e562-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e562-137">입력</span><span class="sxs-lookup"><span data-stu-id="8e562-137">INPUTS</span></span>

### <span data-ttu-id="8e562-138">System.String</span><span class="sxs-lookup"><span data-stu-id="8e562-138">System.String</span></span>

### <span data-ttu-id="8e562-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="8e562-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="8e562-140">출력</span><span class="sxs-lookup"><span data-stu-id="8e562-140">OUTPUTS</span></span>

### <span data-ttu-id="8e562-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="8e562-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="8e562-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8e562-142">NOTES</span></span>

## <span data-ttu-id="8e562-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e562-143">RELATED LINKS</span></span>