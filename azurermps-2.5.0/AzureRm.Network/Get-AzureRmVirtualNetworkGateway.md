---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 1700ec112767397653201ff16608afbfb4af8f3e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881437"
---
# <span data-ttu-id="88737-101">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="88737-101">Get-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="88737-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88737-102">SYNOPSIS</span></span>
<span data-ttu-id="88737-103">가상 네트워크 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="88737-103">Gets a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88737-104">구문과</span><span class="sxs-lookup"><span data-stu-id="88737-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88737-105">설명은</span><span class="sxs-lookup"><span data-stu-id="88737-105">DESCRIPTION</span></span>
<span data-ttu-id="88737-106">가상 네트워크 게이트웨이는 Azure에서 게이트웨이를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="88737-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="88737-107">**AzureRmVirtualNetworkGateway** Cmdlet은 이름 및 리소스 그룹 이름에 따라 Azure에서 게이트웨이의 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="88737-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="88737-108">예제의</span><span class="sxs-lookup"><span data-stu-id="88737-108">EXAMPLES</span></span>

### <span data-ttu-id="88737-109">1: 가상 네트워크 게이트웨이 가져오기</span><span class="sxs-lookup"><span data-stu-id="88737-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="88737-110">리소스 그룹 "Mygateway" 내에서 이름이 "myGateway" 인 가상 네트워크 게이트웨이의 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="88737-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="88737-111">변수</span><span class="sxs-lookup"><span data-stu-id="88737-111">PARAMETERS</span></span>

### <span data-ttu-id="88737-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88737-112">-DefaultProfile</span></span>
<span data-ttu-id="88737-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88737-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88737-114">-이름</span><span class="sxs-lookup"><span data-stu-id="88737-114">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88737-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88737-115">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88737-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88737-116">CommonParameters</span></span>
<span data-ttu-id="88737-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="88737-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88737-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88737-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88737-119">입력</span><span class="sxs-lookup"><span data-stu-id="88737-119">INPUTS</span></span>

## <span data-ttu-id="88737-120">출력</span><span class="sxs-lookup"><span data-stu-id="88737-120">OUTPUTS</span></span>

### <span data-ttu-id="88737-121">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="88737-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="88737-122">상속자</span><span class="sxs-lookup"><span data-stu-id="88737-122">NOTES</span></span>

## <span data-ttu-id="88737-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88737-123">RELATED LINKS</span></span>

