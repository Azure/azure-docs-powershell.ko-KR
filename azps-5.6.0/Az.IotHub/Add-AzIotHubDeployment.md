---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
ms.openlocfilehash: 80494fd18216ce42883a962920ab78bbc2aa628b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997929"
---
# <span data-ttu-id="7887a-101">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="7887a-101">Add-AzIotHubDeployment</span></span>

## <span data-ttu-id="7887a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7887a-102">SYNOPSIS</span></span>
<span data-ttu-id="7887a-103">대상 IoT Hub에 IoT Edge 배포를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7887a-103">Add an IoT Edge deployment in a target IoT Hub.</span></span>

## <span data-ttu-id="7887a-104">구문</span><span class="sxs-lookup"><span data-stu-id="7887a-104">SYNTAX</span></span>

### <span data-ttu-id="7887a-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7887a-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-ModulesContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7887a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7887a-106">InputObjectSet</span></span>
```
Add-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-ModulesContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7887a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7887a-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-ModulesContent <Hashtable>] [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7887a-108">설명</span><span class="sxs-lookup"><span data-stu-id="7887a-108">DESCRIPTION</span></span>
<span data-ttu-id="7887a-109">에지 배포는 사용자 정의 메트릭을 사용하여 수요 평가를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7887a-109">Edge deployments can be created with user defined metrics for on demand evaluation.</span></span>
<span data-ttu-id="7887a-110">자세한 https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring 내용은 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7887a-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="7887a-111">예제</span><span class="sxs-lookup"><span data-stu-id="7887a-111">EXAMPLES</span></span>

### <span data-ttu-id="7887a-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="7887a-112">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="7887a-113">기본 메타데이터를 사용하여 Edge 배포를 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="7887a-113">Create an Edge deployment with default metadata.</span></span>

### <span data-ttu-id="7887a-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="7887a-114">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="7887a-115">디바이스가 건물 9에서 태그가 지정되어 환경이 '테스트'인 경우 조건에 적용되는 3의 우선 순위가 있는 Edge 배포를 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="7887a-115">Create an Edge deployment with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="7887a-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="7887a-116">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Metric $metrics
```

<span data-ttu-id="7887a-117">사용자 메트릭을 사용하여 Edge 배포를 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="7887a-117">Create an Edge deployment with user metrics.</span></span>

### <span data-ttu-id="7887a-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="7887a-118">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels
```

<span data-ttu-id="7887a-119">레이블을 사용하여 Edge 배포를 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="7887a-119">Create an Edge deployment with labels.</span></span>

### <span data-ttu-id="7887a-120">예제 4</span><span class="sxs-lookup"><span data-stu-id="7887a-120">Example 4</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -ModulesContent $content -TargetCondition "from devices.modules where tags.environment='test'"
```

<span data-ttu-id="7887a-121">콘텐츠가 있는 Edge 배포를 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="7887a-121">Create an Edge deployment with content.</span></span>

## <span data-ttu-id="7887a-122">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7887a-122">PARAMETERS</span></span>

### <span data-ttu-id="7887a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7887a-123">-DefaultProfile</span></span>
<span data-ttu-id="7887a-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7887a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7887a-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7887a-125">-InputObject</span></span>
<span data-ttu-id="7887a-126">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="7887a-126">IotHub object</span></span>

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

### <span data-ttu-id="7887a-127">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="7887a-127">-IotHubName</span></span>
<span data-ttu-id="7887a-128">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="7887a-128">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7887a-129">-Label</span><span class="sxs-lookup"><span data-stu-id="7887a-129">-Label</span></span>
<span data-ttu-id="7887a-130">대상 배포에 적용할 레이블의 지도입니다.</span><span class="sxs-lookup"><span data-stu-id="7887a-130">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="7887a-131">-Metric</span><span class="sxs-lookup"><span data-stu-id="7887a-131">-Metric</span></span>
<span data-ttu-id="7887a-132">IoT Edge 배포 메트릭 정의에 대한 쿼리 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="7887a-132">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="7887a-133">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="7887a-133">-ModulesContent</span></span>
<span data-ttu-id="7887a-134">IoT Edge 디바이스용 모듈의 배포 콘텐츠입니다.</span><span class="sxs-lookup"><span data-stu-id="7887a-134">Deployment content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="7887a-135">-Name</span><span class="sxs-lookup"><span data-stu-id="7887a-135">-Name</span></span>
<span data-ttu-id="7887a-136">배포의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7887a-136">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="7887a-137">-Priority</span><span class="sxs-lookup"><span data-stu-id="7887a-137">-Priority</span></span>
<span data-ttu-id="7887a-138">경쟁 규칙(가장 높은 승리)의 경우 배포의 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="7887a-138">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="7887a-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7887a-139">-ResourceGroupName</span></span>
<span data-ttu-id="7887a-140">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="7887a-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7887a-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7887a-141">-ResourceId</span></span>
<span data-ttu-id="7887a-142">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="7887a-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7887a-143">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="7887a-143">-TargetCondition</span></span>
<span data-ttu-id="7887a-144">Edge 배포가 적용되는 대상 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="7887a-144">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="7887a-145">-확인</span><span class="sxs-lookup"><span data-stu-id="7887a-145">-Confirm</span></span>
<span data-ttu-id="7887a-146">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7887a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7887a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7887a-147">-WhatIf</span></span>
<span data-ttu-id="7887a-148">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7887a-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7887a-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7887a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7887a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7887a-150">CommonParameters</span></span>
<span data-ttu-id="7887a-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7887a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7887a-152">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7887a-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7887a-153">입력</span><span class="sxs-lookup"><span data-stu-id="7887a-153">INPUTS</span></span>

### <span data-ttu-id="7887a-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7887a-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7887a-155">System.String</span><span class="sxs-lookup"><span data-stu-id="7887a-155">System.String</span></span>

## <span data-ttu-id="7887a-156">출력</span><span class="sxs-lookup"><span data-stu-id="7887a-156">OUTPUTS</span></span>

### <span data-ttu-id="7887a-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDMicrosoft.Azure.Commands.Management.IotHub.Models.PSD</span><span class="sxs-lookup"><span data-stu-id="7887a-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="7887a-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7887a-158">NOTES</span></span>

## <span data-ttu-id="7887a-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7887a-159">RELATED LINKS</span></span>
