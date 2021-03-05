---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
ms.openlocfilehash: b7deb19377d893d28d5b5924acf8c49daf706907
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978683"
---
# <span data-ttu-id="0964f-101">New-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="0964f-101">New-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="0964f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0964f-102">SYNOPSIS</span></span>
<span data-ttu-id="0964f-103">새 Data Box Edge 디바이스 구성</span><span class="sxs-lookup"><span data-stu-id="0964f-103">Configures a new Data Box Edge device</span></span>

## <span data-ttu-id="0964f-104">구문</span><span class="sxs-lookup"><span data-stu-id="0964f-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0964f-105">설명</span><span class="sxs-lookup"><span data-stu-id="0964f-105">DESCRIPTION</span></span>
<span data-ttu-id="0964f-106">**New-AzDataBoxEdgeDevice** cmdlet은 새 Data Box Edge 디바이스를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="0964f-106">The **New-AzDataBoxEdgeDevice** cmdlet configures a new Data Box Edge device</span></span>

## <span data-ttu-id="0964f-107">예제</span><span class="sxs-lookup"><span data-stu-id="0964f-107">EXAMPLES</span></span>

### <span data-ttu-id="0964f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0964f-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="0964f-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0964f-109">PARAMETERS</span></span>

### <span data-ttu-id="0964f-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0964f-110">-AsJob</span></span>
<span data-ttu-id="0964f-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0964f-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0964f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0964f-112">-DefaultProfile</span></span>
<span data-ttu-id="0964f-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0964f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0964f-114">-Location</span><span class="sxs-lookup"><span data-stu-id="0964f-114">-Location</span></span>
<span data-ttu-id="0964f-115">디바이스의 위치</span><span class="sxs-lookup"><span data-stu-id="0964f-115">Location of the device</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0964f-116">-Name</span><span class="sxs-lookup"><span data-stu-id="0964f-116">-Name</span></span>
<span data-ttu-id="0964f-117">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="0964f-117">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0964f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0964f-118">-ResourceGroupName</span></span>
<span data-ttu-id="0964f-119">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0964f-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0964f-120">-Sku</span><span class="sxs-lookup"><span data-stu-id="0964f-120">-Sku</span></span>
<span data-ttu-id="0964f-121">사용 가능한 Skus는 Edge, Gateway입니다.</span><span class="sxs-lookup"><span data-stu-id="0964f-121">Available Skus are Edge, Gateway</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0964f-122">-확인</span><span class="sxs-lookup"><span data-stu-id="0964f-122">-Confirm</span></span>
<span data-ttu-id="0964f-123">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0964f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0964f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0964f-124">-WhatIf</span></span>
<span data-ttu-id="0964f-125">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0964f-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0964f-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0964f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0964f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0964f-127">CommonParameters</span></span>
<span data-ttu-id="0964f-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0964f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0964f-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0964f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0964f-130">입력</span><span class="sxs-lookup"><span data-stu-id="0964f-130">INPUTS</span></span>

### <span data-ttu-id="0964f-131">없음</span><span class="sxs-lookup"><span data-stu-id="0964f-131">None</span></span>

## <span data-ttu-id="0964f-132">출력</span><span class="sxs-lookup"><span data-stu-id="0964f-132">OUTPUTS</span></span>

### <span data-ttu-id="0964f-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="0964f-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="0964f-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0964f-134">NOTES</span></span>

## <span data-ttu-id="0964f-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0964f-135">RELATED LINKS</span></span>
