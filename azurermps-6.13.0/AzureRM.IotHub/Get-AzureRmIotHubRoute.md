---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoute.md
ms.openlocfilehash: 0711bd1d6290191c2d5311a7375e6f81c4ecd573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711105"
---
# <span data-ttu-id="8fef7-101">Get-AzureRmIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="8fef7-101">Get-AzureRmIotHubRoute</span></span>

## <span data-ttu-id="8fef7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fef7-102">SYNOPSIS</span></span>
<span data-ttu-id="8fef7-103">IoT Hub의 경로에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="8fef7-103">Get information about the route in IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fef7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8fef7-104">SYNTAX</span></span>

### <span data-ttu-id="8fef7-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8fef7-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fef7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8fef7-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fef7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8fef7-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8fef7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8fef7-108">DESCRIPTION</span></span>
<span data-ttu-id="8fef7-109">경로에 대 한 정보를 가져옵니다. IoT Hub에서 모든 경로를 가져오고, 끝점 형식에 대 한 경로를 가져오거나, 특정 끝점에 대 한 경로를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8fef7-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="8fef7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8fef7-110">EXAMPLES</span></span>

### <span data-ttu-id="8fef7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8fef7-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="8fef7-112">"Myiothub" IoT Hub에서 모든 경로를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8fef7-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="8fef7-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="8fef7-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="8fef7-114">"Myiothub" IoT Hub에서 경로 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8fef7-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="8fef7-115">변수</span><span class="sxs-lookup"><span data-stu-id="8fef7-115">PARAMETERS</span></span>

### <span data-ttu-id="8fef7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fef7-116">-DefaultProfile</span></span>
<span data-ttu-id="8fef7-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8fef7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fef7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8fef7-118">-InputObject</span></span>
<span data-ttu-id="8fef7-119">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="8fef7-119">IotHub Object</span></span>

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

### <span data-ttu-id="8fef7-120">-이름</span><span class="sxs-lookup"><span data-stu-id="8fef7-120">-Name</span></span>
<span data-ttu-id="8fef7-121">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="8fef7-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8fef7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fef7-122">-ResourceGroupName</span></span>
<span data-ttu-id="8fef7-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8fef7-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8fef7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fef7-124">-ResourceId</span></span>
<span data-ttu-id="8fef7-125">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="8fef7-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8fef7-126">-RouteName</span><span class="sxs-lookup"><span data-stu-id="8fef7-126">-RouteName</span></span>
<span data-ttu-id="8fef7-127">경로의 이름</span><span class="sxs-lookup"><span data-stu-id="8fef7-127">Name of the Route</span></span>

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

### <span data-ttu-id="8fef7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fef7-128">CommonParameters</span></span>
<span data-ttu-id="8fef7-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fef7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fef7-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fef7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fef7-131">입력</span><span class="sxs-lookup"><span data-stu-id="8fef7-131">INPUTS</span></span>

### <span data-ttu-id="8fef7-132">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="8fef7-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="8fef7-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8fef7-133">System.String</span></span>

## <span data-ttu-id="8fef7-134">출력</span><span class="sxs-lookup"><span data-stu-id="8fef7-134">OUTPUTS</span></span>

### <span data-ttu-id="8fef7-135">IotHub. PSRouteMetadata/. \*</span><span class="sxs-lookup"><span data-stu-id="8fef7-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>
<span data-ttu-id="8fef7-136">System.webserver. List ' 1 [[IotHub]. PSRouteProperties, Microsoft IotHub, Version = 3.1.3.0, Culture = 중립, PublicKeyToken = null]]을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fef7-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8fef7-137">상속자</span><span class="sxs-lookup"><span data-stu-id="8fef7-137">NOTES</span></span>

## <span data-ttu-id="8fef7-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8fef7-138">RELATED LINKS</span></span>
