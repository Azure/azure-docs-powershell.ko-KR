---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServer.md
ms.openlocfilehash: ef5609a34104ca8502b8e4ce96fe294a4714366d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954064"
---
# <span data-ttu-id="0d8bf-101">Get-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="0d8bf-101">Get-AzRouteServer</span></span>

## <span data-ttu-id="0d8bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d8bf-102">SYNOPSIS</span></span>
<span data-ttu-id="0d8bf-103">Azure RouteServer를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="0d8bf-103">Get an Azure RouteServer</span></span>

## <span data-ttu-id="0d8bf-104">구문</span><span class="sxs-lookup"><span data-stu-id="0d8bf-104">SYNTAX</span></span>

### <span data-ttu-id="0d8bf-105">RouteServerSubscriptionIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0d8bf-105">RouteServerSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzRouteServer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d8bf-106">RouteServerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d8bf-106">RouteServerNameParameterSet</span></span>
```
Get-AzRouteServer -ResourceGroupName <String> [-RouteServerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d8bf-107">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d8bf-107">RouteServerResourceIdParameterSet</span></span>
```
Get-AzRouteServer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d8bf-108">설명</span><span class="sxs-lookup"><span data-stu-id="0d8bf-108">DESCRIPTION</span></span>
<span data-ttu-id="0d8bf-109">**Get-AzRouteServer** cmdlet은 Azure RouteServer를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0d8bf-109">The **Get-AzRouteServer** cmdlet gets an Azure RouteServer</span></span>

## <span data-ttu-id="0d8bf-110">예제</span><span class="sxs-lookup"><span data-stu-id="0d8bf-110">EXAMPLES</span></span>

### <span data-ttu-id="0d8bf-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="0d8bf-111">Example 1</span></span>
```powershell
Get-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
```

### <span data-ttu-id="0d8bf-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="0d8bf-112">Example 2</span></span>
```powershell
$routeServerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer'
Get-AzRouteServer -ResourceId $routeServerId
```
## <span data-ttu-id="0d8bf-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0d8bf-113">PARAMETERS</span></span>

### <span data-ttu-id="0d8bf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d8bf-114">-DefaultProfile</span></span>
<span data-ttu-id="0d8bf-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0d8bf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d8bf-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d8bf-116">-ResourceGroupName</span></span>
<span data-ttu-id="0d8bf-117">경로 서버의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0d8bf-117">The resource group name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d8bf-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d8bf-118">-ResourceId</span></span>
<span data-ttu-id="0d8bf-119">경로 서버의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="0d8bf-119">ResourceId of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d8bf-120">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="0d8bf-120">-RouteServerName</span></span>
<span data-ttu-id="0d8bf-121">경로 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0d8bf-121">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d8bf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d8bf-122">CommonParameters</span></span>
<span data-ttu-id="0d8bf-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0d8bf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d8bf-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d8bf-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d8bf-125">입력</span><span class="sxs-lookup"><span data-stu-id="0d8bf-125">INPUTS</span></span>

### <span data-ttu-id="0d8bf-126">System.String</span><span class="sxs-lookup"><span data-stu-id="0d8bf-126">System.String</span></span>

## <span data-ttu-id="0d8bf-127">출력</span><span class="sxs-lookup"><span data-stu-id="0d8bf-127">OUTPUTS</span></span>

### <span data-ttu-id="0d8bf-128">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="0d8bf-128">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="0d8bf-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0d8bf-129">NOTES</span></span>

## <span data-ttu-id="0d8bf-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d8bf-130">RELATED LINKS</span></span>
