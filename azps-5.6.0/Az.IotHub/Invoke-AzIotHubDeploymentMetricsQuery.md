---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubdeploymentmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
ms.openlocfilehash: 02870d2bf0016704328e157b948b9db8ae1207f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962976"
---
# <span data-ttu-id="1f3e6-101">Invoke-AzIotHubDeploymentMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="1f3e6-101">Invoke-AzIotHubDeploymentMetricsQuery</span></span>

## <span data-ttu-id="1f3e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f3e6-102">SYNOPSIS</span></span>
<span data-ttu-id="1f3e6-103">IoT Edge 배포 메트릭 쿼리를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-103">Invoke an IoT Edge deployment metric query.</span></span>

## <span data-ttu-id="1f3e6-104">구문</span><span class="sxs-lookup"><span data-stu-id="1f3e6-104">SYNTAX</span></span>

### <span data-ttu-id="1f3e6-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1f3e6-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f3e6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1f3e6-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f3e6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1f3e6-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f3e6-108">설명</span><span class="sxs-lookup"><span data-stu-id="1f3e6-108">DESCRIPTION</span></span>
<span data-ttu-id="1f3e6-109">IoT Edge 배포에 정의된 대상 사용자 지정 또는 시스템 메트릭을 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-109">Evaluate a target custom or system metric defined in an IoT Edge deployment.</span></span>
<span data-ttu-id="1f3e6-110">Iot Hub에서 계산하고 사용자 지정할 수 없는 미리 정의된 시스템 메트릭이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="1f3e6-111">"대상 지정"은 배포 대상 조건과 일치하는 IoT Edge 디바이스를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-111">"Targeted" shows the IoT Edge devices that match the deployment targeting condition.</span></span>
- <span data-ttu-id="1f3e6-112">"적용"은 우선 순위가 높은 다른 배포의 대상이 아닌 대상 IoT Edge 디바이스를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-112">"Applied" shows the targeted IoT Edge devices that are not targeted by another deployment of higher priority.</span></span>
- <span data-ttu-id="1f3e6-113">"보고 성공"은 모듈이 성공적으로 배포된 것으로 보고된 IoT Edge 디바이스를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-113">"Reporting Success" shows the IoT Edge devices that have reported that the modules have been deployed successfully.</span></span>
- <span data-ttu-id="1f3e6-114">"보고 실패"는 하나 이상의 모듈이 성공적으로 배포되지 않았다고 보고한 IoT Edge 디바이스를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-114">"Reporting Failure" shows the IoT Edge devices that have reported that one or more modules haven't been deployed successfully.</span></span> 
  <span data-ttu-id="1f3e6-115">오류를 더 조사하려면 해당 디바이스에 원격으로 연결하고 로그 파일을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-115">To further investigate the error, connect remotely to those devices and view the log files.</span></span>

## <span data-ttu-id="1f3e6-116">예제</span><span class="sxs-lookup"><span data-stu-id="1f3e6-116">EXAMPLES</span></span>

### <span data-ttu-id="1f3e6-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="1f3e6-117">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeploymentMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "warningLimit"
```

<span data-ttu-id="1f3e6-118">사용자 지정 정의된 'warningLimit' 메트릭을 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-118">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="1f3e6-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="1f3e6-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeployMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "Reporting Success" -MetricType "system"
```

<span data-ttu-id="1f3e6-120">시스템 '보고 성공' 메트릭을 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-120">Evaluate the system 'Reporting Success' metric.</span></span>

## <span data-ttu-id="1f3e6-121">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1f3e6-121">PARAMETERS</span></span>

### <span data-ttu-id="1f3e6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f3e6-122">-DefaultProfile</span></span>
<span data-ttu-id="1f3e6-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f3e6-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f3e6-124">-InputObject</span></span>
<span data-ttu-id="1f3e6-125">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="1f3e6-125">IotHub object</span></span>

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

### <span data-ttu-id="1f3e6-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="1f3e6-126">-IotHubName</span></span>
<span data-ttu-id="1f3e6-127">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="1f3e6-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1f3e6-128">-MetricName</span><span class="sxs-lookup"><span data-stu-id="1f3e6-128">-MetricName</span></span>
<span data-ttu-id="1f3e6-129">평가를 위한 대상 메트릭입니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-129">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="1f3e6-130">-MetricType</span><span class="sxs-lookup"><span data-stu-id="1f3e6-130">-MetricType</span></span>
<span data-ttu-id="1f3e6-131">메트릭을 찾아보는 데 사용할 메트릭 컬렉션을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-131">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="1f3e6-132">-Name</span><span class="sxs-lookup"><span data-stu-id="1f3e6-132">-Name</span></span>
<span data-ttu-id="1f3e6-133">배포의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-133">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="1f3e6-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f3e6-134">-ResourceGroupName</span></span>
<span data-ttu-id="1f3e6-135">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="1f3e6-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1f3e6-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f3e6-136">-ResourceId</span></span>
<span data-ttu-id="1f3e6-137">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="1f3e6-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1f3e6-138">-확인</span><span class="sxs-lookup"><span data-stu-id="1f3e6-138">-Confirm</span></span>
<span data-ttu-id="1f3e6-139">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f3e6-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f3e6-140">-WhatIf</span></span>
<span data-ttu-id="1f3e6-141">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f3e6-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f3e6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f3e6-143">CommonParameters</span></span>
<span data-ttu-id="1f3e6-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f3e6-145">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f3e6-146">입력</span><span class="sxs-lookup"><span data-stu-id="1f3e6-146">INPUTS</span></span>

### <span data-ttu-id="1f3e6-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1f3e6-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1f3e6-148">System.String</span><span class="sxs-lookup"><span data-stu-id="1f3e6-148">System.String</span></span>

## <span data-ttu-id="1f3e6-149">출력</span><span class="sxs-lookup"><span data-stu-id="1f3e6-149">OUTPUTS</span></span>

### <span data-ttu-id="1f3e6-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="1f3e6-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="1f3e6-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1f3e6-151">NOTES</span></span>

## <span data-ttu-id="1f3e6-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f3e6-152">RELATED LINKS</span></span>
