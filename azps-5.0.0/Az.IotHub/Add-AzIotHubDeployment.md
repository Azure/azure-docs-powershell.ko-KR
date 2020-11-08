---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
ms.openlocfilehash: 375e225d4c09368fac82db240988132952a0ada7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217790"
---
# <span data-ttu-id="62219-101">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="62219-101">Add-AzIotHubDeployment</span></span>

## <span data-ttu-id="62219-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62219-102">SYNOPSIS</span></span>
<span data-ttu-id="62219-103">대상 IoT Hub에 IoT Edge 배포를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="62219-103">Add an IoT Edge deployment in a target IoT Hub.</span></span>

## <span data-ttu-id="62219-104">구문과</span><span class="sxs-lookup"><span data-stu-id="62219-104">SYNTAX</span></span>

### <span data-ttu-id="62219-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="62219-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-ModulesContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62219-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="62219-106">InputObjectSet</span></span>
```
Add-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-ModulesContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62219-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="62219-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-ModulesContent <Hashtable>] [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62219-108">설명은</span><span class="sxs-lookup"><span data-stu-id="62219-108">DESCRIPTION</span></span>
<span data-ttu-id="62219-109">Edge 배포는 주문형 평가를 위해 사용자가 정의한 메트릭을 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62219-109">Edge deployments can be created with user defined metrics for on demand evaluation.</span></span>
<span data-ttu-id="62219-110"> https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring자세한 내용은을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="62219-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="62219-111">예제의</span><span class="sxs-lookup"><span data-stu-id="62219-111">EXAMPLES</span></span>

### <span data-ttu-id="62219-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="62219-112">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="62219-113">기본 메타 데이터로 Edge 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="62219-113">Create an Edge deployment with default metadata.</span></span>

### <span data-ttu-id="62219-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="62219-114">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="62219-115">디바이스의 빌드 9에 태그가 지정 되 고 환경이 ' 테스트 ' 인 경우 조건에 적용 되는 우선 순위 3을 사용 하 여 Edge 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="62219-115">Create an Edge deployment with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="62219-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="62219-116">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Metric $metrics
```

<span data-ttu-id="62219-117">사용자 메트릭을 사용 하 여 Edge 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="62219-117">Create an Edge deployment with user metrics.</span></span>

### <span data-ttu-id="62219-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="62219-118">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels
```

<span data-ttu-id="62219-119">레이블을 사용 하 여 Edge 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="62219-119">Create an Edge deployment with labels.</span></span>

### <span data-ttu-id="62219-120">예제 4</span><span class="sxs-lookup"><span data-stu-id="62219-120">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -ModulesContent $content
```

<span data-ttu-id="62219-121">콘텐츠를 사용 하 여 Edge 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="62219-121">Create an Edge deployment with content.</span></span>

## <span data-ttu-id="62219-122">변수</span><span class="sxs-lookup"><span data-stu-id="62219-122">PARAMETERS</span></span>

### <span data-ttu-id="62219-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62219-123">-DefaultProfile</span></span>
<span data-ttu-id="62219-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="62219-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62219-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62219-125">-InputObject</span></span>
<span data-ttu-id="62219-126">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="62219-126">IotHub object</span></span>

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

### <span data-ttu-id="62219-127">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="62219-127">-IotHubName</span></span>
<span data-ttu-id="62219-128">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="62219-128">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="62219-129">-레이블</span><span class="sxs-lookup"><span data-stu-id="62219-129">-Label</span></span>
<span data-ttu-id="62219-130">대상 배포에 적용 되는 레이블의 맵입니다.</span><span class="sxs-lookup"><span data-stu-id="62219-130">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="62219-131">-미터법</span><span class="sxs-lookup"><span data-stu-id="62219-131">-Metric</span></span>
<span data-ttu-id="62219-132">IoT Edge 배포 메트릭 정의에 대 한 쿼리 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="62219-132">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="62219-133">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="62219-133">-ModulesContent</span></span>
<span data-ttu-id="62219-134">IoT Edge 장치에 대 한 모듈 배포 콘텐츠입니다.</span><span class="sxs-lookup"><span data-stu-id="62219-134">Deployment content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="62219-135">-이름</span><span class="sxs-lookup"><span data-stu-id="62219-135">-Name</span></span>
<span data-ttu-id="62219-136">배포의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="62219-136">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="62219-137">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="62219-137">-Priority</span></span>
<span data-ttu-id="62219-138">경쟁 관계 규칙의 경우 (최고 wins) 배포의 중량.</span><span class="sxs-lookup"><span data-stu-id="62219-138">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="62219-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62219-139">-ResourceGroupName</span></span>
<span data-ttu-id="62219-140">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="62219-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="62219-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62219-141">-ResourceId</span></span>
<span data-ttu-id="62219-142">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="62219-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="62219-143">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="62219-143">-TargetCondition</span></span>
<span data-ttu-id="62219-144">Edge 배포가 적용 되는 대상 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="62219-144">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="62219-145">-확인</span><span class="sxs-lookup"><span data-stu-id="62219-145">-Confirm</span></span>
<span data-ttu-id="62219-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="62219-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62219-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62219-147">-WhatIf</span></span>
<span data-ttu-id="62219-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="62219-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62219-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="62219-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62219-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62219-150">CommonParameters</span></span>
<span data-ttu-id="62219-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="62219-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62219-152">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62219-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62219-153">입력</span><span class="sxs-lookup"><span data-stu-id="62219-153">INPUTS</span></span>

### <span data-ttu-id="62219-154">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="62219-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="62219-155">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="62219-155">System.String</span></span>

## <span data-ttu-id="62219-156">출력</span><span class="sxs-lookup"><span data-stu-id="62219-156">OUTPUTS</span></span>

### <span data-ttu-id="62219-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="62219-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="62219-158">상속자</span><span class="sxs-lookup"><span data-stu-id="62219-158">NOTES</span></span>

## <span data-ttu-id="62219-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="62219-159">RELATED LINKS</span></span>
