---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 83289067bef9cf294477dca60a8b26a9b61dcb41
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878202"
---
# <span data-ttu-id="06f1e-101">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="06f1e-101">Get-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="06f1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06f1e-102">SYNOPSIS</span></span>
<span data-ttu-id="06f1e-103">로컬 네트워크 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06f1e-103">Gets a Local Network Gateway</span></span>

## <span data-ttu-id="06f1e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="06f1e-104">SYNTAX</span></span>

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06f1e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="06f1e-105">DESCRIPTION</span></span>
<span data-ttu-id="06f1e-106">로컬 네트워크 게이트웨이는 온-프레미스의 VPN 장치를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="06f1e-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="06f1e-107">**AzLocalNetworkGateway** Cmdlet은 이름 및 리소스 그룹 이름을 기준으로 온-프레미스 gateway를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="06f1e-107">The **Get-AzLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="06f1e-108">예제의</span><span class="sxs-lookup"><span data-stu-id="06f1e-108">EXAMPLES</span></span>

### <span data-ttu-id="06f1e-109">1: 로컬 네트워크 게이트웨이 가져오기</span><span class="sxs-lookup"><span data-stu-id="06f1e-109">1: Get a Local Network Gateway</span></span>
```
Get-AzLocalNetworkGateway -Name myLocalGW1 -ResourceGroupName myRG

Name                     : myLocalGW1
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

<span data-ttu-id="06f1e-110">리소스 그룹 "myRG" 내에서 이름이 "myLocalGW1" 인 로컬 네트워크 게이트웨이의 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="06f1e-110">Returns the object of the Local Network Gateway with the name "myLocalGW1" within the resource group "myRG"</span></span>

### <span data-ttu-id="06f1e-111">2: 필터링을 사용 하 여 로컬 네트워크 게이트웨이 가져오기</span><span class="sxs-lookup"><span data-stu-id="06f1e-111">2: Get Local Network Gateways using filtering</span></span>
```
Get-AzLocalNetworkGateway -Name myLocalGW* -ResourceGroupName myRG

Name                     : myLocalGW1
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null

Name                     : myLocalGW2
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW2
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

<span data-ttu-id="06f1e-112">리소스 그룹 "myRG" 내에서 "myLocalGW"로 시작 하는 이름의 로컬 네트워크 게이트웨이 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="06f1e-112">Returns the object of the Local Network Gateway with name starting with "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="06f1e-113">변수</span><span class="sxs-lookup"><span data-stu-id="06f1e-113">PARAMETERS</span></span>

### <span data-ttu-id="06f1e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06f1e-114">-DefaultProfile</span></span>
<span data-ttu-id="06f1e-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="06f1e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06f1e-116">-이름</span><span class="sxs-lookup"><span data-stu-id="06f1e-116">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="06f1e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06f1e-117">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="06f1e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06f1e-118">CommonParameters</span></span>
<span data-ttu-id="06f1e-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="06f1e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06f1e-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="06f1e-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06f1e-121">입력</span><span class="sxs-lookup"><span data-stu-id="06f1e-121">INPUTS</span></span>

### <span data-ttu-id="06f1e-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="06f1e-122">System.String</span></span>

## <span data-ttu-id="06f1e-123">출력</span><span class="sxs-lookup"><span data-stu-id="06f1e-123">OUTPUTS</span></span>

### <span data-ttu-id="06f1e-124">Microsoft. 네트워크. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="06f1e-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="06f1e-125">상속자</span><span class="sxs-lookup"><span data-stu-id="06f1e-125">NOTES</span></span>

## <span data-ttu-id="06f1e-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06f1e-126">RELATED LINKS</span></span>

[<span data-ttu-id="06f1e-127">새로운 AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="06f1e-127">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="06f1e-128">제거-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="06f1e-128">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="06f1e-129">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="06f1e-129">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
