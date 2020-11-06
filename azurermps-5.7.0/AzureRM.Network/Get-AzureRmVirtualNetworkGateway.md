---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 29d5ad86d9df7bddec8be600d8b7c680c7bcd7fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528055"
---
# <span data-ttu-id="b5a69-101">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b5a69-101">Get-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="b5a69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5a69-102">SYNOPSIS</span></span>
<span data-ttu-id="b5a69-103">가상 네트워크 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b5a69-103">Gets a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5a69-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b5a69-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5a69-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b5a69-105">DESCRIPTION</span></span>
<span data-ttu-id="b5a69-106">가상 네트워크 게이트웨이는 Azure에서 게이트웨이를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b5a69-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="b5a69-107">**AzureRmVirtualNetworkGateway** Cmdlet은 이름 및 리소스 그룹 이름에 따라 Azure에서 게이트웨이의 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5a69-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="b5a69-108">예제의</span><span class="sxs-lookup"><span data-stu-id="b5a69-108">EXAMPLES</span></span>

### <span data-ttu-id="b5a69-109">1: 가상 네트워크 게이트웨이 가져오기</span><span class="sxs-lookup"><span data-stu-id="b5a69-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="b5a69-110">리소스 그룹 "Mygateway" 내에서 이름이 "myGateway" 인 가상 네트워크 게이트웨이의 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5a69-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="b5a69-111">변수</span><span class="sxs-lookup"><span data-stu-id="b5a69-111">PARAMETERS</span></span>

### <span data-ttu-id="b5a69-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5a69-112">-DefaultProfile</span></span>
<span data-ttu-id="b5a69-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b5a69-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5a69-114">-이름</span><span class="sxs-lookup"><span data-stu-id="b5a69-114">-Name</span></span>
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

### <span data-ttu-id="b5a69-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5a69-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="b5a69-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5a69-116">CommonParameters</span></span>
<span data-ttu-id="b5a69-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5a69-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5a69-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5a69-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5a69-119">입력</span><span class="sxs-lookup"><span data-stu-id="b5a69-119">INPUTS</span></span>

### <span data-ttu-id="b5a69-120">않아야</span><span class="sxs-lookup"><span data-stu-id="b5a69-120">None</span></span>
<span data-ttu-id="b5a69-121">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b5a69-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b5a69-122">출력</span><span class="sxs-lookup"><span data-stu-id="b5a69-122">OUTPUTS</span></span>

### <span data-ttu-id="b5a69-123">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b5a69-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="b5a69-124">상속자</span><span class="sxs-lookup"><span data-stu-id="b5a69-124">NOTES</span></span>

## <span data-ttu-id="b5a69-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b5a69-125">RELATED LINKS</span></span>

