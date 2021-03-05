---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 1f2c2e2bf02718053d3656b084f845f40215aceb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988302"
---
# <span data-ttu-id="1b0bd-101">Remove-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="1b0bd-101">Remove-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="1b0bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b0bd-102">SYNOPSIS</span></span>
<span data-ttu-id="1b0bd-103">Data Box Edge 디바이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1b0bd-103">Removes a Data Box Edge device.</span></span>

## <span data-ttu-id="1b0bd-104">구문</span><span class="sxs-lookup"><span data-stu-id="1b0bd-104">SYNTAX</span></span>

### <span data-ttu-id="1b0bd-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1b0bd-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b0bd-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b0bd-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b0bd-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b0bd-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -InputObject <PSDataBoxEdgeDevice> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b0bd-108">설명</span><span class="sxs-lookup"><span data-stu-id="1b0bd-108">DESCRIPTION</span></span>
<span data-ttu-id="1b0bd-109">**Remove-AzDataBoxEdgeDevice** cmdlet은 Data Box Edge 디바이스에 대한 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1b0bd-109">The **Remove-AzDataBoxEdgeDevice** cmdlet removes the configuration for a Data Box Edge device.</span></span>
<span data-ttu-id="1b0bd-110">주문을 한 후에나 디바이스가 배송을 위해 Microsoft에서 준비하기 전에만 디바이스를 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b0bd-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="1b0bd-111">이 cmdlet을 사용하기 전에 리소스 삭제에 대한 [설명서를 참조하세요.](https://docs.microsoft.com/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span><span class="sxs-lookup"><span data-stu-id="1b0bd-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="1b0bd-112">예제</span><span class="sxs-lookup"><span data-stu-id="1b0bd-112">EXAMPLES</span></span>

### <span data-ttu-id="1b0bd-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="1b0bd-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="1b0bd-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1b0bd-114">PARAMETERS</span></span>

### <span data-ttu-id="1b0bd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b0bd-115">-AsJob</span></span>
<span data-ttu-id="1b0bd-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1b0bd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b0bd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b0bd-117">-DefaultProfile</span></span>
<span data-ttu-id="1b0bd-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1b0bd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b0bd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b0bd-119">-InputObject</span></span>
<span data-ttu-id="1b0bd-120">입력 개체</span><span class="sxs-lookup"><span data-stu-id="1b0bd-120">Input Object</span></span>

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

### <span data-ttu-id="1b0bd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1b0bd-121">-Name</span></span>
<span data-ttu-id="1b0bd-122">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="1b0bd-122">Resource Name</span></span>

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

### <span data-ttu-id="1b0bd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b0bd-123">-PassThru</span></span>
<span data-ttu-id="1b0bd-124">성공한 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1b0bd-124">returns true if successful</span></span>

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

### <span data-ttu-id="1b0bd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b0bd-125">-ResourceGroupName</span></span>
<span data-ttu-id="1b0bd-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="1b0bd-126">Resource Group Name</span></span>

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

### <span data-ttu-id="1b0bd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b0bd-127">-ResourceId</span></span>
<span data-ttu-id="1b0bd-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b0bd-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="1b0bd-129">-확인</span><span class="sxs-lookup"><span data-stu-id="1b0bd-129">-Confirm</span></span>
<span data-ttu-id="1b0bd-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b0bd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b0bd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b0bd-131">-WhatIf</span></span>
<span data-ttu-id="1b0bd-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1b0bd-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b0bd-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1b0bd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b0bd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b0bd-134">CommonParameters</span></span>
<span data-ttu-id="1b0bd-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1b0bd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b0bd-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b0bd-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b0bd-137">입력</span><span class="sxs-lookup"><span data-stu-id="1b0bd-137">INPUTS</span></span>

### <span data-ttu-id="1b0bd-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1b0bd-138">System.String</span></span>

### <span data-ttu-id="1b0bd-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="1b0bd-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="1b0bd-140">출력</span><span class="sxs-lookup"><span data-stu-id="1b0bd-140">OUTPUTS</span></span>

### <span data-ttu-id="1b0bd-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1b0bd-141">System.Boolean</span></span>

## <span data-ttu-id="1b0bd-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1b0bd-142">NOTES</span></span>

## <span data-ttu-id="1b0bd-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1b0bd-143">RELATED LINKS</span></span>
