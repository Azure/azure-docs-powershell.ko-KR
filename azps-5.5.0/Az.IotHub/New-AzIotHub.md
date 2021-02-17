---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
ms.openlocfilehash: 392f9362df1cafdb6c047020b3381a7b16320607
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180556"
---
# <span data-ttu-id="c0cb2-101">New-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="c0cb2-101">New-AzIotHub</span></span>

## <span data-ttu-id="c0cb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0cb2-102">SYNOPSIS</span></span>
<span data-ttu-id="c0cb2-103">새 IotHub를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c0cb2-103">Creates a new IotHub.</span></span>

## <span data-ttu-id="c0cb2-104">구문</span><span class="sxs-lookup"><span data-stu-id="c0cb2-104">SYNTAX</span></span>

```
New-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0cb2-105">설명</span><span class="sxs-lookup"><span data-stu-id="c0cb2-105">DESCRIPTION</span></span>
<span data-ttu-id="c0cb2-106">새 IotHub를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c0cb2-106">Creates a new IotHub.</span></span>
<span data-ttu-id="c0cb2-107">기본 속성으로 IotHub를 만들거나 입력 속성을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0cb2-107">You can create the IotHub with either the default properties or specify the input properties.</span></span>

## <span data-ttu-id="c0cb2-108">예제</span><span class="sxs-lookup"><span data-stu-id="c0cb2-108">EXAMPLES</span></span>

### <span data-ttu-id="c0cb2-109">예제 1 기본 속성으로 새 IotHub 만들기</span><span class="sxs-lookup"><span data-stu-id="c0cb2-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> $tags = @{}
PS C:\> $tags.Add('key1','value1')
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Tag $tags
```

<span data-ttu-id="c0cb2-110">태그에 포함된 SKU "S1", 용량 1 및 위치 "northeurope"의 "myiothub"라는 새 IotHub를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c0cb2-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" included with Tags.</span></span>

### <span data-ttu-id="c0cb2-111">예제 2 CloudToDevice 큐의 MaxDeliveryCount를 20으로 설정하여 새 IotHub 만들기</span><span class="sxs-lookup"><span data-stu-id="c0cb2-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudToDevice Queue set to 20</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="c0cb2-112">sku "S1", 용량 1 및 위치 "northeurope"의 "myiothub"라는 새 IotHub를 $properties.</span><span class="sxs-lookup"><span data-stu-id="c0cb2-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>
<span data-ttu-id="c0cb2-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span><span class="sxs-lookup"><span data-stu-id="c0cb2-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="c0cb2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0cb2-114">PARAMETERS</span></span>

### <span data-ttu-id="c0cb2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0cb2-115">-DefaultProfile</span></span>
<span data-ttu-id="c0cb2-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c0cb2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0cb2-117">-Location</span><span class="sxs-lookup"><span data-stu-id="c0cb2-117">-Location</span></span>
<span data-ttu-id="c0cb2-118">IoT Hub를 만들어야 하는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cb2-118">Location where the IoT hub needs to be created.</span></span> 

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

### <span data-ttu-id="c0cb2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c0cb2-119">-Name</span></span>
<span data-ttu-id="c0cb2-120">IotHub의 이름</span><span class="sxs-lookup"><span data-stu-id="c0cb2-120">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0cb2-121">-Properties</span><span class="sxs-lookup"><span data-stu-id="c0cb2-121">-Properties</span></span>
<span data-ttu-id="c0cb2-122">IoT Hub의 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cb2-122">Properties of the IoT hub.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0cb2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0cb2-123">-ResourceGroupName</span></span>
<span data-ttu-id="c0cb2-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c0cb2-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0cb2-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c0cb2-125">-SkuName</span></span>
<span data-ttu-id="c0cb2-126">SKU의 이름</span><span class="sxs-lookup"><span data-stu-id="c0cb2-126">Name of the sku</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: (All)
Aliases:
Accepted values: F1, S1, S2, S3, B1, B2, B3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0cb2-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="c0cb2-127">-Tag</span></span>
<span data-ttu-id="c0cb2-128">IoT Hub 인스턴스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cb2-128">IoT hub instance tags.</span></span> <span data-ttu-id="c0cb2-129">해시 테이블 형식의 키-값 쌍에 있는 속성 바입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cb2-129">Property bag in key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0cb2-130">-Units</span><span class="sxs-lookup"><span data-stu-id="c0cb2-130">-Units</span></span>
<span data-ttu-id="c0cb2-131">단위 수</span><span class="sxs-lookup"><span data-stu-id="c0cb2-131">Number of units</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0cb2-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0cb2-132">-Confirm</span></span>
<span data-ttu-id="c0cb2-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0cb2-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0cb2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0cb2-134">-WhatIf</span></span>
<span data-ttu-id="c0cb2-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c0cb2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0cb2-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c0cb2-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0cb2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0cb2-137">CommonParameters</span></span>
<span data-ttu-id="c0cb2-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c0cb2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0cb2-139">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c0cb2-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0cb2-140">입력</span><span class="sxs-lookup"><span data-stu-id="c0cb2-140">INPUTS</span></span>

### <span data-ttu-id="c0cb2-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c0cb2-141">System.String</span></span>

## <span data-ttu-id="c0cb2-142">출력</span><span class="sxs-lookup"><span data-stu-id="c0cb2-142">OUTPUTS</span></span>

### <span data-ttu-id="c0cb2-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c0cb2-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="c0cb2-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c0cb2-144">NOTES</span></span>

## <span data-ttu-id="c0cb2-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0cb2-145">RELATED LINKS</span></span>
