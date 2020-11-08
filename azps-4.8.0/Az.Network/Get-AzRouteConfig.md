---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: 0d941289f0798854a3647bcb5fbf4d1e6be1053d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204004"
---
# <span data-ttu-id="0d5cb-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0d5cb-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="0d5cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d5cb-102">SYNOPSIS</span></span>
<span data-ttu-id="0d5cb-103">경로 테이블에서 경로를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d5cb-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="0d5cb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0d5cb-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d5cb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0d5cb-105">DESCRIPTION</span></span>
<span data-ttu-id="0d5cb-106">**AzRouteConfig** Cmdlet은 Azure 경로 테이블에서 경로를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d5cb-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="0d5cb-107">이름을 기준으로 경로를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d5cb-107">You can specify a route by name.</span></span>

## <span data-ttu-id="0d5cb-108">예제의</span><span class="sxs-lookup"><span data-stu-id="0d5cb-108">EXAMPLES</span></span>

### <span data-ttu-id="0d5cb-109">예제 1: 경로 테이블 가져오기</span><span class="sxs-lookup"><span data-stu-id="0d5cb-109">Example 1: Get a route table</span></span>
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

<span data-ttu-id="0d5cb-110">이 명령은 **AzRouteTable** cmdlet을 사용 하 여 RouteTable01 이라는 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d5cb-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="0d5cb-111">이 명령은 파이프라인 연산자를 사용 하 여 해당 테이블을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d5cb-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0d5cb-112">현재 cmdlet는 RouteTable01 이라는 경로 테이블에서 Route07 이라는 경로를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d5cb-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="0d5cb-113">변수</span><span class="sxs-lookup"><span data-stu-id="0d5cb-113">PARAMETERS</span></span>

### <span data-ttu-id="0d5cb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d5cb-114">-DefaultProfile</span></span>
<span data-ttu-id="0d5cb-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0d5cb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d5cb-116">-이름</span><span class="sxs-lookup"><span data-stu-id="0d5cb-116">-Name</span></span>
<span data-ttu-id="0d5cb-117">이 cmdlet이 가져오는 경로의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d5cb-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0d5cb-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="0d5cb-118">-RouteTable</span></span>
<span data-ttu-id="0d5cb-119">이 cmdlet이 경로를 가져오는 경로 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d5cb-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="0d5cb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d5cb-120">CommonParameters</span></span>
<span data-ttu-id="0d5cb-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d5cb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d5cb-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0d5cb-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d5cb-123">입력</span><span class="sxs-lookup"><span data-stu-id="0d5cb-123">INPUTS</span></span>

### <span data-ttu-id="0d5cb-124">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="0d5cb-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="0d5cb-125">출력</span><span class="sxs-lookup"><span data-stu-id="0d5cb-125">OUTPUTS</span></span>

### <span data-ttu-id="0d5cb-126">Microsoft. 네트워크 모델. PSRoute</span><span class="sxs-lookup"><span data-stu-id="0d5cb-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="0d5cb-127">상속자</span><span class="sxs-lookup"><span data-stu-id="0d5cb-127">NOTES</span></span>

## <span data-ttu-id="0d5cb-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d5cb-128">RELATED LINKS</span></span>

[<span data-ttu-id="0d5cb-129">추가-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0d5cb-129">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="0d5cb-130">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="0d5cb-130">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="0d5cb-131">새로운 AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0d5cb-131">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="0d5cb-132">제거-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0d5cb-132">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="0d5cb-133">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0d5cb-133">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


