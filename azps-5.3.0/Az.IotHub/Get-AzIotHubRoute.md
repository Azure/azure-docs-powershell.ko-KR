---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
ms.openlocfilehash: 6e72a889264efa82af343a0aab019cc3e5580dc7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495454"
---
# <span data-ttu-id="e121c-101">Get-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="e121c-101">Get-AzIotHubRoute</span></span>

## <span data-ttu-id="e121c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e121c-102">SYNOPSIS</span></span>
<span data-ttu-id="e121c-103">IoT Hub에서 경로에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="e121c-103">Get information about the route in IoT Hub</span></span>

## <span data-ttu-id="e121c-104">구문</span><span class="sxs-lookup"><span data-stu-id="e121c-104">SYNTAX</span></span>

### <span data-ttu-id="e121c-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e121c-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e121c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e121c-106">InputObjectSet</span></span>
```
Get-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e121c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e121c-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e121c-108">설명</span><span class="sxs-lookup"><span data-stu-id="e121c-108">DESCRIPTION</span></span>
<span data-ttu-id="e121c-109">경로에 대한 정보를 얻습니다. IoT Hub에서 모든 경로를 얻거나, 엔드포인트 유형에 대한 경로를 얻거나, 특정 엔드포인트에 대한 경로를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e121c-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="e121c-110">예제</span><span class="sxs-lookup"><span data-stu-id="e121c-110">EXAMPLES</span></span>

### <span data-ttu-id="e121c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e121c-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="e121c-112">"myiothub" IoT Hub에서 모든 경로를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e121c-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="e121c-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="e121c-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="e121c-114">"myiothub" IoT Hub에서 경로 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e121c-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="e121c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e121c-115">PARAMETERS</span></span>

### <span data-ttu-id="e121c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e121c-116">-DefaultProfile</span></span>
<span data-ttu-id="e121c-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e121c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e121c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e121c-118">-InputObject</span></span>
<span data-ttu-id="e121c-119">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="e121c-119">IotHub Object</span></span>

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

### <span data-ttu-id="e121c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e121c-120">-Name</span></span>
<span data-ttu-id="e121c-121">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="e121c-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e121c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e121c-122">-ResourceGroupName</span></span>
<span data-ttu-id="e121c-123">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="e121c-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e121c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e121c-124">-ResourceId</span></span>
<span data-ttu-id="e121c-125">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="e121c-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e121c-126">-RouteName</span><span class="sxs-lookup"><span data-stu-id="e121c-126">-RouteName</span></span>
<span data-ttu-id="e121c-127">경로의 이름</span><span class="sxs-lookup"><span data-stu-id="e121c-127">Name of the Route</span></span>

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

### <span data-ttu-id="e121c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e121c-128">CommonParameters</span></span>
<span data-ttu-id="e121c-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e121c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e121c-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e121c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e121c-131">입력</span><span class="sxs-lookup"><span data-stu-id="e121c-131">INPUTS</span></span>

### <span data-ttu-id="e121c-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e121c-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e121c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e121c-133">System.String</span></span>

## <span data-ttu-id="e121c-134">출력</span><span class="sxs-lookup"><span data-stu-id="e121c-134">OUTPUTS</span></span>

### <span data-ttu-id="e121c-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="e121c-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

### <span data-ttu-id="e121c-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span><span class="sxs-lookup"><span data-stu-id="e121c-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="e121c-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e121c-137">NOTES</span></span>

## <span data-ttu-id="e121c-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e121c-138">RELATED LINKS</span></span>
