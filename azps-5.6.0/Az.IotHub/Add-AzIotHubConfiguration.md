---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
ms.openlocfilehash: 2521d73d26b281e2dbc242e860869e4e31c78208
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997934"
---
# <span data-ttu-id="9f2c8-101">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f2c8-101">Add-AzIotHubConfiguration</span></span>

## <span data-ttu-id="9f2c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f2c8-102">SYNOPSIS</span></span>
<span data-ttu-id="9f2c8-103">대상 IoT Hub에 IoT 자동 디바이스 관리 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-103">Add an IoT automatic device management configuration in a target IoT Hub.</span></span>

## <span data-ttu-id="9f2c8-104">구문</span><span class="sxs-lookup"><span data-stu-id="9f2c8-104">SYNTAX</span></span>

### <span data-ttu-id="9f2c8-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9f2c8-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-DeviceContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f2c8-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9f2c8-106">InputObjectSet</span></span>
```
Add-AzIotHubConfiguration [-InputObject] <PSIotHub> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f2c8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9f2c8-107">ResourceIdSet</span></span>
```
Add-AzIotHubConfiguration [-ResourceId] <String> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f2c8-108">설명</span><span class="sxs-lookup"><span data-stu-id="9f2c8-108">DESCRIPTION</span></span>
<span data-ttu-id="9f2c8-109">구성 콘텐츠는 json으로, 디바이스 또는 모듈 의도에 따라 약간의 차이가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-109">Configuration content is json and slighty varies based on device or module intent.</span></span> <span data-ttu-id="9f2c8-110">디바이스 구성은 {"deviceContent":{...}} 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-110">Device configurations are in the form of {"deviceContent":{...}}</span></span>
<span data-ttu-id="9f2c8-111">모듈 구성은 {"moduleContent":{...}} 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-111">Module configurations are in the form of {"moduleContent":{...}}</span></span>
<span data-ttu-id="9f2c8-112">구성은 사용자 제공 메트릭을 사용하여 수요 평가를 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-112">Configurations can be defined with user provided metrics for on demand evaluation.</span></span>
<span data-ttu-id="9f2c8-113">사용자 메트릭은 json 및 {"queries":{...}} 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-113">User metrics are json and in the form of {"queries":{...}}</span></span> <span data-ttu-id="9f2c8-114">또는 {"metrics":{"queries":{...}}}}.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-114">or {"metrics":{"queries":{...}}}.</span></span>

<span data-ttu-id="9f2c8-115">참고: 모듈의 대상 조건은 "from devices.modules where"로 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-115">Note: Target condition for modules must start with "from devices.modules where".</span></span> <span data-ttu-id="9f2c8-116">자세한 https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management 내용은 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-116">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="9f2c8-117">예제</span><span class="sxs-lookup"><span data-stu-id="9f2c8-117">EXAMPLES</span></span>

### <span data-ttu-id="9f2c8-118">예제 1</span><span class="sxs-lookup"><span data-stu-id="9f2c8-118">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="9f2c8-119">기본 메타데이터를 사용하여 디바이스 구성을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-119">Create a device configuration with default metadata.</span></span>

### <span data-ttu-id="9f2c8-120">예제 2</span><span class="sxs-lookup"><span data-stu-id="9f2c8-120">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="9f2c8-121">디바이스가 건물 9에서 태그가 지정되어 환경이 '테스트'인 경우 조건에 적용되는 3의 우선 순위가 있는 디바이스 구성을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-121">Create a device configuration with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="9f2c8-122">예제 3</span><span class="sxs-lookup"><span data-stu-id="9f2c8-122">Example 3</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Metric $metrics
```

<span data-ttu-id="9f2c8-123">사용자 메트릭을 사용하여 디바이스 구성을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-123">Create a device configuration with user metrics.</span></span>

### <span data-ttu-id="9f2c8-124">예제 4</span><span class="sxs-lookup"><span data-stu-id="9f2c8-124">Example 4</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels
```

<span data-ttu-id="9f2c8-125">레이블을 사용하여 디바이스 구성을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-125">Create a device configuration with labels.</span></span>

### <span data-ttu-id="9f2c8-126">예제 5</span><span class="sxs-lookup"><span data-stu-id="9f2c8-126">Example 5</span></span>
```powershell
PS C:\> $prop = @{}
PS C:\> $prop.add("Location", "US")
PS C:\> $content = @{}
PS C:\> $content.add("properties.desired.Region", $prop)
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -DeviceContent $content
```

<span data-ttu-id="9f2c8-127">콘텐츠가 있는 디바이스 구성을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-127">Create a device configuration with content.</span></span>

## <span data-ttu-id="9f2c8-128">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9f2c8-128">PARAMETERS</span></span>

### <span data-ttu-id="9f2c8-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f2c8-129">-DefaultProfile</span></span>
<span data-ttu-id="9f2c8-130">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f2c8-131">-DeviceContent</span><span class="sxs-lookup"><span data-stu-id="9f2c8-131">-DeviceContent</span></span>
<span data-ttu-id="9f2c8-132">IotHub 디바이스에 대한 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-132">Configuration for IotHub devices.</span></span>

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

### <span data-ttu-id="9f2c8-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f2c8-133">-InputObject</span></span>
<span data-ttu-id="9f2c8-134">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="9f2c8-134">IotHub object</span></span>

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

### <span data-ttu-id="9f2c8-135">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="9f2c8-135">-IotHubName</span></span>
<span data-ttu-id="9f2c8-136">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="9f2c8-136">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9f2c8-137">-Label</span><span class="sxs-lookup"><span data-stu-id="9f2c8-137">-Label</span></span>
<span data-ttu-id="9f2c8-138">대상 구성에 적용할 레이블의 맵입니다.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-138">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="9f2c8-139">-Metric</span><span class="sxs-lookup"><span data-stu-id="9f2c8-139">-Metric</span></span>
<span data-ttu-id="9f2c8-140">구성 메트릭 정의에 대한 쿼리 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-140">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="9f2c8-141">-Name</span><span class="sxs-lookup"><span data-stu-id="9f2c8-141">-Name</span></span>
<span data-ttu-id="9f2c8-142">구성에 대한 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-142">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="9f2c8-143">-Priority</span><span class="sxs-lookup"><span data-stu-id="9f2c8-143">-Priority</span></span>
<span data-ttu-id="9f2c8-144">경쟁 규칙(가장 높은 승리)의 경우 디바이스 구성의 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-144">Weight of the device configuration in case of competing rules (highest wins).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f2c8-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f2c8-145">-ResourceGroupName</span></span>
<span data-ttu-id="9f2c8-146">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="9f2c8-146">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9f2c8-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f2c8-147">-ResourceId</span></span>
<span data-ttu-id="9f2c8-148">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="9f2c8-148">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9f2c8-149">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="9f2c8-149">-TargetCondition</span></span>
<span data-ttu-id="9f2c8-150">디바이스 구성이 적용되는 대상 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-150">Target condition in which a device configuration applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f2c8-151">-확인</span><span class="sxs-lookup"><span data-stu-id="9f2c8-151">-Confirm</span></span>
<span data-ttu-id="9f2c8-152">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f2c8-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f2c8-153">-WhatIf</span></span>
<span data-ttu-id="9f2c8-154">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f2c8-155">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f2c8-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f2c8-156">CommonParameters</span></span>
<span data-ttu-id="9f2c8-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f2c8-158">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f2c8-159">입력</span><span class="sxs-lookup"><span data-stu-id="9f2c8-159">INPUTS</span></span>

### <span data-ttu-id="9f2c8-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9f2c8-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9f2c8-161">System.String</span><span class="sxs-lookup"><span data-stu-id="9f2c8-161">System.String</span></span>

## <span data-ttu-id="9f2c8-162">출력</span><span class="sxs-lookup"><span data-stu-id="9f2c8-162">OUTPUTS</span></span>

### <span data-ttu-id="9f2c8-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f2c8-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="9f2c8-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9f2c8-164">NOTES</span></span>

## <span data-ttu-id="9f2c8-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9f2c8-165">RELATED LINKS</span></span>
