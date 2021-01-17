---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 69a484734dfde2459cf05f6eea763a8433b15827
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343598"
---
# <span data-ttu-id="7573a-101">Remove-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="7573a-101">Remove-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="7573a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7573a-102">SYNOPSIS</span></span>
<span data-ttu-id="7573a-103">Data Box Edge 디바이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7573a-103">Removes a Data Box Edge device.</span></span>

## <span data-ttu-id="7573a-104">구문</span><span class="sxs-lookup"><span data-stu-id="7573a-104">SYNTAX</span></span>

### <span data-ttu-id="7573a-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7573a-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7573a-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7573a-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7573a-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7573a-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -InputObject <PSDataBoxEdgeDevice> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7573a-108">설명</span><span class="sxs-lookup"><span data-stu-id="7573a-108">DESCRIPTION</span></span>
<span data-ttu-id="7573a-109">**Remove-AzDataBoxEdgeDevice** cmdlet은 Data Box Edge 디바이스에 대한 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7573a-109">The **Remove-AzDataBoxEdgeDevice** cmdlet removes the configuration for a Data Box Edge device.</span></span>
<span data-ttu-id="7573a-110">주문한 후 배송을 위해 Microsoft에서 디바이스를 준비하기 전에만 디바이스를 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7573a-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="7573a-111">이 cmdlet을 사용하기 전에 리소스 삭제에 대한 [설명서를 참조하세요.](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span><span class="sxs-lookup"><span data-stu-id="7573a-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="7573a-112">예제</span><span class="sxs-lookup"><span data-stu-id="7573a-112">EXAMPLES</span></span>

### <span data-ttu-id="7573a-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="7573a-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="7573a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7573a-114">PARAMETERS</span></span>

### <span data-ttu-id="7573a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7573a-115">-AsJob</span></span>
<span data-ttu-id="7573a-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7573a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7573a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7573a-117">-DefaultProfile</span></span>
<span data-ttu-id="7573a-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7573a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7573a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7573a-119">-InputObject</span></span>
<span data-ttu-id="7573a-120">입력 개체</span><span class="sxs-lookup"><span data-stu-id="7573a-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7573a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7573a-121">-Name</span></span>
<span data-ttu-id="7573a-122">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="7573a-122">Resource Name</span></span>

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

### <span data-ttu-id="7573a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7573a-123">-PassThru</span></span>
<span data-ttu-id="7573a-124">성공한 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7573a-124">returns true if successful</span></span>

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

### <span data-ttu-id="7573a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7573a-125">-ResourceGroupName</span></span>
<span data-ttu-id="7573a-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="7573a-126">Resource Group Name</span></span>

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

### <span data-ttu-id="7573a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7573a-127">-ResourceId</span></span>
<span data-ttu-id="7573a-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7573a-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="7573a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7573a-129">-Confirm</span></span>
<span data-ttu-id="7573a-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7573a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7573a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7573a-131">-WhatIf</span></span>
<span data-ttu-id="7573a-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7573a-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7573a-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7573a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7573a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7573a-134">CommonParameters</span></span>
<span data-ttu-id="7573a-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7573a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7573a-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7573a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7573a-137">입력</span><span class="sxs-lookup"><span data-stu-id="7573a-137">INPUTS</span></span>

### <span data-ttu-id="7573a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="7573a-138">System.String</span></span>

### <span data-ttu-id="7573a-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="7573a-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="7573a-140">출력</span><span class="sxs-lookup"><span data-stu-id="7573a-140">OUTPUTS</span></span>

### <span data-ttu-id="7573a-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7573a-141">System.Boolean</span></span>

## <span data-ttu-id="7573a-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7573a-142">NOTES</span></span>

## <span data-ttu-id="7573a-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7573a-143">RELATED LINKS</span></span>
