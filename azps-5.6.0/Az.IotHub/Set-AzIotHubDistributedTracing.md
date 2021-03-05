---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
ms.openlocfilehash: b1bdc6b5910f47fdca8e8b66ab99939945547a08
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004139"
---
# <span data-ttu-id="99ba7-101">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="99ba7-101">Set-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="99ba7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99ba7-102">SYNOPSIS</span></span>
<span data-ttu-id="99ba7-103">디바이스에 대한 분산 추적 옵션을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="99ba7-103">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="99ba7-104">구문</span><span class="sxs-lookup"><span data-stu-id="99ba7-104">SYNTAX</span></span>

### <span data-ttu-id="99ba7-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="99ba7-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99ba7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="99ba7-106">InputObjectSet</span></span>
```
Set-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99ba7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="99ba7-107">ResourceIdSet</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99ba7-108">설명</span><span class="sxs-lookup"><span data-stu-id="99ba7-108">DESCRIPTION</span></span>
<span data-ttu-id="99ba7-109">디바이스에 대한 분산 추적 옵션을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="99ba7-109">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="99ba7-110">예제</span><span class="sxs-lookup"><span data-stu-id="99ba7-110">EXAMPLES</span></span>

### <span data-ttu-id="99ba7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="99ba7-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -SamplingMode Enabled -SamplingRate 22

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="99ba7-112">디바이스에 대한 분산 추적 옵션을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="99ba7-112">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="99ba7-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="99ba7-113">PARAMETERS</span></span>

### <span data-ttu-id="99ba7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99ba7-114">-DefaultProfile</span></span>
<span data-ttu-id="99ba7-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="99ba7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99ba7-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="99ba7-116">-DeviceId</span></span>
<span data-ttu-id="99ba7-117">대상 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="99ba7-117">Target Device Id.</span></span>

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

### <span data-ttu-id="99ba7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99ba7-118">-InputObject</span></span>
<span data-ttu-id="99ba7-119">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="99ba7-119">IotHub object</span></span>

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

### <span data-ttu-id="99ba7-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="99ba7-120">-IotHubName</span></span>
<span data-ttu-id="99ba7-121">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="99ba7-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="99ba7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99ba7-122">-ResourceGroupName</span></span>
<span data-ttu-id="99ba7-123">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="99ba7-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="99ba7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99ba7-124">-ResourceId</span></span>
<span data-ttu-id="99ba7-125">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="99ba7-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="99ba7-126">-SamplingMode</span><span class="sxs-lookup"><span data-stu-id="99ba7-126">-SamplingMode</span></span>
<span data-ttu-id="99ba7-127">분산 추적에 대한 샘플링을 사용하도록 설정하고 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="99ba7-127">Turns sampling for distributed tracing enable and disable.</span></span>

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

### <span data-ttu-id="99ba7-128">-샘플링레이트</span><span class="sxs-lookup"><span data-stu-id="99ba7-128">-SamplingRate</span></span>
<span data-ttu-id="99ba7-129">추적 컨텍스트를 추가하기 위해 샘플링된 메시지의 양을 제어합니다.</span><span class="sxs-lookup"><span data-stu-id="99ba7-129">Controls the amount of messages sampled for adding trace context.</span></span>
<span data-ttu-id="99ba7-130">이 값은 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="99ba7-130">This value is a percentage.</span></span>
<span data-ttu-id="99ba7-131">0에서 100(포함)의 값만 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="99ba7-131">Only values from 0 to 100 (inclusive) are permitted.</span></span>

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

### <span data-ttu-id="99ba7-132">-확인</span><span class="sxs-lookup"><span data-stu-id="99ba7-132">-Confirm</span></span>
<span data-ttu-id="99ba7-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="99ba7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99ba7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99ba7-134">-WhatIf</span></span>
<span data-ttu-id="99ba7-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="99ba7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99ba7-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99ba7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99ba7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99ba7-137">CommonParameters</span></span>
<span data-ttu-id="99ba7-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="99ba7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99ba7-139">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="99ba7-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99ba7-140">입력</span><span class="sxs-lookup"><span data-stu-id="99ba7-140">INPUTS</span></span>

### <span data-ttu-id="99ba7-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="99ba7-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="99ba7-142">System.String</span><span class="sxs-lookup"><span data-stu-id="99ba7-142">System.String</span></span>

## <span data-ttu-id="99ba7-143">출력</span><span class="sxs-lookup"><span data-stu-id="99ba7-143">OUTPUTS</span></span>

### <span data-ttu-id="99ba7-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="99ba7-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="99ba7-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="99ba7-145">NOTES</span></span>

## <span data-ttu-id="99ba7-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99ba7-146">RELATED LINKS</span></span>
