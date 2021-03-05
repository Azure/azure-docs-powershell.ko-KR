---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
ms.openlocfilehash: fbb0801dd586731a938c773711d72847e7a96e50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997808"
---
# <span data-ttu-id="ef33e-101">Add-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="ef33e-101">Add-AzIotHubRoute</span></span>

## <span data-ttu-id="ef33e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef33e-102">SYNOPSIS</span></span>
<span data-ttu-id="ef33e-103">IoT Hub에서 경로 만들기</span><span class="sxs-lookup"><span data-stu-id="ef33e-103">Create a route in IoT Hub</span></span>

## <span data-ttu-id="ef33e-104">구문</span><span class="sxs-lookup"><span data-stu-id="ef33e-104">SYNTAX</span></span>

### <span data-ttu-id="ef33e-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ef33e-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 -Source <PSRoutingSource> -EndpointName <String> [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef33e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ef33e-106">InputObjectSet</span></span>
```
Add-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> -Source <PSRoutingSource>
 -EndpointName <String> [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef33e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ef33e-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> -Source <PSRoutingSource> -EndpointName <String>
 [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef33e-108">설명</span><span class="sxs-lookup"><span data-stu-id="ef33e-108">DESCRIPTION</span></span>
<span data-ttu-id="ef33e-109">원하는 엔드포인트에 특정 데이터 원본 및 조건을 보내기 위한 경로를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="ef33e-109">Create a route to send specific data source and condition to a desired endpoint.</span></span>

## <span data-ttu-id="ef33e-110">예제</span><span class="sxs-lookup"><span data-stu-id="ef33e-110">EXAMPLES</span></span>

### <span data-ttu-id="ef33e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ef33e-111">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source DeviceMessages -EndpointName E1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : E1
Condition     : 
IsEnabled     : False
```

<span data-ttu-id="ef33e-112">새 경로 "R1"을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="ef33e-112">Create a new route "R1".</span></span>

## <span data-ttu-id="ef33e-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ef33e-113">PARAMETERS</span></span>

### <span data-ttu-id="ef33e-114">-조건</span><span class="sxs-lookup"><span data-stu-id="ef33e-114">-Condition</span></span>
<span data-ttu-id="ef33e-115">라우팅 규칙을 적용하기 위해 평가된 조건</span><span class="sxs-lookup"><span data-stu-id="ef33e-115">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="ef33e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef33e-116">-DefaultProfile</span></span>
<span data-ttu-id="ef33e-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ef33e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef33e-118">-사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="ef33e-118">-Enabled</span></span>
<span data-ttu-id="ef33e-119">경로 사용</span><span class="sxs-lookup"><span data-stu-id="ef33e-119">Enable route</span></span>

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

### <span data-ttu-id="ef33e-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ef33e-120">-EndpointName</span></span>
<span data-ttu-id="ef33e-121">라우팅 엔드포인트의 이름</span><span class="sxs-lookup"><span data-stu-id="ef33e-121">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="ef33e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef33e-122">-InputObject</span></span>
<span data-ttu-id="ef33e-123">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="ef33e-123">IotHub Object</span></span>

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

### <span data-ttu-id="ef33e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ef33e-124">-Name</span></span>
<span data-ttu-id="ef33e-125">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="ef33e-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ef33e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef33e-126">-ResourceGroupName</span></span>
<span data-ttu-id="ef33e-127">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="ef33e-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ef33e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef33e-128">-ResourceId</span></span>
<span data-ttu-id="ef33e-129">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="ef33e-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ef33e-130">-RouteName</span><span class="sxs-lookup"><span data-stu-id="ef33e-130">-RouteName</span></span>
<span data-ttu-id="ef33e-131">경로의 이름</span><span class="sxs-lookup"><span data-stu-id="ef33e-131">Name of the Route</span></span>

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

### <span data-ttu-id="ef33e-132">-Source</span><span class="sxs-lookup"><span data-stu-id="ef33e-132">-Source</span></span>
<span data-ttu-id="ef33e-133">경로의 원본</span><span class="sxs-lookup"><span data-stu-id="ef33e-133">Source of the route</span></span>

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

### <span data-ttu-id="ef33e-134">-확인</span><span class="sxs-lookup"><span data-stu-id="ef33e-134">-Confirm</span></span>
<span data-ttu-id="ef33e-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef33e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef33e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef33e-136">-WhatIf</span></span>
<span data-ttu-id="ef33e-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ef33e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef33e-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ef33e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef33e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef33e-139">CommonParameters</span></span>
<span data-ttu-id="ef33e-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ef33e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef33e-141">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ef33e-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef33e-142">입력</span><span class="sxs-lookup"><span data-stu-id="ef33e-142">INPUTS</span></span>

### <span data-ttu-id="ef33e-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ef33e-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ef33e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="ef33e-144">System.String</span></span>

## <span data-ttu-id="ef33e-145">출력</span><span class="sxs-lookup"><span data-stu-id="ef33e-145">OUTPUTS</span></span>

### <span data-ttu-id="ef33e-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="ef33e-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="ef33e-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ef33e-147">NOTES</span></span>

## <span data-ttu-id="ef33e-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef33e-148">RELATED LINKS</span></span>
