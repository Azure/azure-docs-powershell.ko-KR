---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: 173e84e3587a6844896791ef38a185db522d4e4b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386436"
---
# <span data-ttu-id="5ac48-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="5ac48-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="5ac48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ac48-102">SYNOPSIS</span></span>
<span data-ttu-id="5ac48-103">IoT Hub에서 경로 테스트</span><span class="sxs-lookup"><span data-stu-id="5ac48-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="5ac48-104">구문</span><span class="sxs-lookup"><span data-stu-id="5ac48-104">SYNTAX</span></span>

### <span data-ttu-id="5ac48-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5ac48-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ac48-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="5ac48-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ac48-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="5ac48-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ac48-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="5ac48-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ac48-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="5ac48-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ac48-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="5ac48-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ac48-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="5ac48-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ac48-112">설명</span><span class="sxs-lookup"><span data-stu-id="5ac48-112">DESCRIPTION</span></span>
<span data-ttu-id="5ac48-113">특정 경로를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="5ac48-113">Test a specific route.</span></span>

## <span data-ttu-id="5ac48-114">예제</span><span class="sxs-lookup"><span data-stu-id="5ac48-114">EXAMPLES</span></span>

### <span data-ttu-id="5ac48-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="5ac48-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="5ac48-116">원본 "DeviceMessages"로 모든 경로를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="5ac48-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="5ac48-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="5ac48-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="5ac48-118">특정 경로를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="5ac48-118">Test a specific route.</span></span>

### <span data-ttu-id="5ac48-119">예제 3</span><span class="sxs-lookup"><span data-stu-id="5ac48-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="5ac48-120">특정 경로를 테스트하고 실패 이유를 보여 주면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5ac48-120">Test a specific route and showing the reason of failure.</span></span>

### <span data-ttu-id="5ac48-121">예제 4</span><span class="sxs-lookup"><span data-stu-id="5ac48-121">Example 4</span></span>
```
PS C:\> $ap = @{}
PS C:\> $ap.add("key0","value0")
PS C:\> $sp = @{}
PS C:\> $sp.add("key1", "value1")
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -AppProperty $ap -SystemProperty $sp

Result : true
```

<span data-ttu-id="5ac48-122">AppProperty 및 SystemProperty를 통해 특정 경로를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="5ac48-122">Test a specific route with AppProperty and SystemProperty.</span></span>

## <span data-ttu-id="5ac48-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ac48-123">PARAMETERS</span></span>

### <span data-ttu-id="5ac48-124">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="5ac48-124">-AppProperty</span></span>
<span data-ttu-id="5ac48-125">경로 메시지의 앱 속성</span><span class="sxs-lookup"><span data-stu-id="5ac48-125">App properties of the route message</span></span>

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

### <span data-ttu-id="5ac48-126">-Body</span><span class="sxs-lookup"><span data-stu-id="5ac48-126">-Body</span></span>
<span data-ttu-id="5ac48-127">경로 메시지의 본문</span><span class="sxs-lookup"><span data-stu-id="5ac48-127">Body of the route message</span></span>

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

### <span data-ttu-id="5ac48-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ac48-128">-DefaultProfile</span></span>
<span data-ttu-id="5ac48-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5ac48-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ac48-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ac48-130">-InputObject</span></span>
<span data-ttu-id="5ac48-131">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="5ac48-131">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectTestRouteSet, InputObjectTestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac48-132">-Name</span><span class="sxs-lookup"><span data-stu-id="5ac48-132">-Name</span></span>
<span data-ttu-id="5ac48-133">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="5ac48-133">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: TestRouteSet, TestAllRouteSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac48-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ac48-134">-ResourceGroupName</span></span>
<span data-ttu-id="5ac48-135">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="5ac48-135">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: TestRouteSet, TestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac48-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ac48-136">-ResourceId</span></span>
<span data-ttu-id="5ac48-137">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="5ac48-137">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdTestRouteSet, ResourceIdTestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac48-138">-RouteName</span><span class="sxs-lookup"><span data-stu-id="5ac48-138">-RouteName</span></span>
<span data-ttu-id="5ac48-139">경로의 이름</span><span class="sxs-lookup"><span data-stu-id="5ac48-139">Name of the Route</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectTestRouteSet, TestRouteSet, ResourceIdTestRouteSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac48-140">-ShowError</span><span class="sxs-lookup"><span data-stu-id="5ac48-140">-ShowError</span></span>
<span data-ttu-id="5ac48-141">자세한 오류 표시(있는 경우)</span><span class="sxs-lookup"><span data-stu-id="5ac48-141">Show detailed error, if exist</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InputObjectTestRouteSet, TestRouteSet, ResourceIdTestRouteSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac48-142">-Source</span><span class="sxs-lookup"><span data-stu-id="5ac48-142">-Source</span></span>
<span data-ttu-id="5ac48-143">경로의 원본</span><span class="sxs-lookup"><span data-stu-id="5ac48-143">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: InputObjectTestAllRouteSet, TestAllRouteSet, ResourceIdTestAllRouteSet
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac48-144">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="5ac48-144">-SystemProperty</span></span>
<span data-ttu-id="5ac48-145">경로 메시지의 시스템 속성</span><span class="sxs-lookup"><span data-stu-id="5ac48-145">System properties of the route message</span></span>

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

### <span data-ttu-id="5ac48-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ac48-146">CommonParameters</span></span>
<span data-ttu-id="5ac48-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5ac48-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ac48-148">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5ac48-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ac48-149">입력</span><span class="sxs-lookup"><span data-stu-id="5ac48-149">INPUTS</span></span>

### <span data-ttu-id="5ac48-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="5ac48-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5ac48-151">System.String</span><span class="sxs-lookup"><span data-stu-id="5ac48-151">System.String</span></span>

## <span data-ttu-id="5ac48-152">출력</span><span class="sxs-lookup"><span data-stu-id="5ac48-152">OUTPUTS</span></span>

### <span data-ttu-id="5ac48-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="5ac48-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="5ac48-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span><span class="sxs-lookup"><span data-stu-id="5ac48-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="5ac48-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span><span class="sxs-lookup"><span data-stu-id="5ac48-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="5ac48-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5ac48-156">NOTES</span></span>

## <span data-ttu-id="5ac48-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5ac48-157">RELATED LINKS</span></span>
