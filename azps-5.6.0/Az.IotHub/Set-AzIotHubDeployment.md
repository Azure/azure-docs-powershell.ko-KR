---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
ms.openlocfilehash: 5a0c56a946e9f81163a94a092e646acbc99fb6cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956144"
---
# <span data-ttu-id="87b64-101">Set-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="87b64-101">Set-AzIotHubDeployment</span></span>

## <span data-ttu-id="87b64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87b64-102">SYNOPSIS</span></span>
<span data-ttu-id="87b64-103">IoT Edge 배포의 변경 가능한 필드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="87b64-103">Update the mutable fields of IoT Edge deployment.</span></span>

## <span data-ttu-id="87b64-104">구문</span><span class="sxs-lookup"><span data-stu-id="87b64-104">SYNTAX</span></span>

### <span data-ttu-id="87b64-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="87b64-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87b64-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="87b64-106">InputObjectSet</span></span>
```
Set-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87b64-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="87b64-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87b64-108">설명</span><span class="sxs-lookup"><span data-stu-id="87b64-108">DESCRIPTION</span></span>
<span data-ttu-id="87b64-109">IoT Edge 배포의 지정된 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="87b64-109">Update specified properties of an IoT Edge deployment.</span></span>
<span data-ttu-id="87b64-110">참고: 구성 콘텐츠는 변경 불가능합니다.</span><span class="sxs-lookup"><span data-stu-id="87b64-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="87b64-111">업데이트할 수 있는 구성 속성은 '레이블', '메트릭', '우선 순위' 및 'targetCondition'입니다.</span><span class="sxs-lookup"><span data-stu-id="87b64-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="87b64-112">자세한 https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  내용은 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="87b64-112">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  for more information.</span></span>

## <span data-ttu-id="87b64-113">예제</span><span class="sxs-lookup"><span data-stu-id="87b64-113">EXAMPLES</span></span>

### <span data-ttu-id="87b64-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="87b64-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="87b64-115">IoT Edge 배포의 우선 순위를 변경하고 대상 조건을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="87b64-115">Alter the priority of IoT Edge deployment and update its target condition.</span></span>

### <span data-ttu-id="87b64-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="87b64-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels -Metric $metrics
```

<span data-ttu-id="87b64-117">IoT Edge 배포의 메트릭 및 레이블을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="87b64-117">Update the metrics and labels of IoT Edge deployment.</span></span>

## <span data-ttu-id="87b64-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="87b64-118">PARAMETERS</span></span>

### <span data-ttu-id="87b64-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87b64-119">-DefaultProfile</span></span>
<span data-ttu-id="87b64-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="87b64-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87b64-121">-Force</span><span class="sxs-lookup"><span data-stu-id="87b64-121">-Force</span></span>
<span data-ttu-id="87b64-122">배포 개체를 마지막으로 검색한 후 업데이트된 경우에도 배포 개체를 바꿀 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87b64-122">Allows deployment object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="87b64-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87b64-123">-InputObject</span></span>
<span data-ttu-id="87b64-124">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="87b64-124">IotHub object</span></span>

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

### <span data-ttu-id="87b64-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="87b64-125">-IotHubName</span></span>
<span data-ttu-id="87b64-126">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="87b64-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="87b64-127">-Label</span><span class="sxs-lookup"><span data-stu-id="87b64-127">-Label</span></span>
<span data-ttu-id="87b64-128">대상 배포에 적용할 레이블의 지도입니다.</span><span class="sxs-lookup"><span data-stu-id="87b64-128">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="87b64-129">-Metric</span><span class="sxs-lookup"><span data-stu-id="87b64-129">-Metric</span></span>
<span data-ttu-id="87b64-130">IoT Edge 배포 메트릭 정의에 대한 쿼리 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="87b64-130">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="87b64-131">-Name</span><span class="sxs-lookup"><span data-stu-id="87b64-131">-Name</span></span>
<span data-ttu-id="87b64-132">배포의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="87b64-132">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="87b64-133">-Priority</span><span class="sxs-lookup"><span data-stu-id="87b64-133">-Priority</span></span>
<span data-ttu-id="87b64-134">경쟁 규칙(가장 높은 승리)의 경우 배포의 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="87b64-134">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="87b64-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87b64-135">-ResourceGroupName</span></span>
<span data-ttu-id="87b64-136">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="87b64-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="87b64-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87b64-137">-ResourceId</span></span>
<span data-ttu-id="87b64-138">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="87b64-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="87b64-139">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="87b64-139">-TargetCondition</span></span>
<span data-ttu-id="87b64-140">Edge 배포가 적용되는 대상 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="87b64-140">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="87b64-141">-확인</span><span class="sxs-lookup"><span data-stu-id="87b64-141">-Confirm</span></span>
<span data-ttu-id="87b64-142">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="87b64-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87b64-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87b64-143">-WhatIf</span></span>
<span data-ttu-id="87b64-144">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="87b64-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87b64-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="87b64-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87b64-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87b64-146">CommonParameters</span></span>
<span data-ttu-id="87b64-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="87b64-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87b64-148">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="87b64-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87b64-149">입력</span><span class="sxs-lookup"><span data-stu-id="87b64-149">INPUTS</span></span>

### <span data-ttu-id="87b64-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="87b64-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="87b64-151">System.String</span><span class="sxs-lookup"><span data-stu-id="87b64-151">System.String</span></span>

## <span data-ttu-id="87b64-152">출력</span><span class="sxs-lookup"><span data-stu-id="87b64-152">OUTPUTS</span></span>

### <span data-ttu-id="87b64-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDMicrosoft.Azure.Commands.Management.IotHub.Models.PSD</span><span class="sxs-lookup"><span data-stu-id="87b64-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="87b64-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="87b64-154">NOTES</span></span>

## <span data-ttu-id="87b64-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="87b64-155">RELATED LINKS</span></span>
