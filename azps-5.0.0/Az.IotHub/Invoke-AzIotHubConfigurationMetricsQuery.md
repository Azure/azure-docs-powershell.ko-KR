---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubconfigurationmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
ms.openlocfilehash: 85793ba3097297de646db4695cac36173bb01673
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226986"
---
# <span data-ttu-id="967f4-101">Invoke-AzIotHubConfigurationMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="967f4-101">Invoke-AzIotHubConfigurationMetricsQuery</span></span>

## <span data-ttu-id="967f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="967f4-102">SYNOPSIS</span></span>
<span data-ttu-id="967f4-103">IoT 장치 구성 메트릭 쿼리를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="967f4-103">Invoke an IoT device configuration metric query.</span></span>

## <span data-ttu-id="967f4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="967f4-104">SYNTAX</span></span>

### <span data-ttu-id="967f4-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="967f4-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="967f4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="967f4-106">InputObjectSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="967f4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="967f4-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="967f4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="967f4-108">DESCRIPTION</span></span>
<span data-ttu-id="967f4-109">IoT 장치 구성에 정의 된 대상 사용자 지정 또는 시스템 메트릭을 평가 합니다.</span><span class="sxs-lookup"><span data-stu-id="967f4-109">Evaluate a target custom or system metric defined in an IoT device configuration.</span></span>
<span data-ttu-id="967f4-110">Iot Hub로 계산 되며 사용자 지정할 수 없는 미리 정의 된 시스템 메트릭이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="967f4-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="967f4-111">"대상"은 대상 조건과 일치 하는 장치 twins 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="967f4-111">"Targeted" specifies the number of device twins that match the target condition.</span></span>
- <span data-ttu-id="967f4-112">"적용 됨"이 구성에 의해 수정 된 장치 twins 수를 지정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="967f4-112">"Applied" specified the number of device twins that have been modified by the configuration.</span></span> 

## <span data-ttu-id="967f4-113">예제의</span><span class="sxs-lookup"><span data-stu-id="967f4-113">EXAMPLES</span></span>

### <span data-ttu-id="967f4-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="967f4-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigurationMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "warningLimit"
```

<span data-ttu-id="967f4-115">사용자 지정 정의 ' warningLimit ' 메트릭을 평가 합니다.</span><span class="sxs-lookup"><span data-stu-id="967f4-115">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="967f4-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="967f4-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "applied" -MetricType "system"
```

<span data-ttu-id="967f4-117">시스템의 적용 된 메트릭을 평가 합니다.</span><span class="sxs-lookup"><span data-stu-id="967f4-117">Evaluate the system 'applied' metric.</span></span>

## <span data-ttu-id="967f4-118">변수</span><span class="sxs-lookup"><span data-stu-id="967f4-118">PARAMETERS</span></span>

### <span data-ttu-id="967f4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="967f4-119">-DefaultProfile</span></span>
<span data-ttu-id="967f4-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="967f4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="967f4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="967f4-121">-InputObject</span></span>
<span data-ttu-id="967f4-122">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="967f4-122">IotHub object</span></span>

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

### <span data-ttu-id="967f4-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="967f4-123">-IotHubName</span></span>
<span data-ttu-id="967f4-124">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="967f4-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="967f4-125">-MetricName</span><span class="sxs-lookup"><span data-stu-id="967f4-125">-MetricName</span></span>
<span data-ttu-id="967f4-126">평가를 위한 대상 메트릭입니다.</span><span class="sxs-lookup"><span data-stu-id="967f4-126">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="967f4-127">-MetricType</span><span class="sxs-lookup"><span data-stu-id="967f4-127">-MetricType</span></span>
<span data-ttu-id="967f4-128">메트릭을 조회 하는 데 사용 해야 하는 메트릭 컬렉션을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="967f4-128">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="967f4-129">-이름</span><span class="sxs-lookup"><span data-stu-id="967f4-129">-Name</span></span>
<span data-ttu-id="967f4-130">구성의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="967f4-130">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="967f4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="967f4-131">-ResourceGroupName</span></span>
<span data-ttu-id="967f4-132">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="967f4-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="967f4-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="967f4-133">-ResourceId</span></span>
<span data-ttu-id="967f4-134">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="967f4-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="967f4-135">-확인</span><span class="sxs-lookup"><span data-stu-id="967f4-135">-Confirm</span></span>
<span data-ttu-id="967f4-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="967f4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="967f4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="967f4-137">-WhatIf</span></span>
<span data-ttu-id="967f4-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="967f4-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="967f4-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="967f4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="967f4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="967f4-140">CommonParameters</span></span>
<span data-ttu-id="967f4-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="967f4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="967f4-142">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="967f4-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="967f4-143">입력</span><span class="sxs-lookup"><span data-stu-id="967f4-143">INPUTS</span></span>

### <span data-ttu-id="967f4-144">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="967f4-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="967f4-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="967f4-145">System.String</span></span>

## <span data-ttu-id="967f4-146">출력</span><span class="sxs-lookup"><span data-stu-id="967f4-146">OUTPUTS</span></span>

### <span data-ttu-id="967f4-147">IotHub. PSConfigurationMetricsResult/. \*</span><span class="sxs-lookup"><span data-stu-id="967f4-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="967f4-148">상속자</span><span class="sxs-lookup"><span data-stu-id="967f4-148">NOTES</span></span>

## <span data-ttu-id="967f4-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="967f4-149">RELATED LINKS</span></span>
