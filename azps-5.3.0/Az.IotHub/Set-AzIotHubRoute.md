---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
ms.openlocfilehash: a54bfdb26b7013e490ca36e4ae5608da228d9d70
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386464"
---
# <span data-ttu-id="2eadf-101">Set-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="2eadf-101">Set-AzIotHubRoute</span></span>

## <span data-ttu-id="2eadf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2eadf-102">SYNOPSIS</span></span>
<span data-ttu-id="2eadf-103">IoT Hub에서 경로 업데이트</span><span class="sxs-lookup"><span data-stu-id="2eadf-103">Update a route in IoT Hub</span></span>

## <span data-ttu-id="2eadf-104">구문</span><span class="sxs-lookup"><span data-stu-id="2eadf-104">SYNTAX</span></span>

### <span data-ttu-id="2eadf-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="2eadf-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 [-Source <PSRoutingSource>] [-EndpointName <String>] [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eadf-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2eadf-106">InputObjectSet</span></span>
```
Set-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eadf-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2eadf-107">ResourceIdSet</span></span>
```
Set-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2eadf-108">설명</span><span class="sxs-lookup"><span data-stu-id="2eadf-108">DESCRIPTION</span></span>
<span data-ttu-id="2eadf-109">경로를 편집합니다.</span><span class="sxs-lookup"><span data-stu-id="2eadf-109">Edit a route.</span></span> <span data-ttu-id="2eadf-110">데이터 원본, 엔드포인트, 라우팅 쿼리를 포함하여 경로의 모든 필드를 업데이트하고 경로를 사용 또는 사용하지 않도록 설정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2eadf-110">You can update all the fields in a route including the data source, endpoint, routing query and also enable or disable the route.</span></span>

## <span data-ttu-id="2eadf-111">예제</span><span class="sxs-lookup"><span data-stu-id="2eadf-111">EXAMPLES</span></span>

### <span data-ttu-id="2eadf-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="2eadf-112">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source TwinChangeEvents 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="2eadf-113">경로 정보 업데이트.</span><span class="sxs-lookup"><span data-stu-id="2eadf-113">Updating the route information.</span></span>

### <span data-ttu-id="2eadf-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="2eadf-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -EndpointName E1 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="2eadf-115">경로 정보 업데이트.</span><span class="sxs-lookup"><span data-stu-id="2eadf-115">Updating the route information.</span></span>

### <span data-ttu-id="2eadf-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="2eadf-116">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Enabled

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : True
```

<span data-ttu-id="2eadf-117">경로 정보 업데이트.</span><span class="sxs-lookup"><span data-stu-id="2eadf-117">Updating the route information.</span></span>

## <span data-ttu-id="2eadf-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2eadf-118">PARAMETERS</span></span>

### <span data-ttu-id="2eadf-119">-Condition</span><span class="sxs-lookup"><span data-stu-id="2eadf-119">-Condition</span></span>
<span data-ttu-id="2eadf-120">라우팅 규칙을 적용하기 위해 평가되는 조건</span><span class="sxs-lookup"><span data-stu-id="2eadf-120">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="2eadf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eadf-121">-DefaultProfile</span></span>
<span data-ttu-id="2eadf-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2eadf-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2eadf-123">-Enabled</span><span class="sxs-lookup"><span data-stu-id="2eadf-123">-Enabled</span></span>
<span data-ttu-id="2eadf-124">경로 사용</span><span class="sxs-lookup"><span data-stu-id="2eadf-124">Enable route</span></span>

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

### <span data-ttu-id="2eadf-125">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2eadf-125">-EndpointName</span></span>
<span data-ttu-id="2eadf-126">라우팅 엔드포인트의 이름</span><span class="sxs-lookup"><span data-stu-id="2eadf-126">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="2eadf-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2eadf-127">-InputObject</span></span>
<span data-ttu-id="2eadf-128">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="2eadf-128">IotHub Object</span></span>

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

### <span data-ttu-id="2eadf-129">-Name</span><span class="sxs-lookup"><span data-stu-id="2eadf-129">-Name</span></span>
<span data-ttu-id="2eadf-130">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="2eadf-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2eadf-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eadf-131">-ResourceGroupName</span></span>
<span data-ttu-id="2eadf-132">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="2eadf-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2eadf-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2eadf-133">-ResourceId</span></span>
<span data-ttu-id="2eadf-134">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="2eadf-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="2eadf-135">-RouteName</span><span class="sxs-lookup"><span data-stu-id="2eadf-135">-RouteName</span></span>
<span data-ttu-id="2eadf-136">경로의 이름</span><span class="sxs-lookup"><span data-stu-id="2eadf-136">Name of the Route</span></span>

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

### <span data-ttu-id="2eadf-137">-Source</span><span class="sxs-lookup"><span data-stu-id="2eadf-137">-Source</span></span>
<span data-ttu-id="2eadf-138">경로의 원본</span><span class="sxs-lookup"><span data-stu-id="2eadf-138">Source of the route</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource]
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eadf-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2eadf-139">-Confirm</span></span>
<span data-ttu-id="2eadf-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2eadf-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eadf-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eadf-141">-WhatIf</span></span>
<span data-ttu-id="2eadf-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2eadf-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2eadf-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2eadf-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2eadf-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eadf-144">CommonParameters</span></span>
<span data-ttu-id="2eadf-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2eadf-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eadf-146">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2eadf-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eadf-147">입력</span><span class="sxs-lookup"><span data-stu-id="2eadf-147">INPUTS</span></span>

### <span data-ttu-id="2eadf-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="2eadf-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2eadf-149">System.String</span><span class="sxs-lookup"><span data-stu-id="2eadf-149">System.String</span></span>

## <span data-ttu-id="2eadf-150">출력</span><span class="sxs-lookup"><span data-stu-id="2eadf-150">OUTPUTS</span></span>

### <span data-ttu-id="2eadf-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="2eadf-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="2eadf-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2eadf-152">NOTES</span></span>

## <span data-ttu-id="2eadf-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2eadf-153">RELATED LINKS</span></span>
