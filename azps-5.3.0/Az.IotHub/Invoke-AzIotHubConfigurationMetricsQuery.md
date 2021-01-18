---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubconfigurationmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
ms.openlocfilehash: 85793ba3097297de646db4695cac36173bb01673
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495362"
---
# <span data-ttu-id="0e8f0-101">Invoke-AzIotHubConfigurationMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="0e8f0-101">Invoke-AzIotHubConfigurationMetricsQuery</span></span>

## <span data-ttu-id="0e8f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e8f0-102">SYNOPSIS</span></span>
<span data-ttu-id="0e8f0-103">IoT 디바이스 구성 메트릭 쿼리를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8f0-103">Invoke an IoT device configuration metric query.</span></span>

## <span data-ttu-id="0e8f0-104">구문</span><span class="sxs-lookup"><span data-stu-id="0e8f0-104">SYNTAX</span></span>

### <span data-ttu-id="0e8f0-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0e8f0-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e8f0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0e8f0-106">InputObjectSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0e8f0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0e8f0-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0e8f0-108">설명</span><span class="sxs-lookup"><span data-stu-id="0e8f0-108">DESCRIPTION</span></span>
<span data-ttu-id="0e8f0-109">IoT 디바이스 구성에 정의된 대상 사용자 지정 또는 시스템 메트릭을 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8f0-109">Evaluate a target custom or system metric defined in an IoT device configuration.</span></span>
<span data-ttu-id="0e8f0-110">미리 정의된 시스템 메트릭은 Iot Hub에서 계산되고 사용자 지정될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0e8f0-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="0e8f0-111">"Targeted"는 대상 조건과 일치하는 디바이스 쌍의 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8f0-111">"Targeted" specifies the number of device twins that match the target condition.</span></span>
- <span data-ttu-id="0e8f0-112">"적용"은 구성에 의해 수정된 디바이스 쌍의 수를 지정했습니다.</span><span class="sxs-lookup"><span data-stu-id="0e8f0-112">"Applied" specified the number of device twins that have been modified by the configuration.</span></span> 

## <span data-ttu-id="0e8f0-113">예제</span><span class="sxs-lookup"><span data-stu-id="0e8f0-113">EXAMPLES</span></span>

### <span data-ttu-id="0e8f0-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="0e8f0-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigurationMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "warningLimit"
```

<span data-ttu-id="0e8f0-115">사용자 지정 정의된 'warningLimit' 메트릭을 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8f0-115">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="0e8f0-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="0e8f0-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "applied" -MetricType "system"
```

<span data-ttu-id="0e8f0-117">시스템 '적용된' 메트릭을 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8f0-117">Evaluate the system 'applied' metric.</span></span>

## <span data-ttu-id="0e8f0-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e8f0-118">PARAMETERS</span></span>

### <span data-ttu-id="0e8f0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e8f0-119">-DefaultProfile</span></span>
<span data-ttu-id="0e8f0-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0e8f0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e8f0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e8f0-121">-InputObject</span></span>
<span data-ttu-id="0e8f0-122">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="0e8f0-122">IotHub object</span></span>

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

### <span data-ttu-id="0e8f0-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="0e8f0-123">-IotHubName</span></span>
<span data-ttu-id="0e8f0-124">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="0e8f0-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="0e8f0-125">-MetricName</span><span class="sxs-lookup"><span data-stu-id="0e8f0-125">-MetricName</span></span>
<span data-ttu-id="0e8f0-126">평가를 위한 대상 메트릭입니다.</span><span class="sxs-lookup"><span data-stu-id="0e8f0-126">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="0e8f0-127">-MetricType</span><span class="sxs-lookup"><span data-stu-id="0e8f0-127">-MetricType</span></span>
<span data-ttu-id="0e8f0-128">메트릭을 찾아보는 데 사용할 메트릭 컬렉션을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0e8f0-128">Indicates which metric collection should be used to lookup a metric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricType
Parameter Sets: (All)
Aliases:
Accepted values: Custom, System

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e8f0-129">-Name</span><span class="sxs-lookup"><span data-stu-id="0e8f0-129">-Name</span></span>
<span data-ttu-id="0e8f0-130">구성에 대한 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="0e8f0-130">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="0e8f0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e8f0-131">-ResourceGroupName</span></span>
<span data-ttu-id="0e8f0-132">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="0e8f0-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0e8f0-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e8f0-133">-ResourceId</span></span>
<span data-ttu-id="0e8f0-134">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="0e8f0-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="0e8f0-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e8f0-135">-Confirm</span></span>
<span data-ttu-id="0e8f0-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e8f0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e8f0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e8f0-137">-WhatIf</span></span>
<span data-ttu-id="0e8f0-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0e8f0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e8f0-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e8f0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e8f0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e8f0-140">CommonParameters</span></span>
<span data-ttu-id="0e8f0-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8f0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e8f0-142">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0e8f0-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e8f0-143">입력</span><span class="sxs-lookup"><span data-stu-id="0e8f0-143">INPUTS</span></span>

### <span data-ttu-id="0e8f0-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="0e8f0-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="0e8f0-145">System.String</span><span class="sxs-lookup"><span data-stu-id="0e8f0-145">System.String</span></span>

## <span data-ttu-id="0e8f0-146">출력</span><span class="sxs-lookup"><span data-stu-id="0e8f0-146">OUTPUTS</span></span>

### <span data-ttu-id="0e8f0-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="0e8f0-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="0e8f0-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0e8f0-148">NOTES</span></span>

## <span data-ttu-id="0e8f0-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e8f0-149">RELATED LINKS</span></span>
