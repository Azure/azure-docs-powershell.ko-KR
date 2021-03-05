---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/remove-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
ms.openlocfilehash: e7659c6437e9566a4793e12518a30067aa73297a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005072"
---
# <span data-ttu-id="6359d-101">Remove-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="6359d-101">Remove-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="6359d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6359d-102">SYNOPSIS</span></span>
<span data-ttu-id="6359d-103">디바이스에서 기존 트리거를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6359d-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="6359d-104">구문</span><span class="sxs-lookup"><span data-stu-id="6359d-104">SYNTAX</span></span>

### <span data-ttu-id="6359d-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6359d-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6359d-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6359d-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6359d-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6359d-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-InputObject] <PSStackEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6359d-108">설명</span><span class="sxs-lookup"><span data-stu-id="6359d-108">DESCRIPTION</span></span>
<span data-ttu-id="6359d-109">**Remove-AzStackEdgeTrigger** cmdlet은 Stack Edge 디바이스에서 기존 트리거를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6359d-109">The **Remove-AzStackEdgeTrigger** cmdlet removes an existing trigger on the Stack Edge device.</span></span>

## <span data-ttu-id="6359d-110">예제</span><span class="sxs-lookup"><span data-stu-id="6359d-110">EXAMPLES</span></span>

### <span data-ttu-id="6359d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6359d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="6359d-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6359d-112">PARAMETERS</span></span>

### <span data-ttu-id="6359d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6359d-113">-AsJob</span></span>
<span data-ttu-id="6359d-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6359d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6359d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6359d-115">-DefaultProfile</span></span>
<span data-ttu-id="6359d-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6359d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6359d-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6359d-117">-DeviceName</span></span>
<span data-ttu-id="6359d-118">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="6359d-118">Device Name</span></span>

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

### <span data-ttu-id="6359d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6359d-119">-InputObject</span></span>
<span data-ttu-id="6359d-120">입력 개체</span><span class="sxs-lookup"><span data-stu-id="6359d-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Trigger

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6359d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6359d-121">-Name</span></span>
<span data-ttu-id="6359d-122">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="6359d-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6359d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6359d-123">-PassThru</span></span>
<span data-ttu-id="6359d-124">성공한 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6359d-124">returns true if successful</span></span>

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

### <span data-ttu-id="6359d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6359d-125">-ResourceGroupName</span></span>
<span data-ttu-id="6359d-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6359d-126">Resource Group Name</span></span>

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

### <span data-ttu-id="6359d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6359d-127">-ResourceId</span></span>
<span data-ttu-id="6359d-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="6359d-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="6359d-129">-확인</span><span class="sxs-lookup"><span data-stu-id="6359d-129">-Confirm</span></span>
<span data-ttu-id="6359d-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6359d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6359d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6359d-131">-WhatIf</span></span>
<span data-ttu-id="6359d-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6359d-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6359d-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6359d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6359d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6359d-134">CommonParameters</span></span>
<span data-ttu-id="6359d-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6359d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6359d-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6359d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6359d-137">입력</span><span class="sxs-lookup"><span data-stu-id="6359d-137">INPUTS</span></span>

### <span data-ttu-id="6359d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="6359d-138">System.String</span></span>

### <span data-ttu-id="6359d-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="6359d-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="6359d-140">출력</span><span class="sxs-lookup"><span data-stu-id="6359d-140">OUTPUTS</span></span>

### <span data-ttu-id="6359d-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6359d-141">System.Boolean</span></span>

## <span data-ttu-id="6359d-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6359d-142">NOTES</span></span>

## <span data-ttu-id="6359d-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6359d-143">RELATED LINKS</span></span>
