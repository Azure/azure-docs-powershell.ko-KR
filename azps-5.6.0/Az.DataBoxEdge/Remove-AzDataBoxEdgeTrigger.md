---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: 2e1b3e3db319f724e22673e4139b4cb290879d50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004288"
---
# <span data-ttu-id="2f058-101">Remove-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="2f058-101">Remove-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="2f058-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f058-102">SYNOPSIS</span></span>
<span data-ttu-id="2f058-103">디바이스에서 기존 트리거를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2f058-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="2f058-104">구문</span><span class="sxs-lookup"><span data-stu-id="2f058-104">SYNTAX</span></span>

### <span data-ttu-id="2f058-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="2f058-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f058-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f058-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f058-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f058-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-InputObject] <PSDataBoxEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f058-108">설명</span><span class="sxs-lookup"><span data-stu-id="2f058-108">DESCRIPTION</span></span>
<span data-ttu-id="2f058-109">**Remove-AzDataBoxEdgeTrigger** cmdlet은 Data Box Edge 디바이스에서 기존 트리거를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2f058-109">The **Remove-AzDataBoxEdgeTrigger** cmdlet removes an existing trigger on the Data Box Edge device.</span></span>

## <span data-ttu-id="2f058-110">예제</span><span class="sxs-lookup"><span data-stu-id="2f058-110">EXAMPLES</span></span>

### <span data-ttu-id="2f058-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2f058-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="2f058-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2f058-112">PARAMETERS</span></span>

### <span data-ttu-id="2f058-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f058-113">-AsJob</span></span>
<span data-ttu-id="2f058-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2f058-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f058-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f058-115">-DefaultProfile</span></span>
<span data-ttu-id="2f058-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2f058-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f058-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="2f058-117">-DeviceName</span></span>
<span data-ttu-id="2f058-118">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="2f058-118">Device Name</span></span>

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

### <span data-ttu-id="2f058-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f058-119">-InputObject</span></span>
<span data-ttu-id="2f058-120">입력 개체</span><span class="sxs-lookup"><span data-stu-id="2f058-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f058-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2f058-121">-Name</span></span>
<span data-ttu-id="2f058-122">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="2f058-122">Resource Name</span></span>

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

### <span data-ttu-id="2f058-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f058-123">-PassThru</span></span>
<span data-ttu-id="2f058-124">성공한 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="2f058-124">returns true if successful</span></span>

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

### <span data-ttu-id="2f058-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f058-125">-ResourceGroupName</span></span>
<span data-ttu-id="2f058-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2f058-126">Resource Group Name</span></span>

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

### <span data-ttu-id="2f058-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f058-127">-ResourceId</span></span>
<span data-ttu-id="2f058-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f058-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f058-129">-확인</span><span class="sxs-lookup"><span data-stu-id="2f058-129">-Confirm</span></span>
<span data-ttu-id="2f058-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2f058-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f058-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f058-131">-WhatIf</span></span>
<span data-ttu-id="2f058-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2f058-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f058-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2f058-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f058-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f058-134">CommonParameters</span></span>
<span data-ttu-id="2f058-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2f058-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f058-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f058-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f058-137">입력</span><span class="sxs-lookup"><span data-stu-id="2f058-137">INPUTS</span></span>

### <span data-ttu-id="2f058-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2f058-138">System.String</span></span>

### <span data-ttu-id="2f058-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="2f058-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="2f058-140">출력</span><span class="sxs-lookup"><span data-stu-id="2f058-140">OUTPUTS</span></span>

### <span data-ttu-id="2f058-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2f058-141">System.Boolean</span></span>

## <span data-ttu-id="2f058-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2f058-142">NOTES</span></span>

## <span data-ttu-id="2f058-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f058-143">RELATED LINKS</span></span>
