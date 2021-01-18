---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
ms.openlocfilehash: c3fa71b6fb54f359f035f4f6c2f18789ff24b3ac
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495696"
---
# <span data-ttu-id="ab0e5-101">Invoke-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="ab0e5-101">Invoke-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="ab0e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab0e5-102">SYNOPSIS</span></span>
<span data-ttu-id="ab0e5-103">공유에 대한 특정 작업을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="ab0e5-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="ab0e5-104">구문</span><span class="sxs-lookup"><span data-stu-id="ab0e5-104">SYNTAX</span></span>

### <span data-ttu-id="ab0e5-105">InvokeByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ab0e5-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab0e5-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab0e5-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab0e5-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab0e5-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab0e5-108">설명</span><span class="sxs-lookup"><span data-stu-id="ab0e5-108">DESCRIPTION</span></span>
<span data-ttu-id="ab0e5-109">**Invoke-AzDataBoxEdgeShare** cmdlet은 Data Box Edge 디바이스의 공유에서 데이터를 새로 고치기 위해 작업을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="ab0e5-109">The **Invoke-AzDataBoxEdgeShare** cmdlet invokes action to refresh data on a share on a Data Box Edge device.</span></span>

## <span data-ttu-id="ab0e5-110">예제</span><span class="sxs-lookup"><span data-stu-id="ab0e5-110">EXAMPLES</span></span>

### <span data-ttu-id="ab0e5-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ab0e5-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="ab0e5-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="ab0e5-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzDataBoxEdgeShare
```

## <span data-ttu-id="ab0e5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab0e5-113">PARAMETERS</span></span>

### <span data-ttu-id="ab0e5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab0e5-114">-AsJob</span></span>
<span data-ttu-id="ab0e5-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ab0e5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ab0e5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab0e5-116">-DefaultProfile</span></span>
<span data-ttu-id="ab0e5-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ab0e5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab0e5-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ab0e5-118">-DeviceName</span></span>
<span data-ttu-id="ab0e5-119">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="ab0e5-119">Device Name</span></span>

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

### <span data-ttu-id="ab0e5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab0e5-120">-InputObject</span></span>
<span data-ttu-id="ab0e5-121">입력 개체</span><span class="sxs-lookup"><span data-stu-id="ab0e5-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab0e5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ab0e5-122">-Name</span></span>
<span data-ttu-id="ab0e5-123">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="ab0e5-123">Resource Name</span></span>

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

### <span data-ttu-id="ab0e5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab0e5-124">-PassThru</span></span>
<span data-ttu-id="ab0e5-125">성공한 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ab0e5-125">returns true if successful</span></span>

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

### <span data-ttu-id="ab0e5-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="ab0e5-126">-RefreshData</span></span>
<span data-ttu-id="ab0e5-127">클라우드의 데이터를 사용하여 공유 메타데이터 새로 고침</span><span class="sxs-lookup"><span data-stu-id="ab0e5-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="ab0e5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab0e5-128">-ResourceGroupName</span></span>
<span data-ttu-id="ab0e5-129">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ab0e5-129">Resource Group Name</span></span>

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

### <span data-ttu-id="ab0e5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab0e5-130">-ResourceId</span></span>
<span data-ttu-id="ab0e5-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab0e5-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="ab0e5-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab0e5-132">-Confirm</span></span>
<span data-ttu-id="ab0e5-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab0e5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab0e5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab0e5-134">-WhatIf</span></span>
<span data-ttu-id="ab0e5-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ab0e5-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab0e5-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab0e5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab0e5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab0e5-137">CommonParameters</span></span>
<span data-ttu-id="ab0e5-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ab0e5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab0e5-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ab0e5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab0e5-140">입력</span><span class="sxs-lookup"><span data-stu-id="ab0e5-140">INPUTS</span></span>

### <span data-ttu-id="ab0e5-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ab0e5-141">System.String</span></span>

### <span data-ttu-id="ab0e5-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="ab0e5-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="ab0e5-143">출력</span><span class="sxs-lookup"><span data-stu-id="ab0e5-143">OUTPUTS</span></span>

### <span data-ttu-id="ab0e5-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ab0e5-144">System.Boolean</span></span>

## <span data-ttu-id="ab0e5-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ab0e5-145">NOTES</span></span>

## <span data-ttu-id="ab0e5-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab0e5-146">RELATED LINKS</span></span>
