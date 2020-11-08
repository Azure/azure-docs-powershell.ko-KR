---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdeploymentmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
ms.openlocfilehash: 570caa5d788fae000834a7f3a79230849daf372f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214919"
---
# <span data-ttu-id="1f7b8-101">Invoke-AzIotHubDeploymentMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="1f7b8-101">Invoke-AzIotHubDeploymentMetricsQuery</span></span>

## <span data-ttu-id="1f7b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f7b8-102">SYNOPSIS</span></span>
<span data-ttu-id="1f7b8-103">IoT Edge 배포 메트릭 쿼리를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-103">Invoke an IoT Edge deployment metric query.</span></span>

## <span data-ttu-id="1f7b8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1f7b8-104">SYNTAX</span></span>

### <span data-ttu-id="1f7b8-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="1f7b8-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f7b8-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1f7b8-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f7b8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1f7b8-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f7b8-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1f7b8-108">DESCRIPTION</span></span>
<span data-ttu-id="1f7b8-109">IoT Edge 배포에 정의 된 대상 사용자 지정 또는 시스템 메트릭을 평가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-109">Evaluate a target custom or system metric defined in an IoT Edge deployment.</span></span>
<span data-ttu-id="1f7b8-110">Iot Hub로 계산 되며 사용자 지정할 수 없는 미리 정의 된 시스템 메트릭이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="1f7b8-111">"대상"은 배포 대상 지정 조건과 일치 하는 IoT Edge 장치를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-111">"Targeted" shows the IoT Edge devices that match the deployment targeting condition.</span></span>
- <span data-ttu-id="1f7b8-112">"적용 됨"을 지정 하면 우선 순위가 높은 다른 배포의 대상으로 지정 되지 않은 IoT Edge 장치가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-112">"Applied" shows the targeted IoT Edge devices that are not targeted by another deployment of higher priority.</span></span>
- <span data-ttu-id="1f7b8-113">"보고 성공"은 모듈이 성공적으로 배포 되었다고 보고 한 IoT Edge 장치를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-113">"Reporting Success" shows the IoT Edge devices that have reported that the modules have been deployed successfully.</span></span>
- <span data-ttu-id="1f7b8-114">"보고 실패"는 하나 이상의 모듈이 성공적으로 배포 되지 않았다고 보고 한 IoT Edge 장치를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-114">"Reporting Failure" shows the IoT Edge devices that have reported that one or more modules haven't been deployed successfully.</span></span> 
  <span data-ttu-id="1f7b8-115">오류를 자세히 조사 하려면 해당 장치에 원격으로 연결 하 고 로그 파일을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-115">To further investigate the error, connect remotely to those devices and view the log files.</span></span>

## <span data-ttu-id="1f7b8-116">예제의</span><span class="sxs-lookup"><span data-stu-id="1f7b8-116">EXAMPLES</span></span>

### <span data-ttu-id="1f7b8-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="1f7b8-117">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeploymentMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "warningLimit"
```

<span data-ttu-id="1f7b8-118">사용자 지정 정의 ' warningLimit ' 메트릭을 평가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-118">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="1f7b8-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="1f7b8-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeployMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "Reporting Success" -MetricType "system"
```

<span data-ttu-id="1f7b8-120">시스템의 ' 보고 성공 ' 메트릭을 평가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-120">Evaluate the system 'Reporting Success' metric.</span></span>

## <span data-ttu-id="1f7b8-121">변수</span><span class="sxs-lookup"><span data-stu-id="1f7b8-121">PARAMETERS</span></span>

### <span data-ttu-id="1f7b8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f7b8-122">-DefaultProfile</span></span>
<span data-ttu-id="1f7b8-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f7b8-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f7b8-124">-InputObject</span></span>
<span data-ttu-id="1f7b8-125">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="1f7b8-125">IotHub object</span></span>

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

### <span data-ttu-id="1f7b8-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="1f7b8-126">-IotHubName</span></span>
<span data-ttu-id="1f7b8-127">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="1f7b8-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1f7b8-128">-MetricName</span><span class="sxs-lookup"><span data-stu-id="1f7b8-128">-MetricName</span></span>
<span data-ttu-id="1f7b8-129">평가를 위한 대상 메트릭입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-129">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="1f7b8-130">-MetricType</span><span class="sxs-lookup"><span data-stu-id="1f7b8-130">-MetricType</span></span>
<span data-ttu-id="1f7b8-131">메트릭을 조회 하는 데 사용 해야 하는 메트릭 컬렉션을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-131">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="1f7b8-132">-이름</span><span class="sxs-lookup"><span data-stu-id="1f7b8-132">-Name</span></span>
<span data-ttu-id="1f7b8-133">배포의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-133">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="1f7b8-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f7b8-134">-ResourceGroupName</span></span>
<span data-ttu-id="1f7b8-135">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1f7b8-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f7b8-136">-ResourceId</span></span>
<span data-ttu-id="1f7b8-137">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="1f7b8-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1f7b8-138">-확인</span><span class="sxs-lookup"><span data-stu-id="1f7b8-138">-Confirm</span></span>
<span data-ttu-id="1f7b8-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f7b8-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f7b8-140">-WhatIf</span></span>
<span data-ttu-id="1f7b8-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f7b8-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f7b8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f7b8-143">CommonParameters</span></span>
<span data-ttu-id="1f7b8-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f7b8-145">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f7b8-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f7b8-146">입력</span><span class="sxs-lookup"><span data-stu-id="1f7b8-146">INPUTS</span></span>

### <span data-ttu-id="1f7b8-147">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="1f7b8-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1f7b8-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1f7b8-148">System.String</span></span>

## <span data-ttu-id="1f7b8-149">출력</span><span class="sxs-lookup"><span data-stu-id="1f7b8-149">OUTPUTS</span></span>

### <span data-ttu-id="1f7b8-150">IotHub. PSConfigurationMetricsResult/. \*</span><span class="sxs-lookup"><span data-stu-id="1f7b8-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="1f7b8-151">상속자</span><span class="sxs-lookup"><span data-stu-id="1f7b8-151">NOTES</span></span>

## <span data-ttu-id="1f7b8-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f7b8-152">RELATED LINKS</span></span>
