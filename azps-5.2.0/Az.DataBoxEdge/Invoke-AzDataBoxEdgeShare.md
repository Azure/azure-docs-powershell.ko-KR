---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
ms.openlocfilehash: c3fa71b6fb54f359f035f4f6c2f18789ff24b3ac
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356945"
---
# <span data-ttu-id="a4b75-101">Invoke-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="a4b75-101">Invoke-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="a4b75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4b75-102">SYNOPSIS</span></span>
<span data-ttu-id="a4b75-103">공유에 대한 특정 작업을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="a4b75-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="a4b75-104">구문</span><span class="sxs-lookup"><span data-stu-id="a4b75-104">SYNTAX</span></span>

### <span data-ttu-id="a4b75-105">InvokeByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a4b75-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4b75-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4b75-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4b75-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4b75-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4b75-108">설명</span><span class="sxs-lookup"><span data-stu-id="a4b75-108">DESCRIPTION</span></span>
<span data-ttu-id="a4b75-109">**Invoke-AzDataBoxEdgeShare** cmdlet은 Data Box Edge 디바이스의 공유에서 데이터를 새로 고치기 위해 작업을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="a4b75-109">The **Invoke-AzDataBoxEdgeShare** cmdlet invokes action to refresh data on a share on a Data Box Edge device.</span></span>

## <span data-ttu-id="a4b75-110">예제</span><span class="sxs-lookup"><span data-stu-id="a4b75-110">EXAMPLES</span></span>

### <span data-ttu-id="a4b75-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a4b75-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="a4b75-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="a4b75-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzDataBoxEdgeShare
```

## <span data-ttu-id="a4b75-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4b75-113">PARAMETERS</span></span>

### <span data-ttu-id="a4b75-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4b75-114">-AsJob</span></span>
<span data-ttu-id="a4b75-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a4b75-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4b75-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4b75-116">-DefaultProfile</span></span>
<span data-ttu-id="a4b75-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a4b75-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4b75-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a4b75-118">-DeviceName</span></span>
<span data-ttu-id="a4b75-119">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="a4b75-119">Device Name</span></span>

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

### <span data-ttu-id="a4b75-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4b75-120">-InputObject</span></span>
<span data-ttu-id="a4b75-121">입력 개체</span><span class="sxs-lookup"><span data-stu-id="a4b75-121">Input Object</span></span>

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

### <span data-ttu-id="a4b75-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a4b75-122">-Name</span></span>
<span data-ttu-id="a4b75-123">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="a4b75-123">Resource Name</span></span>

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

### <span data-ttu-id="a4b75-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4b75-124">-PassThru</span></span>
<span data-ttu-id="a4b75-125">성공한 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a4b75-125">returns true if successful</span></span>

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

### <span data-ttu-id="a4b75-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="a4b75-126">-RefreshData</span></span>
<span data-ttu-id="a4b75-127">클라우드의 데이터를 사용하여 공유 메타데이터 새로 고침</span><span class="sxs-lookup"><span data-stu-id="a4b75-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="a4b75-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4b75-128">-ResourceGroupName</span></span>
<span data-ttu-id="a4b75-129">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="a4b75-129">Resource Group Name</span></span>

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

### <span data-ttu-id="a4b75-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4b75-130">-ResourceId</span></span>
<span data-ttu-id="a4b75-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4b75-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="a4b75-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4b75-132">-Confirm</span></span>
<span data-ttu-id="a4b75-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4b75-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4b75-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4b75-134">-WhatIf</span></span>
<span data-ttu-id="a4b75-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a4b75-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a4b75-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4b75-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4b75-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4b75-137">CommonParameters</span></span>
<span data-ttu-id="a4b75-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a4b75-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4b75-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a4b75-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4b75-140">입력</span><span class="sxs-lookup"><span data-stu-id="a4b75-140">INPUTS</span></span>

### <span data-ttu-id="a4b75-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a4b75-141">System.String</span></span>

### <span data-ttu-id="a4b75-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="a4b75-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="a4b75-143">출력</span><span class="sxs-lookup"><span data-stu-id="a4b75-143">OUTPUTS</span></span>

### <span data-ttu-id="a4b75-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a4b75-144">System.Boolean</span></span>

## <span data-ttu-id="a4b75-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a4b75-145">NOTES</span></span>

## <span data-ttu-id="a4b75-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a4b75-146">RELATED LINKS</span></span>
