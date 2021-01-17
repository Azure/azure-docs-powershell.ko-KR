---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
ms.openlocfilehash: 40fa5d382972c53de94187c9731748be5b1bfe2a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386576"
---
# <span data-ttu-id="9d07b-101">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d07b-101">Set-AzIotHubConfiguration</span></span>

## <span data-ttu-id="9d07b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d07b-102">SYNOPSIS</span></span>
<span data-ttu-id="9d07b-103">구성 등록의 변경 가능한 필드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9d07b-103">Update the mutable fields of the configuration registration.</span></span>

## <span data-ttu-id="9d07b-104">구문</span><span class="sxs-lookup"><span data-stu-id="9d07b-104">SYNTAX</span></span>

### <span data-ttu-id="9d07b-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9d07b-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name] <String>
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d07b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9d07b-106">InputObjectSet</span></span>
```
Set-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d07b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9d07b-107">ResourceIdSet</span></span>
```
Set-AzIotHubConfiguration [-ResourceId] <String> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d07b-108">설명</span><span class="sxs-lookup"><span data-stu-id="9d07b-108">DESCRIPTION</span></span>
<span data-ttu-id="9d07b-109">IoT 자동 디바이스 관리 구성의 지정된 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9d07b-109">Update specified properties of an IoT automatic device management configuration.</span></span>
<span data-ttu-id="9d07b-110">참고: 구성 콘텐츠는 변경 불가능합니다.</span><span class="sxs-lookup"><span data-stu-id="9d07b-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="9d07b-111">업데이트할 수 있는 구성 속성은 'labels', 'metrics', 'priority' 및 'targetCondition'입니다.</span><span class="sxs-lookup"><span data-stu-id="9d07b-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="9d07b-112">자세한 https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9d07b-112">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="9d07b-113">예제</span><span class="sxs-lookup"><span data-stu-id="9d07b-113">EXAMPLES</span></span>

### <span data-ttu-id="9d07b-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="9d07b-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="9d07b-115">디바이스 구성의 우선 순위를 변경하고 대상 조건을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9d07b-115">Alter the priority of a device configuration and update its target condition</span></span>

### <span data-ttu-id="9d07b-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="9d07b-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels -Metric $metrics
```

<span data-ttu-id="9d07b-117">디바이스 구성의 메트릭 및 레이블 업데이트</span><span class="sxs-lookup"><span data-stu-id="9d07b-117">Update the metrics and labels of a device configuration</span></span>

## <span data-ttu-id="9d07b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d07b-118">PARAMETERS</span></span>

### <span data-ttu-id="9d07b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d07b-119">-DefaultProfile</span></span>
<span data-ttu-id="9d07b-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9d07b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d07b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9d07b-121">-Force</span></span>
<span data-ttu-id="9d07b-122">구성 개체를 마지막으로 검색한 후 업데이트된 경우에도 바꿀 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9d07b-122">Allows configuration object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="9d07b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d07b-123">-InputObject</span></span>
<span data-ttu-id="9d07b-124">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="9d07b-124">IotHub object</span></span>

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

### <span data-ttu-id="9d07b-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="9d07b-125">-IotHubName</span></span>
<span data-ttu-id="9d07b-126">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="9d07b-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9d07b-127">-Label</span><span class="sxs-lookup"><span data-stu-id="9d07b-127">-Label</span></span>
<span data-ttu-id="9d07b-128">대상 구성에 적용할 레이블의 맵입니다.</span><span class="sxs-lookup"><span data-stu-id="9d07b-128">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="9d07b-129">-Metric</span><span class="sxs-lookup"><span data-stu-id="9d07b-129">-Metric</span></span>
<span data-ttu-id="9d07b-130">구성 메트릭 정의에 대한 쿼리 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="9d07b-130">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="9d07b-131">-Name</span><span class="sxs-lookup"><span data-stu-id="9d07b-131">-Name</span></span>
<span data-ttu-id="9d07b-132">구성에 대한 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="9d07b-132">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="9d07b-133">-Priority</span><span class="sxs-lookup"><span data-stu-id="9d07b-133">-Priority</span></span>
<span data-ttu-id="9d07b-134">경쟁 규칙(최고 우승)의 경우 디바이스 구성의 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="9d07b-134">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="9d07b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d07b-135">-ResourceGroupName</span></span>
<span data-ttu-id="9d07b-136">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="9d07b-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9d07b-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d07b-137">-ResourceId</span></span>
<span data-ttu-id="9d07b-138">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="9d07b-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9d07b-139">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="9d07b-139">-TargetCondition</span></span>
<span data-ttu-id="9d07b-140">디바이스 구성이 적용되는 대상 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="9d07b-140">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="9d07b-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d07b-141">-Confirm</span></span>
<span data-ttu-id="9d07b-142">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9d07b-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d07b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d07b-143">-WhatIf</span></span>
<span data-ttu-id="9d07b-144">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9d07b-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d07b-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9d07b-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d07b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d07b-146">CommonParameters</span></span>
<span data-ttu-id="9d07b-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9d07b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d07b-148">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9d07b-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d07b-149">입력</span><span class="sxs-lookup"><span data-stu-id="9d07b-149">INPUTS</span></span>

### <span data-ttu-id="9d07b-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9d07b-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9d07b-151">System.String</span><span class="sxs-lookup"><span data-stu-id="9d07b-151">System.String</span></span>

## <span data-ttu-id="9d07b-152">출력</span><span class="sxs-lookup"><span data-stu-id="9d07b-152">OUTPUTS</span></span>

### <span data-ttu-id="9d07b-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d07b-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="9d07b-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9d07b-154">NOTES</span></span>

## <span data-ttu-id="9d07b-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9d07b-155">RELATED LINKS</span></span>
