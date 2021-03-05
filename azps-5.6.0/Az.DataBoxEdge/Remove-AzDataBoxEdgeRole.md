---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeRole.md
ms.openlocfilehash: bf0c995081e98f3c3e79af2aec8da5144c3e2e32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998545"
---
# <span data-ttu-id="e8807-101">Remove-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="e8807-101">Remove-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="e8807-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8807-102">SYNOPSIS</span></span>
<span data-ttu-id="e8807-103">디바이스에 대한 연결된 IoT 역할을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e8807-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="e8807-104">구문</span><span class="sxs-lookup"><span data-stu-id="e8807-104">SYNTAX</span></span>

### <span data-ttu-id="e8807-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e8807-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8807-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8807-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8807-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8807-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeRole -InputObject <PSDataBoxEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8807-108">설명</span><span class="sxs-lookup"><span data-stu-id="e8807-108">DESCRIPTION</span></span>
<span data-ttu-id="e8807-109">**Remove-AzDataBoxEdgeRole** cmdlet은 Data Box Edge 디바이스에 대한 연결된 IoT 역할을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e8807-109">The **Remove-AzDataBoxEdgeRole** cmdlet removes the associated IoT role for a Data Box Edge device.</span></span>

## <span data-ttu-id="e8807-110">예제</span><span class="sxs-lookup"><span data-stu-id="e8807-110">EXAMPLES</span></span>

### <span data-ttu-id="e8807-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e8807-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="e8807-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e8807-112">PARAMETERS</span></span>

### <span data-ttu-id="e8807-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8807-113">-AsJob</span></span>
<span data-ttu-id="e8807-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e8807-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e8807-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8807-115">-DefaultProfile</span></span>
<span data-ttu-id="e8807-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e8807-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8807-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e8807-117">-DeviceName</span></span>
<span data-ttu-id="e8807-118">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="e8807-118">Device Name</span></span>

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

### <span data-ttu-id="e8807-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8807-119">-InputObject</span></span>
<span data-ttu-id="e8807-120">입력 개체</span><span class="sxs-lookup"><span data-stu-id="e8807-120">Input Object</span></span>

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

### <span data-ttu-id="e8807-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e8807-121">-Name</span></span>
<span data-ttu-id="e8807-122">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="e8807-122">Resource Name</span></span>

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

### <span data-ttu-id="e8807-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8807-123">-PassThru</span></span>
<span data-ttu-id="e8807-124">성공한 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e8807-124">returns true if successful</span></span>

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

### <span data-ttu-id="e8807-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8807-125">-ResourceGroupName</span></span>
<span data-ttu-id="e8807-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e8807-126">Resource Group Name</span></span>

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

### <span data-ttu-id="e8807-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8807-127">-ResourceId</span></span>
<span data-ttu-id="e8807-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8807-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="e8807-129">-확인</span><span class="sxs-lookup"><span data-stu-id="e8807-129">-Confirm</span></span>
<span data-ttu-id="e8807-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8807-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8807-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8807-131">-WhatIf</span></span>
<span data-ttu-id="e8807-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e8807-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8807-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8807-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8807-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8807-134">CommonParameters</span></span>
<span data-ttu-id="e8807-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e8807-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8807-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8807-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8807-137">입력</span><span class="sxs-lookup"><span data-stu-id="e8807-137">INPUTS</span></span>

### <span data-ttu-id="e8807-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e8807-138">System.String</span></span>

### <span data-ttu-id="e8807-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="e8807-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="e8807-140">출력</span><span class="sxs-lookup"><span data-stu-id="e8807-140">OUTPUTS</span></span>

### <span data-ttu-id="e8807-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="e8807-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="e8807-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e8807-142">NOTES</span></span>

## <span data-ttu-id="e8807-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e8807-143">RELATED LINKS</span></span>
