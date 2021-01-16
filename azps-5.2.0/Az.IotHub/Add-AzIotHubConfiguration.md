---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
ms.openlocfilehash: d84d5b172d1a22880b508f8b43f071d5d454cf38
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348866"
---
# <span data-ttu-id="5bbdc-101">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="5bbdc-101">Add-AzIotHubConfiguration</span></span>

## <span data-ttu-id="5bbdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bbdc-102">SYNOPSIS</span></span>
<span data-ttu-id="5bbdc-103">대상 IoT Hub에 IoT 자동 디바이스 관리 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5bbdc-103">Add an IoT automatic device management configuration in a target IoT Hub.</span></span>

## <span data-ttu-id="5bbdc-104">구문</span><span class="sxs-lookup"><span data-stu-id="5bbdc-104">SYNTAX</span></span>

### <span data-ttu-id="5bbdc-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5bbdc-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-DeviceContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bbdc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5bbdc-106">InputObjectSet</span></span>
```
Add-AzIotHubConfiguration [-InputObject] <PSIotHub> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bbdc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5bbdc-107">ResourceIdSet</span></span>
```
Add-AzIotHubConfiguration [-ResourceId] <String> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bbdc-108">설명</span><span class="sxs-lookup"><span data-stu-id="5bbdc-108">DESCRIPTION</span></span>
<span data-ttu-id="5bbdc-109">구성 콘텐츠는 json으로, 디바이스 또는 모듈 의도에 따라 약간의 차이가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bbdc-109">Configuration content is json and slighty varies based on device or module intent.</span></span> <span data-ttu-id="5bbdc-110">디바이스 구성은 {"deviceContent":{...}} 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5bbdc-110">Device configurations are in the form of {"deviceContent":{...}}</span></span>
<span data-ttu-id="5bbdc-111">모듈 구성은 {"moduleContent":{...}} 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5bbdc-111">Module configurations are in the form of {"moduleContent":{...}}</span></span>
<span data-ttu-id="5bbdc-112">사용자 제공 메트릭을 사용하여 구성을 정의하여 필요 시 평가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bbdc-112">Configurations can be defined with user provided metrics for on demand evaluation.</span></span>
<span data-ttu-id="5bbdc-113">사용자 메트릭은 json 및 {"queries":{...}} 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5bbdc-113">User metrics are json and in the form of {"queries":{...}}</span></span> <span data-ttu-id="5bbdc-114">또는 {"metrics":{"queries":{...}}}.</span><span class="sxs-lookup"><span data-stu-id="5bbdc-114">or {"metrics":{"queries":{...}}}.</span></span>

<span data-ttu-id="5bbdc-115">참고: 모듈의 대상 조건은 "from devices.modules where"로 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bbdc-115">Note: Target condition for modules must start with "from devices.modules where".</span></span> <span data-ttu-id="5bbdc-116">자세한 https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5bbdc-116">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="5bbdc-117">예제</span><span class="sxs-lookup"><span data-stu-id="5bbdc-117">EXAMPLES</span></span>

### <span data-ttu-id="5bbdc-118">예제 1</span><span class="sxs-lookup"><span data-stu-id="5bbdc-118">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="5bbdc-119">기본 메타데이터를 사용하여 디바이스 구성을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="5bbdc-119">Create a device configuration with default metadata.</span></span>

### <span data-ttu-id="5bbdc-120">예제 2</span><span class="sxs-lookup"><span data-stu-id="5bbdc-120">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="5bbdc-121">디바이스가 건물 9에서 태그가 지정되어 환경이 '테스트'인 경우 조건에 적용되는 우선 순위가 3인 디바이스 구성을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="5bbdc-121">Create a device configuration with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="5bbdc-122">예제 3</span><span class="sxs-lookup"><span data-stu-id="5bbdc-122">Example 3</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Metric $metrics
```

<span data-ttu-id="5bbdc-123">사용자 메트릭을 사용하여 디바이스 구성을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bbdc-123">Create a device configuration with user metrics.</span></span>

### <span data-ttu-id="5bbdc-124">예제 4</span><span class="sxs-lookup"><span data-stu-id="5bbdc-124">Example 4</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels
```

<span data-ttu-id="5bbdc-125">레이블이 있는 디바이스 구성을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bbdc-125">Create a device configuration with labels.</span></span>

### <span data-ttu-id="5bbdc-126">예제 5</span><span class="sxs-lookup"><span data-stu-id="5bbdc-126">Example 5</span></span>
```powershell
PS C:\> $prop = @{}
PS C:\> $prop.add("Location", "US")
PS C:\> $content = @{}
PS C:\> $content.add("properties.desired.Region", $prop)
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -DeviceContent $content
```

<span data-ttu-id="5bbdc-127">콘텐츠가 있는 디바이스 구성을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bbdc-127">Create a device configuration with content.</span></span>

## <span data-ttu-id="5bbdc-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bbdc-128">PARAMETERS</span></span>

### <span data-ttu-id="5bbdc-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bbdc-129">-DefaultProfile</span></span>
<span data-ttu-id="5bbdc-130">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5bbdc-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bbdc-131">-DeviceContent</span><span class="sxs-lookup"><span data-stu-id="5bbdc-131">-DeviceContent</span></span>
<span data-ttu-id="5bbdc-132">IotHub 디바이스에 대한 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="5bbdc-132">Configuration for IotHub devices.</span></span>

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

### <span data-ttu-id="5bbdc-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5bbdc-133">-InputObject</span></span>
<span data-ttu-id="5bbdc-134">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="5bbdc-134">IotHub object</span></span>

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

### <span data-ttu-id="5bbdc-135">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="5bbdc-135">-IotHubName</span></span>
<span data-ttu-id="5bbdc-136">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="5bbdc-136">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5bbdc-137">-Label</span><span class="sxs-lookup"><span data-stu-id="5bbdc-137">-Label</span></span>
<span data-ttu-id="5bbdc-138">대상 구성에 적용할 레이블의 맵입니다.</span><span class="sxs-lookup"><span data-stu-id="5bbdc-138">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="5bbdc-139">-Metric</span><span class="sxs-lookup"><span data-stu-id="5bbdc-139">-Metric</span></span>
<span data-ttu-id="5bbdc-140">구성 메트릭 정의에 대한 쿼리 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="5bbdc-140">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="5bbdc-141">-Name</span><span class="sxs-lookup"><span data-stu-id="5bbdc-141">-Name</span></span>
<span data-ttu-id="5bbdc-142">구성에 대한 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5bbdc-142">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="5bbdc-143">-Priority</span><span class="sxs-lookup"><span data-stu-id="5bbdc-143">-Priority</span></span>
<span data-ttu-id="5bbdc-144">경쟁 규칙(최고 우승)의 경우 디바이스 구성의 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="5bbdc-144">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="5bbdc-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bbdc-145">-ResourceGroupName</span></span>
<span data-ttu-id="5bbdc-146">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="5bbdc-146">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5bbdc-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5bbdc-147">-ResourceId</span></span>
<span data-ttu-id="5bbdc-148">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="5bbdc-148">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5bbdc-149">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="5bbdc-149">-TargetCondition</span></span>
<span data-ttu-id="5bbdc-150">디바이스 구성이 적용되는 대상 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="5bbdc-150">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="5bbdc-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5bbdc-151">-Confirm</span></span>
<span data-ttu-id="5bbdc-152">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5bbdc-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bbdc-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bbdc-153">-WhatIf</span></span>
<span data-ttu-id="5bbdc-154">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5bbdc-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bbdc-155">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5bbdc-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bbdc-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bbdc-156">CommonParameters</span></span>
<span data-ttu-id="5bbdc-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5bbdc-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bbdc-158">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5bbdc-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bbdc-159">입력</span><span class="sxs-lookup"><span data-stu-id="5bbdc-159">INPUTS</span></span>

### <span data-ttu-id="5bbdc-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="5bbdc-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5bbdc-161">System.String</span><span class="sxs-lookup"><span data-stu-id="5bbdc-161">System.String</span></span>

## <span data-ttu-id="5bbdc-162">출력</span><span class="sxs-lookup"><span data-stu-id="5bbdc-162">OUTPUTS</span></span>

### <span data-ttu-id="5bbdc-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="5bbdc-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="5bbdc-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5bbdc-164">NOTES</span></span>

## <span data-ttu-id="5bbdc-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5bbdc-165">RELATED LINKS</span></span>
