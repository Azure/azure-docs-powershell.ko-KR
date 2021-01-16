---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubconfigurationmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
ms.openlocfilehash: 85793ba3097297de646db4695cac36173bb01673
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338673"
---
# <span data-ttu-id="444d5-101">Invoke-AzIotHubConfigurationMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="444d5-101">Invoke-AzIotHubConfigurationMetricsQuery</span></span>

## <span data-ttu-id="444d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="444d5-102">SYNOPSIS</span></span>
<span data-ttu-id="444d5-103">IoT 디바이스 구성 메트릭 쿼리를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="444d5-103">Invoke an IoT device configuration metric query.</span></span>

## <span data-ttu-id="444d5-104">구문</span><span class="sxs-lookup"><span data-stu-id="444d5-104">SYNTAX</span></span>

### <span data-ttu-id="444d5-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="444d5-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="444d5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="444d5-106">InputObjectSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="444d5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="444d5-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="444d5-108">설명</span><span class="sxs-lookup"><span data-stu-id="444d5-108">DESCRIPTION</span></span>
<span data-ttu-id="444d5-109">IoT 디바이스 구성에 정의된 대상 사용자 지정 또는 시스템 메트릭을 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="444d5-109">Evaluate a target custom or system metric defined in an IoT device configuration.</span></span>
<span data-ttu-id="444d5-110">미리 정의된 시스템 메트릭은 Iot Hub에서 계산되고 사용자 지정될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="444d5-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="444d5-111">"Targeted"는 대상 조건과 일치하는 디바이스 쌍의 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="444d5-111">"Targeted" specifies the number of device twins that match the target condition.</span></span>
- <span data-ttu-id="444d5-112">"적용"은 구성에 의해 수정된 디바이스 쌍의 수를 지정했습니다.</span><span class="sxs-lookup"><span data-stu-id="444d5-112">"Applied" specified the number of device twins that have been modified by the configuration.</span></span> 

## <span data-ttu-id="444d5-113">예제</span><span class="sxs-lookup"><span data-stu-id="444d5-113">EXAMPLES</span></span>

### <span data-ttu-id="444d5-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="444d5-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigurationMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "warningLimit"
```

<span data-ttu-id="444d5-115">사용자 지정 정의된 'warningLimit' 메트릭을 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="444d5-115">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="444d5-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="444d5-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "applied" -MetricType "system"
```

<span data-ttu-id="444d5-117">시스템 '적용된' 메트릭을 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="444d5-117">Evaluate the system 'applied' metric.</span></span>

## <span data-ttu-id="444d5-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="444d5-118">PARAMETERS</span></span>

### <span data-ttu-id="444d5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="444d5-119">-DefaultProfile</span></span>
<span data-ttu-id="444d5-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="444d5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="444d5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="444d5-121">-InputObject</span></span>
<span data-ttu-id="444d5-122">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="444d5-122">IotHub object</span></span>

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

### <span data-ttu-id="444d5-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="444d5-123">-IotHubName</span></span>
<span data-ttu-id="444d5-124">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="444d5-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="444d5-125">-MetricName</span><span class="sxs-lookup"><span data-stu-id="444d5-125">-MetricName</span></span>
<span data-ttu-id="444d5-126">평가를 위한 대상 메트릭입니다.</span><span class="sxs-lookup"><span data-stu-id="444d5-126">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="444d5-127">-MetricType</span><span class="sxs-lookup"><span data-stu-id="444d5-127">-MetricType</span></span>
<span data-ttu-id="444d5-128">메트릭을 찾아보는 데 사용할 메트릭 컬렉션을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="444d5-128">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="444d5-129">-Name</span><span class="sxs-lookup"><span data-stu-id="444d5-129">-Name</span></span>
<span data-ttu-id="444d5-130">구성에 대한 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="444d5-130">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="444d5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="444d5-131">-ResourceGroupName</span></span>
<span data-ttu-id="444d5-132">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="444d5-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="444d5-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="444d5-133">-ResourceId</span></span>
<span data-ttu-id="444d5-134">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="444d5-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="444d5-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="444d5-135">-Confirm</span></span>
<span data-ttu-id="444d5-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="444d5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="444d5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="444d5-137">-WhatIf</span></span>
<span data-ttu-id="444d5-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="444d5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="444d5-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="444d5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="444d5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="444d5-140">CommonParameters</span></span>
<span data-ttu-id="444d5-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="444d5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="444d5-142">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="444d5-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="444d5-143">입력</span><span class="sxs-lookup"><span data-stu-id="444d5-143">INPUTS</span></span>

### <span data-ttu-id="444d5-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="444d5-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="444d5-145">System.String</span><span class="sxs-lookup"><span data-stu-id="444d5-145">System.String</span></span>

## <span data-ttu-id="444d5-146">출력</span><span class="sxs-lookup"><span data-stu-id="444d5-146">OUTPUTS</span></span>

### <span data-ttu-id="444d5-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="444d5-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="444d5-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="444d5-148">NOTES</span></span>

## <span data-ttu-id="444d5-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="444d5-149">RELATED LINKS</span></span>
