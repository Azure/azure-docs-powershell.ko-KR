---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 0e8644e55a599ae1cc72d9d04caa4ea4fb7eb5ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532452"
---
# <span data-ttu-id="ea28b-101">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ea28b-101">Get-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="ea28b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea28b-102">SYNOPSIS</span></span>
<span data-ttu-id="ea28b-103">가상 네트워크 게이트웨이 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ea28b-103">Gets a Virtual Network Gateway Connection</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea28b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ea28b-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea28b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ea28b-105">DESCRIPTION</span></span>
<span data-ttu-id="ea28b-106">가상 네트워크 게이트웨이 연결은 Azure의 가상 네트워크 게이트웨이에 연결 된 IPsec 터널 (사이트 간 또는 Vnet to Vnet)을 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ea28b-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="ea28b-107">**AzureRmVirtualNetworkGatewayConnection** Cmdlet은 이름 및 리소스 그룹 이름을 기준으로 연결 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea28b-107">The **Get-AzureRmVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="ea28b-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ea28b-108">EXAMPLES</span></span>

### <span data-ttu-id="ea28b-109">1: 가상 네트워크 게이트웨이 연결 가져오기</span><span class="sxs-lookup"><span data-stu-id="ea28b-109">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzureRmVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="ea28b-110">리소스 그룹 "Mytunnel" 내에서 이름이 "myTunnel" 인 가상 네트워크 게이트웨이 연결의 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea28b-110">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="ea28b-111">변수</span><span class="sxs-lookup"><span data-stu-id="ea28b-111">PARAMETERS</span></span>

### <span data-ttu-id="ea28b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea28b-112">-DefaultProfile</span></span>
<span data-ttu-id="ea28b-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ea28b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea28b-114">-이름</span><span class="sxs-lookup"><span data-stu-id="ea28b-114">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea28b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea28b-115">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea28b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea28b-116">CommonParameters</span></span>
<span data-ttu-id="ea28b-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea28b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea28b-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea28b-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea28b-119">입력</span><span class="sxs-lookup"><span data-stu-id="ea28b-119">INPUTS</span></span>

### <span data-ttu-id="ea28b-120">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ea28b-120">System.String</span></span>

## <span data-ttu-id="ea28b-121">출력</span><span class="sxs-lookup"><span data-stu-id="ea28b-121">OUTPUTS</span></span>

### <span data-ttu-id="ea28b-122">PSVirtualNetworkGatewayConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ea28b-122">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="ea28b-123">상속자</span><span class="sxs-lookup"><span data-stu-id="ea28b-123">NOTES</span></span>

## <span data-ttu-id="ea28b-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea28b-124">RELATED LINKS</span></span>
