---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: af925c1de08a5a615f5435bb20377582fedc0089
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537972"
---
# <span data-ttu-id="9e6d2-101">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e6d2-101">Get-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="9e6d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e6d2-102">SYNOPSIS</span></span>
<span data-ttu-id="9e6d2-103">가상 네트워크 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9e6d2-103">Gets a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e6d2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9e6d2-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e6d2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9e6d2-105">DESCRIPTION</span></span>
<span data-ttu-id="9e6d2-106">가상 네트워크 게이트웨이는 Azure에서 게이트웨이를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9e6d2-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="9e6d2-107">**AzureRmVirtualNetworkGateway** Cmdlet은 이름 및 리소스 그룹 이름에 따라 Azure에서 게이트웨이의 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e6d2-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="9e6d2-108">예제의</span><span class="sxs-lookup"><span data-stu-id="9e6d2-108">EXAMPLES</span></span>

### <span data-ttu-id="9e6d2-109">1: 가상 네트워크 게이트웨이 가져오기</span><span class="sxs-lookup"><span data-stu-id="9e6d2-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="9e6d2-110">리소스 그룹 "Mygateway" 내에서 이름이 "myGateway" 인 가상 네트워크 게이트웨이의 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e6d2-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="9e6d2-111">변수</span><span class="sxs-lookup"><span data-stu-id="9e6d2-111">PARAMETERS</span></span>

### <span data-ttu-id="9e6d2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e6d2-112">-DefaultProfile</span></span>
<span data-ttu-id="9e6d2-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9e6d2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e6d2-114">-이름</span><span class="sxs-lookup"><span data-stu-id="9e6d2-114">-Name</span></span>
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

### <span data-ttu-id="9e6d2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e6d2-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="9e6d2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e6d2-116">CommonParameters</span></span>
<span data-ttu-id="9e6d2-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e6d2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e6d2-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e6d2-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e6d2-119">입력</span><span class="sxs-lookup"><span data-stu-id="9e6d2-119">INPUTS</span></span>

### <span data-ttu-id="9e6d2-120">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9e6d2-120">System.String</span></span>

## <span data-ttu-id="9e6d2-121">출력</span><span class="sxs-lookup"><span data-stu-id="9e6d2-121">OUTPUTS</span></span>

### <span data-ttu-id="9e6d2-122">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9e6d2-122">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="9e6d2-123">상속자</span><span class="sxs-lookup"><span data-stu-id="9e6d2-123">NOTES</span></span>

## <span data-ttu-id="9e6d2-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e6d2-124">RELATED LINKS</span></span>
