---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: d3695216cdbda51ae3583218f7d0993894f472eb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495542"
---
# <span data-ttu-id="08261-101">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="08261-101">Get-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="08261-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08261-102">SYNOPSIS</span></span>
<span data-ttu-id="08261-103">Virtual Network 게이트웨이 연결을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="08261-103">Gets a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="08261-104">구문</span><span class="sxs-lookup"><span data-stu-id="08261-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08261-105">설명</span><span class="sxs-lookup"><span data-stu-id="08261-105">DESCRIPTION</span></span>
<span data-ttu-id="08261-106">Virtual Network 게이트웨이 연결은 Azure의 Virtual Network Gateway에 연결된 IPsec 터널(사이트-사이트 또는 Vnet-Vnet)을 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="08261-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="08261-107">**Get-AzVirtualNetworkGatewayConnection** cmdlet은 이름 및 리소스 그룹 이름에 따라 연결의 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="08261-107">The **Get-AzVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>
<span data-ttu-id="08261-108">-Name 매개 변수를 지정하지 않고 **Get-AzVirtualNetworkGatewayConnection** cmdlet을 발급하면 출력에 ConnectionStatus 및 SharedKey 세부 정보가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="08261-108">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show ConnectionStatus and SharedKey details.</span></span>

## <span data-ttu-id="08261-109">예제</span><span class="sxs-lookup"><span data-stu-id="08261-109">EXAMPLES</span></span>

### <span data-ttu-id="08261-110">1: Virtual Network 게이트웨이 연결 얻기</span><span class="sxs-lookup"><span data-stu-id="08261-110">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="08261-111">리소스 그룹 "myRG" 내에서 이름이 "myTunnel"인 Virtual Network 게이트웨이 연결의 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="08261-111">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

### <span data-ttu-id="08261-112">2: 필터링을 사용하여 모든 Virtual Network 게이트웨이 연결 얻기</span><span class="sxs-lookup"><span data-stu-id="08261-112">2: Get all Virtual Network Gateway Connections using filtering</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel* -ResourceGroupName myRG
```

<span data-ttu-id="08261-113">리소스 그룹 "myRG" 내에서 "myTunnel"로 시작하는 모든 Virtual Network 게이트웨이 연결을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="08261-113">Returns all Virtual Network Gateway Connections that start with "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="08261-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08261-114">PARAMETERS</span></span>

### <span data-ttu-id="08261-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08261-115">-DefaultProfile</span></span>
<span data-ttu-id="08261-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="08261-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08261-117">-Name</span><span class="sxs-lookup"><span data-stu-id="08261-117">-Name</span></span>
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

### <span data-ttu-id="08261-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08261-118">-ResourceGroupName</span></span>
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

### <span data-ttu-id="08261-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08261-119">CommonParameters</span></span>
<span data-ttu-id="08261-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="08261-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08261-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="08261-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08261-122">입력</span><span class="sxs-lookup"><span data-stu-id="08261-122">INPUTS</span></span>

### <span data-ttu-id="08261-123">System.String</span><span class="sxs-lookup"><span data-stu-id="08261-123">System.String</span></span>

## <span data-ttu-id="08261-124">출력</span><span class="sxs-lookup"><span data-stu-id="08261-124">OUTPUTS</span></span>

### <span data-ttu-id="08261-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="08261-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="08261-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="08261-126">NOTES</span></span>

## <span data-ttu-id="08261-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="08261-127">RELATED LINKS</span></span>

[<span data-ttu-id="08261-128">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="08261-128">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="08261-129">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="08261-129">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="08261-130">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="08261-130">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
