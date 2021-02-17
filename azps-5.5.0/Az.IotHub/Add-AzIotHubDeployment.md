---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
ms.openlocfilehash: 0e3065cb2ee668f6b0ef5b20ac25ee51d922edc7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188276"
---
# <span data-ttu-id="fe3fd-101">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="fe3fd-101">Add-AzIotHubDeployment</span></span>

## <span data-ttu-id="fe3fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe3fd-102">SYNOPSIS</span></span>
<span data-ttu-id="fe3fd-103">대상 IoT Hub에 IoT Edge 배포를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="fe3fd-103">Add an IoT Edge deployment in a target IoT Hub.</span></span>

## <span data-ttu-id="fe3fd-104">구문</span><span class="sxs-lookup"><span data-stu-id="fe3fd-104">SYNTAX</span></span>

### <span data-ttu-id="fe3fd-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="fe3fd-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-ModulesContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe3fd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fe3fd-106">InputObjectSet</span></span>
```
Add-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-ModulesContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe3fd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fe3fd-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-ModulesContent <Hashtable>] [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe3fd-108">설명</span><span class="sxs-lookup"><span data-stu-id="fe3fd-108">DESCRIPTION</span></span>
<span data-ttu-id="fe3fd-109">에지 배포는 사용자 정의 메트릭을 사용하여 수요 평가를 위해 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe3fd-109">Edge deployments can be created with user defined metrics for on demand evaluation.</span></span>
<span data-ttu-id="fe3fd-110">자세한 https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fe3fd-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="fe3fd-111">예제</span><span class="sxs-lookup"><span data-stu-id="fe3fd-111">EXAMPLES</span></span>

### <span data-ttu-id="fe3fd-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="fe3fd-112">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="fe3fd-113">기본 메타데이터를 사용하여 Edge 배포를 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="fe3fd-113">Create an Edge deployment with default metadata.</span></span>

### <span data-ttu-id="fe3fd-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="fe3fd-114">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="fe3fd-115">디바이스가 건물 9에서 태그가 지정되어 환경이 '테스트'인 경우 조건에 적용되는 우선 순위가 3인 Edge 배포를 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="fe3fd-115">Create an Edge deployment with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="fe3fd-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="fe3fd-116">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Metric $metrics
```

<span data-ttu-id="fe3fd-117">사용자 메트릭을 사용하여 Edge 배포를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe3fd-117">Create an Edge deployment with user metrics.</span></span>

### <span data-ttu-id="fe3fd-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="fe3fd-118">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels
```

<span data-ttu-id="fe3fd-119">레이블이 있는 Edge 배포를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe3fd-119">Create an Edge deployment with labels.</span></span>

### <span data-ttu-id="fe3fd-120">예제 4</span><span class="sxs-lookup"><span data-stu-id="fe3fd-120">Example 4</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -ModulesContent $content -TargetCondition "from devices.modules where tags.environment='test'"
```

<span data-ttu-id="fe3fd-121">콘텐츠가 있는 Edge 배포를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe3fd-121">Create an Edge deployment with content.</span></span>

## <span data-ttu-id="fe3fd-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe3fd-122">PARAMETERS</span></span>

### <span data-ttu-id="fe3fd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe3fd-123">-DefaultProfile</span></span>
<span data-ttu-id="fe3fd-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fe3fd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe3fd-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe3fd-125">-InputObject</span></span>
<span data-ttu-id="fe3fd-126">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="fe3fd-126">IotHub object</span></span>

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

### <span data-ttu-id="fe3fd-127">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="fe3fd-127">-IotHubName</span></span>
<span data-ttu-id="fe3fd-128">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="fe3fd-128">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fe3fd-129">-Label</span><span class="sxs-lookup"><span data-stu-id="fe3fd-129">-Label</span></span>
<span data-ttu-id="fe3fd-130">대상 배포에 적용할 레이블의 맵입니다.</span><span class="sxs-lookup"><span data-stu-id="fe3fd-130">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="fe3fd-131">-Metric</span><span class="sxs-lookup"><span data-stu-id="fe3fd-131">-Metric</span></span>
<span data-ttu-id="fe3fd-132">IoT Edge 배포 메트릭 정의에 대한 쿼리 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="fe3fd-132">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="fe3fd-133">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="fe3fd-133">-ModulesContent</span></span>
<span data-ttu-id="fe3fd-134">IoT Edge 디바이스용 모듈의 배포 콘텐츠입니다.</span><span class="sxs-lookup"><span data-stu-id="fe3fd-134">Deployment content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="fe3fd-135">-Name</span><span class="sxs-lookup"><span data-stu-id="fe3fd-135">-Name</span></span>
<span data-ttu-id="fe3fd-136">배포에 대한 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="fe3fd-136">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="fe3fd-137">-Priority</span><span class="sxs-lookup"><span data-stu-id="fe3fd-137">-Priority</span></span>
<span data-ttu-id="fe3fd-138">경쟁 규칙의 경우 배포 가중치(최고 우승).</span><span class="sxs-lookup"><span data-stu-id="fe3fd-138">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="fe3fd-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe3fd-139">-ResourceGroupName</span></span>
<span data-ttu-id="fe3fd-140">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="fe3fd-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fe3fd-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe3fd-141">-ResourceId</span></span>
<span data-ttu-id="fe3fd-142">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="fe3fd-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fe3fd-143">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="fe3fd-143">-TargetCondition</span></span>
<span data-ttu-id="fe3fd-144">Edge 배포가 적용되는 대상 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="fe3fd-144">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="fe3fd-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe3fd-145">-Confirm</span></span>
<span data-ttu-id="fe3fd-146">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fe3fd-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe3fd-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe3fd-147">-WhatIf</span></span>
<span data-ttu-id="fe3fd-148">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fe3fd-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe3fd-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fe3fd-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe3fd-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe3fd-150">CommonParameters</span></span>
<span data-ttu-id="fe3fd-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fe3fd-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe3fd-152">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fe3fd-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe3fd-153">입력</span><span class="sxs-lookup"><span data-stu-id="fe3fd-153">INPUTS</span></span>

### <span data-ttu-id="fe3fd-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fe3fd-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fe3fd-155">System.String</span><span class="sxs-lookup"><span data-stu-id="fe3fd-155">System.String</span></span>

## <span data-ttu-id="fe3fd-156">출력</span><span class="sxs-lookup"><span data-stu-id="fe3fd-156">OUTPUTS</span></span>

### <span data-ttu-id="fe3fd-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSD</span><span class="sxs-lookup"><span data-stu-id="fe3fd-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="fe3fd-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fe3fd-158">NOTES</span></span>

## <span data-ttu-id="fe3fd-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fe3fd-159">RELATED LINKS</span></span>
