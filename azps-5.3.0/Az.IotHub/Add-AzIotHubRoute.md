---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
ms.openlocfilehash: a84d432e5771b5f04a7d9f478cd8ef446e08620a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495472"
---
# <span data-ttu-id="1e876-101">Add-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="1e876-101">Add-AzIotHubRoute</span></span>

## <span data-ttu-id="1e876-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e876-102">SYNOPSIS</span></span>
<span data-ttu-id="1e876-103">IoT Hub에서 경로 만들기</span><span class="sxs-lookup"><span data-stu-id="1e876-103">Create a route in IoT Hub</span></span>

## <span data-ttu-id="1e876-104">구문</span><span class="sxs-lookup"><span data-stu-id="1e876-104">SYNTAX</span></span>

### <span data-ttu-id="1e876-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1e876-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 -Source <PSRoutingSource> -EndpointName <String> [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e876-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1e876-106">InputObjectSet</span></span>
```
Add-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> -Source <PSRoutingSource>
 -EndpointName <String> [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e876-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1e876-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> -Source <PSRoutingSource> -EndpointName <String>
 [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e876-108">설명</span><span class="sxs-lookup"><span data-stu-id="1e876-108">DESCRIPTION</span></span>
<span data-ttu-id="1e876-109">특정 데이터 원본 및 조건을 원하는 엔드포인트로 보내는 경로를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1e876-109">Create a route to send specific data source and condition to a desired endpoint.</span></span>

## <span data-ttu-id="1e876-110">예제</span><span class="sxs-lookup"><span data-stu-id="1e876-110">EXAMPLES</span></span>

### <span data-ttu-id="1e876-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="1e876-111">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source DeviceMessages -EndpointName E1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : E1
Condition     : 
IsEnabled     : False
```

<span data-ttu-id="1e876-112">새 경로 "R1"을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e876-112">Create a new route "R1".</span></span>

## <span data-ttu-id="1e876-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e876-113">PARAMETERS</span></span>

### <span data-ttu-id="1e876-114">-Condition</span><span class="sxs-lookup"><span data-stu-id="1e876-114">-Condition</span></span>
<span data-ttu-id="1e876-115">라우팅 규칙을 적용하기 위해 평가되는 조건</span><span class="sxs-lookup"><span data-stu-id="1e876-115">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="1e876-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e876-116">-DefaultProfile</span></span>
<span data-ttu-id="1e876-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1e876-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e876-118">-Enabled</span><span class="sxs-lookup"><span data-stu-id="1e876-118">-Enabled</span></span>
<span data-ttu-id="1e876-119">경로 사용</span><span class="sxs-lookup"><span data-stu-id="1e876-119">Enable route</span></span>

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

### <span data-ttu-id="1e876-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="1e876-120">-EndpointName</span></span>
<span data-ttu-id="1e876-121">라우팅 엔드포인트의 이름</span><span class="sxs-lookup"><span data-stu-id="1e876-121">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="1e876-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e876-122">-InputObject</span></span>
<span data-ttu-id="1e876-123">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="1e876-123">IotHub Object</span></span>

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

### <span data-ttu-id="1e876-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1e876-124">-Name</span></span>
<span data-ttu-id="1e876-125">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="1e876-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1e876-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e876-126">-ResourceGroupName</span></span>
<span data-ttu-id="1e876-127">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="1e876-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1e876-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e876-128">-ResourceId</span></span>
<span data-ttu-id="1e876-129">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="1e876-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1e876-130">-RouteName</span><span class="sxs-lookup"><span data-stu-id="1e876-130">-RouteName</span></span>
<span data-ttu-id="1e876-131">경로의 이름</span><span class="sxs-lookup"><span data-stu-id="1e876-131">Name of the Route</span></span>

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

### <span data-ttu-id="1e876-132">-Source</span><span class="sxs-lookup"><span data-stu-id="1e876-132">-Source</span></span>
<span data-ttu-id="1e876-133">경로의 원본</span><span class="sxs-lookup"><span data-stu-id="1e876-133">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e876-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e876-134">-Confirm</span></span>
<span data-ttu-id="1e876-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e876-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e876-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e876-136">-WhatIf</span></span>
<span data-ttu-id="1e876-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1e876-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e876-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e876-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e876-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e876-139">CommonParameters</span></span>
<span data-ttu-id="1e876-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1e876-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e876-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1e876-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e876-142">입력</span><span class="sxs-lookup"><span data-stu-id="1e876-142">INPUTS</span></span>

### <span data-ttu-id="1e876-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1e876-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1e876-144">System.String</span><span class="sxs-lookup"><span data-stu-id="1e876-144">System.String</span></span>

## <span data-ttu-id="1e876-145">출력</span><span class="sxs-lookup"><span data-stu-id="1e876-145">OUTPUTS</span></span>

### <span data-ttu-id="1e876-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="1e876-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="1e876-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1e876-147">NOTES</span></span>

## <span data-ttu-id="1e876-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e876-148">RELATED LINKS</span></span>
