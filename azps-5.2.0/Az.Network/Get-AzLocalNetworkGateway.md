---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 14c0ec31f10a6405fb2a3f412f004d53dbdeb9a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356133"
---
# <span data-ttu-id="8acf7-101">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8acf7-101">Get-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="8acf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8acf7-102">SYNOPSIS</span></span>
<span data-ttu-id="8acf7-103">로컬 네트워크 게이트웨이를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8acf7-103">Gets a Local Network Gateway</span></span>

## <span data-ttu-id="8acf7-104">구문</span><span class="sxs-lookup"><span data-stu-id="8acf7-104">SYNTAX</span></span>

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8acf7-105">설명</span><span class="sxs-lookup"><span data-stu-id="8acf7-105">DESCRIPTION</span></span>
<span data-ttu-id="8acf7-106">로컬 네트워크 게이트웨이는 VPN 디바이스 On-프레미스를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8acf7-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="8acf7-107">**Get-AzLocalNetworkGateway** cmdlet은 이름 및 리소스 그룹 이름에 따라 프레미스 게이트웨이를 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8acf7-107">The **Get-AzLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="8acf7-108">예제</span><span class="sxs-lookup"><span data-stu-id="8acf7-108">EXAMPLES</span></span>

### <span data-ttu-id="8acf7-109">예제 1: 로컬 네트워크 게이트웨이를 얻게</span><span class="sxs-lookup"><span data-stu-id="8acf7-109">Example 1: Get a Local Network Gateway</span></span>
```powershell
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

<span data-ttu-id="8acf7-110">리소스 그룹 "myRG" 내에서 이름이 "myLocalGW1"인 로컬 네트워크 게이트웨이의 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8acf7-110">Returns the object of the Local Network Gateway with the name "myLocalGW1" within the resource group "myRG"</span></span>

### <span data-ttu-id="8acf7-111">예제 2: 필터링을 사용하여 로컬 네트워크 게이트웨이를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8acf7-111">Example 2: Get Local Network Gateways using filtering</span></span>
```powershell
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

<span data-ttu-id="8acf7-112">리소스 그룹 "myRG"에서 "myLocalGW"로 시작하는 이름으로 로컬 네트워크 게이트웨이의 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8acf7-112">Returns the object of the Local Network Gateway with name starting with "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="8acf7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8acf7-113">PARAMETERS</span></span>

### <span data-ttu-id="8acf7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8acf7-114">-DefaultProfile</span></span>
<span data-ttu-id="8acf7-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8acf7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8acf7-116">-Name</span><span class="sxs-lookup"><span data-stu-id="8acf7-116">-Name</span></span>
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

### <span data-ttu-id="8acf7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8acf7-117">-ResourceGroupName</span></span>
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

### <span data-ttu-id="8acf7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8acf7-118">CommonParameters</span></span>
<span data-ttu-id="8acf7-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8acf7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8acf7-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8acf7-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8acf7-121">입력</span><span class="sxs-lookup"><span data-stu-id="8acf7-121">INPUTS</span></span>

### <span data-ttu-id="8acf7-122">System.String</span><span class="sxs-lookup"><span data-stu-id="8acf7-122">System.String</span></span>

## <span data-ttu-id="8acf7-123">출력</span><span class="sxs-lookup"><span data-stu-id="8acf7-123">OUTPUTS</span></span>

### <span data-ttu-id="8acf7-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8acf7-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="8acf7-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8acf7-125">NOTES</span></span>

## <span data-ttu-id="8acf7-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8acf7-126">RELATED LINKS</span></span>

[<span data-ttu-id="8acf7-127">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8acf7-127">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="8acf7-128">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8acf7-128">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="8acf7-129">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8acf7-129">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
