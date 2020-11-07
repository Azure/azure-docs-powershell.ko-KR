---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
ms.openlocfilehash: 54ba89e380bf5f35d4a95b0bf026b872aa78b14c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868094"
---
# <span data-ttu-id="6cc9a-101">New-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="6cc9a-101">New-AzIotHub</span></span>

## <span data-ttu-id="6cc9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cc9a-102">SYNOPSIS</span></span>
<span data-ttu-id="6cc9a-103">새 IotHub를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6cc9a-103">Creates a new IotHub.</span></span>

## <span data-ttu-id="6cc9a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6cc9a-104">SYNTAX</span></span>

```
New-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cc9a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6cc9a-105">DESCRIPTION</span></span>
<span data-ttu-id="6cc9a-106">새 IotHub를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6cc9a-106">Creates a new IotHub.</span></span>
<span data-ttu-id="6cc9a-107">기본 속성 중 하나를 사용 하 여 IotHub를 만들거나 입력 proerties를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6cc9a-107">You can create the IotHub with either the default properties or specify the input proerties.</span></span>

## <span data-ttu-id="6cc9a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="6cc9a-108">EXAMPLES</span></span>

### <span data-ttu-id="6cc9a-109">예제 1 기본 속성으로 새 IotHub 만들기</span><span class="sxs-lookup"><span data-stu-id="6cc9a-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope"
```

<span data-ttu-id="6cc9a-110">Sku "S1", 용량 1 및 위치 "northeurope"에 대 한 "myiothub" 이라는 새 IotHub를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6cc9a-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope".</span></span>

### <span data-ttu-id="6cc9a-111">예제 2 CloudtoDevice 대기열의 MaxDeliveryCount를 20으로 설정 하 여 새 IotHub 만들기</span><span class="sxs-lookup"><span data-stu-id="6cc9a-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudtoDevice Queue set to 20</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="6cc9a-112">$Properties으로 표시 되는 고급 입력 속성이 있는 sku "S1", 용량 1 및 위치 "northeurope"의 "myiothub" 라는 새 IotHub를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6cc9a-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>
<span data-ttu-id="6cc9a-113">$psCloudToDeviceProperties = Microsoft Azure를 New-Object 합니다. IotHub. PSCloudToDeviceProperties-Property @ {MaxDeliveryCount = 20} $properties = New-Object-IotHub. PSIotHubInputProperties-속성 @ {CloudToDevice = $psCloudToDeviceProperties} New-AzIotHub-ResourceGroupName "myresourcegroup"-Name "myiothub"-"m"-단위 1-"northeurope"-속성 $properties</span><span class="sxs-lookup"><span data-stu-id="6cc9a-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="6cc9a-114">변수</span><span class="sxs-lookup"><span data-stu-id="6cc9a-114">PARAMETERS</span></span>

### <span data-ttu-id="6cc9a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cc9a-115">-DefaultProfile</span></span>
<span data-ttu-id="6cc9a-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6cc9a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6cc9a-117">-위치</span><span class="sxs-lookup"><span data-stu-id="6cc9a-117">-Location</span></span>
<span data-ttu-id="6cc9a-118">IoT hub를 만들어야 할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6cc9a-118">Location where the IoT hub needs to be created.</span></span> 

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

### <span data-ttu-id="6cc9a-119">-이름</span><span class="sxs-lookup"><span data-stu-id="6cc9a-119">-Name</span></span>
<span data-ttu-id="6cc9a-120">IotHub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6cc9a-120">Name of the IotHub</span></span>

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

### <span data-ttu-id="6cc9a-121">-속성</span><span class="sxs-lookup"><span data-stu-id="6cc9a-121">-Properties</span></span>
<span data-ttu-id="6cc9a-122">IoT hub의 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="6cc9a-122">Properties of the IoT hub.</span></span> 

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

### <span data-ttu-id="6cc9a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cc9a-123">-ResourceGroupName</span></span>
<span data-ttu-id="6cc9a-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6cc9a-124">Resource Group Name</span></span>

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

### <span data-ttu-id="6cc9a-125">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="6cc9a-125">-SkuName</span></span>
<span data-ttu-id="6cc9a-126">Sku 이름</span><span class="sxs-lookup"><span data-stu-id="6cc9a-126">Name of the sku</span></span>

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

### <span data-ttu-id="6cc9a-127">-단위</span><span class="sxs-lookup"><span data-stu-id="6cc9a-127">-Units</span></span>
<span data-ttu-id="6cc9a-128">단위 수</span><span class="sxs-lookup"><span data-stu-id="6cc9a-128">Number of units</span></span>

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

### <span data-ttu-id="6cc9a-129">-확인</span><span class="sxs-lookup"><span data-stu-id="6cc9a-129">-Confirm</span></span>
<span data-ttu-id="6cc9a-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cc9a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cc9a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cc9a-131">-WhatIf</span></span>
<span data-ttu-id="6cc9a-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6cc9a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cc9a-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6cc9a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cc9a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cc9a-134">CommonParameters</span></span>
<span data-ttu-id="6cc9a-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cc9a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cc9a-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cc9a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cc9a-137">입력</span><span class="sxs-lookup"><span data-stu-id="6cc9a-137">INPUTS</span></span>

### <span data-ttu-id="6cc9a-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6cc9a-138">System.String</span></span>

## <span data-ttu-id="6cc9a-139">출력</span><span class="sxs-lookup"><span data-stu-id="6cc9a-139">OUTPUTS</span></span>

### <span data-ttu-id="6cc9a-140">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="6cc9a-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="6cc9a-141">상속자</span><span class="sxs-lookup"><span data-stu-id="6cc9a-141">NOTES</span></span>

## <span data-ttu-id="6cc9a-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6cc9a-142">RELATED LINKS</span></span>
