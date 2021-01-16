---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: f3f38feff8b6d855121a6772cfb56ef0b57cebfd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352286"
---
# <span data-ttu-id="e3c98-101">Remove-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="e3c98-101">Remove-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="e3c98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3c98-102">SYNOPSIS</span></span>
<span data-ttu-id="e3c98-103">대역폭 일정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e3c98-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="e3c98-104">구문</span><span class="sxs-lookup"><span data-stu-id="e3c98-104">SYNTAX</span></span>

### <span data-ttu-id="e3c98-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e3c98-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3c98-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3c98-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3c98-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3c98-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3c98-108">설명</span><span class="sxs-lookup"><span data-stu-id="e3c98-108">DESCRIPTION</span></span>
<span data-ttu-id="e3c98-109">**Remove-AzStackEdgeBandwidthSchedule** cmdlet은 Stack Edge 디바이스에 대한 대역폭 일정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e3c98-109">The **Remove-AzStackEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Stack Edge device.</span></span> 

## <span data-ttu-id="e3c98-110">예제</span><span class="sxs-lookup"><span data-stu-id="e3c98-110">EXAMPLES</span></span>

### <span data-ttu-id="e3c98-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e3c98-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="e3c98-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3c98-112">PARAMETERS</span></span>

### <span data-ttu-id="e3c98-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3c98-113">-AsJob</span></span>
<span data-ttu-id="e3c98-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e3c98-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3c98-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3c98-115">-DefaultProfile</span></span>
<span data-ttu-id="e3c98-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e3c98-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3c98-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e3c98-117">-DeviceName</span></span>
<span data-ttu-id="e3c98-118">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="e3c98-118">Device Name</span></span>

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

### <span data-ttu-id="e3c98-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3c98-119">-InputObject</span></span>
<span data-ttu-id="e3c98-120">입력 개체</span><span class="sxs-lookup"><span data-stu-id="e3c98-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: BandwidthSchedule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3c98-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e3c98-121">-Name</span></span>
<span data-ttu-id="e3c98-122">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="e3c98-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3c98-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3c98-123">-PassThru</span></span>
<span data-ttu-id="e3c98-124">성공한 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e3c98-124">returns true if successful</span></span>

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

### <span data-ttu-id="e3c98-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3c98-125">-ResourceGroupName</span></span>
<span data-ttu-id="e3c98-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e3c98-126">Resource Group Name</span></span>

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

### <span data-ttu-id="e3c98-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3c98-127">-ResourceId</span></span>
<span data-ttu-id="e3c98-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3c98-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="e3c98-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3c98-129">-Confirm</span></span>
<span data-ttu-id="e3c98-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3c98-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3c98-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3c98-131">-WhatIf</span></span>
<span data-ttu-id="e3c98-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e3c98-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3c98-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3c98-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3c98-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3c98-134">CommonParameters</span></span>
<span data-ttu-id="e3c98-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e3c98-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3c98-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e3c98-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3c98-137">입력</span><span class="sxs-lookup"><span data-stu-id="e3c98-137">INPUTS</span></span>

### <span data-ttu-id="e3c98-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e3c98-138">System.String</span></span>

### <span data-ttu-id="e3c98-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="e3c98-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="e3c98-140">출력</span><span class="sxs-lookup"><span data-stu-id="e3c98-140">OUTPUTS</span></span>

### <span data-ttu-id="e3c98-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e3c98-141">System.Boolean</span></span>

## <span data-ttu-id="e3c98-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e3c98-142">NOTES</span></span>

## <span data-ttu-id="e3c98-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3c98-143">RELATED LINKS</span></span>