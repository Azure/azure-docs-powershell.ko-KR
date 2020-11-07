---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHub.md
ms.openlocfilehash: ad491605fcba26f713fcf295c419990e9db6ff2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711274"
---
# <span data-ttu-id="654ea-101">New-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="654ea-101">New-AzureRmIotHub</span></span>

## <span data-ttu-id="654ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="654ea-102">SYNOPSIS</span></span>
<span data-ttu-id="654ea-103">새 IotHub를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="654ea-103">Creates a new IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="654ea-104">구문과</span><span class="sxs-lookup"><span data-stu-id="654ea-104">SYNTAX</span></span>

```
New-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <PSIotHubSku> [-Units] <Int64>
 [-Location] <String> [-Properties <PSIotHubInputProperties>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="654ea-105">설명은</span><span class="sxs-lookup"><span data-stu-id="654ea-105">DESCRIPTION</span></span>
<span data-ttu-id="654ea-106">새 IotHub를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="654ea-106">Creates a new IotHub.</span></span>
<span data-ttu-id="654ea-107">기본 속성 중 하나를 사용 하 여 IotHub를 만들거나 입력 proerties를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="654ea-107">You can create the IotHub with either the default properties or specify the input proerties.</span></span>

## <span data-ttu-id="654ea-108">예제의</span><span class="sxs-lookup"><span data-stu-id="654ea-108">EXAMPLES</span></span>

### <span data-ttu-id="654ea-109">예제 1 기본 속성으로 새 IotHub 만들기</span><span class="sxs-lookup"><span data-stu-id="654ea-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope"
```

<span data-ttu-id="654ea-110">Sku "S1", 용량 1 및 위치 "northeurope"에 대 한 "myiothub" 이라는 새 IotHub를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="654ea-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope".</span></span>

### <span data-ttu-id="654ea-111">예제 2 CloudtoDevice 대기열의 MaxDeliveryCount를 20으로 설정 하 여 새 IotHub 만들기</span><span class="sxs-lookup"><span data-stu-id="654ea-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudtoDevice Queue set to 20</span></span>
```
PS C:\> New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="654ea-112">$Properties으로 표시 되는 고급 입력 속성이 있는 sku "S1", 용량 1 및 위치 "northeurope"의 "myiothub" 라는 새 IotHub를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="654ea-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>

<span data-ttu-id="654ea-113">$psCloudToDeviceProperties = Microsoft Azure를 New-Object 합니다. IotHub. PSCloudToDeviceProperties-Property @ {MaxDeliveryCount = 20} $properties = New-Object-IotHub. PSIotHubInputProperties-속성 @ {CloudToDevice = $psCloudToDeviceProperties} New-AzureRmIotHub-ResourceGroupName "myresourcegroup"-Name "myiothub"-"m"-단위 1-"northeurope"-속성 $properties</span><span class="sxs-lookup"><span data-stu-id="654ea-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="654ea-114">변수</span><span class="sxs-lookup"><span data-stu-id="654ea-114">PARAMETERS</span></span>

### <span data-ttu-id="654ea-115">-위치</span><span class="sxs-lookup"><span data-stu-id="654ea-115">-Location</span></span>
<span data-ttu-id="654ea-116">IoT hub를 만들어야 할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="654ea-116">Location where the IoT hub needs to be created.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="654ea-117">-이름</span><span class="sxs-lookup"><span data-stu-id="654ea-117">-Name</span></span>
<span data-ttu-id="654ea-118">IotHub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="654ea-118">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="654ea-119">-속성</span><span class="sxs-lookup"><span data-stu-id="654ea-119">-Properties</span></span>
<span data-ttu-id="654ea-120">IoT hub의 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="654ea-120">Properties of the IoT hub.</span></span> 

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

### <span data-ttu-id="654ea-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="654ea-121">-ResourceGroupName</span></span>
<span data-ttu-id="654ea-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="654ea-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="654ea-123">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="654ea-123">-SkuName</span></span>
<span data-ttu-id="654ea-124">Sku 이름</span><span class="sxs-lookup"><span data-stu-id="654ea-124">Name of the sku</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: (All)
Aliases: 
Accepted values: F1, S1, S2, S3

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="654ea-125">-단위</span><span class="sxs-lookup"><span data-stu-id="654ea-125">-Units</span></span>
<span data-ttu-id="654ea-126">단위 수</span><span class="sxs-lookup"><span data-stu-id="654ea-126">Number of units</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="654ea-127">-확인</span><span class="sxs-lookup"><span data-stu-id="654ea-127">-Confirm</span></span>
<span data-ttu-id="654ea-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="654ea-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="654ea-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="654ea-129">-WhatIf</span></span>
<span data-ttu-id="654ea-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="654ea-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="654ea-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="654ea-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="654ea-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="654ea-132">-DefaultProfile</span></span>
<span data-ttu-id="654ea-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="654ea-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="654ea-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="654ea-134">CommonParameters</span></span>
<span data-ttu-id="654ea-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="654ea-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="654ea-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="654ea-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="654ea-137">입력</span><span class="sxs-lookup"><span data-stu-id="654ea-137">INPUTS</span></span>

### <span data-ttu-id="654ea-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="654ea-138">System.String</span></span>
<span data-ttu-id="654ea-139">IotHub. PSIotHubSku. PSIotHubInputProperties. IotHub. \* \*. \* \*. \*. \*.</span><span class="sxs-lookup"><span data-stu-id="654ea-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku System.Int64 Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties</span></span>

## <span data-ttu-id="654ea-140">출력</span><span class="sxs-lookup"><span data-stu-id="654ea-140">OUTPUTS</span></span>

### <span data-ttu-id="654ea-141">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="654ea-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="654ea-142">상속자</span><span class="sxs-lookup"><span data-stu-id="654ea-142">NOTES</span></span>

## <span data-ttu-id="654ea-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="654ea-143">RELATED LINKS</span></span>

