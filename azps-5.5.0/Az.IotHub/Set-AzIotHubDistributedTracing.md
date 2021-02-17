---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
ms.openlocfilehash: 364b54f9e0b7a9112c2ce46f33363a4510c7bb68
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180508"
---
# <span data-ttu-id="35d8d-101">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="35d8d-101">Set-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="35d8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35d8d-102">SYNOPSIS</span></span>
<span data-ttu-id="35d8d-103">디바이스에 대한 분산 추적 옵션을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8d-103">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="35d8d-104">구문</span><span class="sxs-lookup"><span data-stu-id="35d8d-104">SYNTAX</span></span>

### <span data-ttu-id="35d8d-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="35d8d-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35d8d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="35d8d-106">InputObjectSet</span></span>
```
Set-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35d8d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="35d8d-107">ResourceIdSet</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35d8d-108">설명</span><span class="sxs-lookup"><span data-stu-id="35d8d-108">DESCRIPTION</span></span>
<span data-ttu-id="35d8d-109">디바이스에 대한 분산 추적 옵션을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8d-109">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="35d8d-110">예제</span><span class="sxs-lookup"><span data-stu-id="35d8d-110">EXAMPLES</span></span>

### <span data-ttu-id="35d8d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="35d8d-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -SamplingMode Enabled -SamplingRate 22

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="35d8d-112">디바이스에 대한 분산 추적 옵션을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8d-112">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="35d8d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35d8d-113">PARAMETERS</span></span>

### <span data-ttu-id="35d8d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35d8d-114">-DefaultProfile</span></span>
<span data-ttu-id="35d8d-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="35d8d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35d8d-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="35d8d-116">-DeviceId</span></span>
<span data-ttu-id="35d8d-117">대상 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="35d8d-117">Target Device Id.</span></span>

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

### <span data-ttu-id="35d8d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35d8d-118">-InputObject</span></span>
<span data-ttu-id="35d8d-119">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="35d8d-119">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35d8d-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="35d8d-120">-IotHubName</span></span>
<span data-ttu-id="35d8d-121">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="35d8d-121">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35d8d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35d8d-122">-ResourceGroupName</span></span>
<span data-ttu-id="35d8d-123">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="35d8d-123">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35d8d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35d8d-124">-ResourceId</span></span>
<span data-ttu-id="35d8d-125">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="35d8d-125">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35d8d-126">-SamplingMode</span><span class="sxs-lookup"><span data-stu-id="35d8d-126">-SamplingMode</span></span>
<span data-ttu-id="35d8d-127">분산 추적 사용 및 비활성화에 대한 샘플링을 턴합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8d-127">Turns sampling for distributed tracing enable and disable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDistributedTracingSamplingMode
Parameter Sets: (All)
Aliases: Mode
Accepted values: Disabled, Enabled

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35d8d-128">-SamplingRate</span><span class="sxs-lookup"><span data-stu-id="35d8d-128">-SamplingRate</span></span>
<span data-ttu-id="35d8d-129">추적 컨텍스트를 추가하기 위해 샘플링된 메시지의 양을 제어합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8d-129">Controls the amount of messages sampled for adding trace context.</span></span>
<span data-ttu-id="35d8d-130">이 값은 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="35d8d-130">This value is a percentage.</span></span>
<span data-ttu-id="35d8d-131">0~100(포함)의 값만 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="35d8d-131">Only values from 0 to 100 (inclusive) are permitted.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Rate

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35d8d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35d8d-132">-Confirm</span></span>
<span data-ttu-id="35d8d-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="35d8d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35d8d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35d8d-134">-WhatIf</span></span>
<span data-ttu-id="35d8d-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="35d8d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35d8d-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35d8d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35d8d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35d8d-137">CommonParameters</span></span>
<span data-ttu-id="35d8d-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35d8d-139">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="35d8d-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35d8d-140">입력</span><span class="sxs-lookup"><span data-stu-id="35d8d-140">INPUTS</span></span>

### <span data-ttu-id="35d8d-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="35d8d-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="35d8d-142">System.String</span><span class="sxs-lookup"><span data-stu-id="35d8d-142">System.String</span></span>

## <span data-ttu-id="35d8d-143">출력</span><span class="sxs-lookup"><span data-stu-id="35d8d-143">OUTPUTS</span></span>

### <span data-ttu-id="35d8d-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="35d8d-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="35d8d-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="35d8d-145">NOTES</span></span>

## <span data-ttu-id="35d8d-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35d8d-146">RELATED LINKS</span></span>
