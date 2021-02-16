---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: 0d941289f0798854a3647bcb5fbf4d1e6be1053d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203066"
---
# <span data-ttu-id="e9c5f-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e9c5f-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="e9c5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9c5f-102">SYNOPSIS</span></span>
<span data-ttu-id="e9c5f-103">경로 테이블에서 경로를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e9c5f-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="e9c5f-104">구문</span><span class="sxs-lookup"><span data-stu-id="e9c5f-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9c5f-105">설명</span><span class="sxs-lookup"><span data-stu-id="e9c5f-105">DESCRIPTION</span></span>
<span data-ttu-id="e9c5f-106">**Get-AzRouteConfig** cmdlet은 Azure 경로 테이블에서 경로를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e9c5f-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="e9c5f-107">이름으로 경로를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9c5f-107">You can specify a route by name.</span></span>

## <span data-ttu-id="e9c5f-108">예제</span><span class="sxs-lookup"><span data-stu-id="e9c5f-108">EXAMPLES</span></span>

### <span data-ttu-id="e9c5f-109">예제 1: 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e9c5f-109">Example 1: Get a route table</span></span>
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

<span data-ttu-id="e9c5f-110">이 명령은 **Get-AzRouteTable** cmdlet을 사용하여 RouteTable01이라는 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e9c5f-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="e9c5f-111">이 명령은 파이프라인 연산자를 사용하여 테이블을 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="e9c5f-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e9c5f-112">현재 cmdlet은 RouteTable01이라는 경로 테이블에서 Route07이라는 경로를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e9c5f-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="e9c5f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9c5f-113">PARAMETERS</span></span>

### <span data-ttu-id="e9c5f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9c5f-114">-DefaultProfile</span></span>
<span data-ttu-id="e9c5f-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e9c5f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9c5f-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e9c5f-116">-Name</span></span>
<span data-ttu-id="e9c5f-117">이 cmdlet이 얻을 경로의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e9c5f-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e9c5f-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="e9c5f-118">-RouteTable</span></span>
<span data-ttu-id="e9c5f-119">이 cmdlet이 경로를 얻을 경로 테이블을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e9c5f-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="e9c5f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9c5f-120">CommonParameters</span></span>
<span data-ttu-id="e9c5f-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e9c5f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9c5f-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e9c5f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9c5f-123">입력</span><span class="sxs-lookup"><span data-stu-id="e9c5f-123">INPUTS</span></span>

### <span data-ttu-id="e9c5f-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="e9c5f-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="e9c5f-125">출력</span><span class="sxs-lookup"><span data-stu-id="e9c5f-125">OUTPUTS</span></span>

### <span data-ttu-id="e9c5f-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span><span class="sxs-lookup"><span data-stu-id="e9c5f-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="e9c5f-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e9c5f-127">NOTES</span></span>

## <span data-ttu-id="e9c5f-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9c5f-128">RELATED LINKS</span></span>

[<span data-ttu-id="e9c5f-129">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e9c5f-129">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="e9c5f-130">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="e9c5f-130">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="e9c5f-131">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e9c5f-131">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="e9c5f-132">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e9c5f-132">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="e9c5f-133">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e9c5f-133">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


