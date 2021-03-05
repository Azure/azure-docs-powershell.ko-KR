---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/invoke-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
ms.openlocfilehash: fc920e04ce3e031e25b0c27ec0998266f077840c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002944"
---
# <span data-ttu-id="00668-101">Invoke-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="00668-101">Invoke-AzStackEdgeShare</span></span>

## <span data-ttu-id="00668-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00668-102">SYNOPSIS</span></span>
<span data-ttu-id="00668-103">공유에 대한 특정 작업을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="00668-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="00668-104">구문</span><span class="sxs-lookup"><span data-stu-id="00668-104">SYNTAX</span></span>

### <span data-ttu-id="00668-105">InvokeByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="00668-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00668-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="00668-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-RefreshData]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00668-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00668-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00668-108">설명</span><span class="sxs-lookup"><span data-stu-id="00668-108">DESCRIPTION</span></span>
<span data-ttu-id="00668-109">**Invoke-AzStackEdgeShare** cmdlet은 Stack Edge 디바이스의 공유에서 데이터를 새로 고치기 위해 작업을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="00668-109">The **Invoke-AzStackEdgeShare** cmdlet invokes action to refresh data on a share on a Stack Edge device.</span></span>

## <span data-ttu-id="00668-110">예제</span><span class="sxs-lookup"><span data-stu-id="00668-110">EXAMPLES</span></span>

### <span data-ttu-id="00668-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="00668-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="00668-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="00668-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzStackEdgeShare
```

## <span data-ttu-id="00668-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="00668-113">PARAMETERS</span></span>

### <span data-ttu-id="00668-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00668-114">-AsJob</span></span>
<span data-ttu-id="00668-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="00668-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="00668-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00668-116">-DefaultProfile</span></span>
<span data-ttu-id="00668-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="00668-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00668-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="00668-118">-DeviceName</span></span>
<span data-ttu-id="00668-119">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="00668-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00668-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00668-120">-InputObject</span></span>
<span data-ttu-id="00668-121">입력 개체</span><span class="sxs-lookup"><span data-stu-id="00668-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00668-122">-Name</span><span class="sxs-lookup"><span data-stu-id="00668-122">-Name</span></span>
<span data-ttu-id="00668-123">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="00668-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00668-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00668-124">-PassThru</span></span>
<span data-ttu-id="00668-125">성공한 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="00668-125">returns true if successful</span></span>

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

### <span data-ttu-id="00668-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="00668-126">-RefreshData</span></span>
<span data-ttu-id="00668-127">클라우드의 데이터로 메타데이터 공유 새로 고침</span><span class="sxs-lookup"><span data-stu-id="00668-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="00668-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00668-128">-ResourceGroupName</span></span>
<span data-ttu-id="00668-129">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="00668-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00668-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00668-130">-ResourceId</span></span>
<span data-ttu-id="00668-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="00668-131">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00668-132">-확인</span><span class="sxs-lookup"><span data-stu-id="00668-132">-Confirm</span></span>
<span data-ttu-id="00668-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="00668-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00668-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00668-134">-WhatIf</span></span>
<span data-ttu-id="00668-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="00668-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="00668-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00668-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00668-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00668-137">CommonParameters</span></span>
<span data-ttu-id="00668-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="00668-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00668-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00668-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00668-140">입력</span><span class="sxs-lookup"><span data-stu-id="00668-140">INPUTS</span></span>

### <span data-ttu-id="00668-141">System.String</span><span class="sxs-lookup"><span data-stu-id="00668-141">System.String</span></span>

### <span data-ttu-id="00668-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="00668-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="00668-143">출력</span><span class="sxs-lookup"><span data-stu-id="00668-143">OUTPUTS</span></span>

### <span data-ttu-id="00668-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="00668-144">System.Boolean</span></span>

## <span data-ttu-id="00668-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="00668-145">NOTES</span></span>

## <span data-ttu-id="00668-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00668-146">RELATED LINKS</span></span>
