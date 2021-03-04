---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: 892d160decb7bc595e25f2f0512996fe2bdce5da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954096"
---
# <span data-ttu-id="7b2d1-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="7b2d1-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="7b2d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b2d1-102">SYNOPSIS</span></span>
<span data-ttu-id="7b2d1-103">경로 테이블에서 경로를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7b2d1-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="7b2d1-104">구문</span><span class="sxs-lookup"><span data-stu-id="7b2d1-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b2d1-105">설명</span><span class="sxs-lookup"><span data-stu-id="7b2d1-105">DESCRIPTION</span></span>
<span data-ttu-id="7b2d1-106">**Get-AzRouteConfig** cmdlet은 Azure 경로 테이블에서 경로를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7b2d1-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="7b2d1-107">이름을 통해 경로를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b2d1-107">You can specify a route by name.</span></span>

## <span data-ttu-id="7b2d1-108">예제</span><span class="sxs-lookup"><span data-stu-id="7b2d1-108">EXAMPLES</span></span>

### <span data-ttu-id="7b2d1-109">예제 1: 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7b2d1-109">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="7b2d1-110">이 명령은 **Get-AzRouteTable** cmdlet을 사용하여 RouteTable01이라는 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7b2d1-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="7b2d1-111">명령은 파이프라인 연산자를 사용하여 현재 cmdlet에 테이블을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="7b2d1-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7b2d1-112">현재 cmdlet은 RouteTable01이라는 경로 테이블에서 Route07이라는 경로를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7b2d1-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="7b2d1-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7b2d1-113">PARAMETERS</span></span>

### <span data-ttu-id="7b2d1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b2d1-114">-DefaultProfile</span></span>
<span data-ttu-id="7b2d1-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7b2d1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b2d1-116">-Name</span><span class="sxs-lookup"><span data-stu-id="7b2d1-116">-Name</span></span>
<span data-ttu-id="7b2d1-117">이 cmdlet이 도착하는 경로의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b2d1-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7b2d1-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="7b2d1-118">-RouteTable</span></span>
<span data-ttu-id="7b2d1-119">이 cmdlet에서 경로를 얻을 경로 테이블을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b2d1-119">Specifies the route table from which this cmdlet gets routes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b2d1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b2d1-120">CommonParameters</span></span>
<span data-ttu-id="7b2d1-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7b2d1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b2d1-122">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7b2d1-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b2d1-123">입력</span><span class="sxs-lookup"><span data-stu-id="7b2d1-123">INPUTS</span></span>

### <span data-ttu-id="7b2d1-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="7b2d1-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="7b2d1-125">출력</span><span class="sxs-lookup"><span data-stu-id="7b2d1-125">OUTPUTS</span></span>

### <span data-ttu-id="7b2d1-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span><span class="sxs-lookup"><span data-stu-id="7b2d1-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="7b2d1-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7b2d1-127">NOTES</span></span>

## <span data-ttu-id="7b2d1-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b2d1-128">RELATED LINKS</span></span>

[<span data-ttu-id="7b2d1-129">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="7b2d1-129">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="7b2d1-130">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="7b2d1-130">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="7b2d1-131">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="7b2d1-131">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="7b2d1-132">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="7b2d1-132">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="7b2d1-133">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="7b2d1-133">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


