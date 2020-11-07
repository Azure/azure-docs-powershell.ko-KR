---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkpeering
schema: 2.0.0
ms.openlocfilehash: b5e3cf083f003a643639635c61ca8e3f13e16eaf
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881410"
---
# <span data-ttu-id="24fe4-101">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="24fe4-101">Get-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="24fe4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24fe4-102">SYNOPSIS</span></span>
<span data-ttu-id="24fe4-103">가상 네트워크 피어 링을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24fe4-103">Gets the virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24fe4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24fe4-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24fe4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="24fe4-105">DESCRIPTION</span></span>
<span data-ttu-id="24fe4-106">**AzureRmVirtualNetworkPeering** cmdlet은 가상 네트워크 피어 링을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24fe4-106">The **Get-AzureRmVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="24fe4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="24fe4-107">EXAMPLES</span></span>

### <span data-ttu-id="24fe4-108">예제 1: 두 가상 네트워크 간 피어 링 가져오기</span><span class="sxs-lookup"><span data-stu-id="24fe4-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="24fe4-109">변수</span><span class="sxs-lookup"><span data-stu-id="24fe4-109">PARAMETERS</span></span>

### <span data-ttu-id="24fe4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24fe4-110">-DefaultProfile</span></span>
<span data-ttu-id="24fe4-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24fe4-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24fe4-112">-이름</span><span class="sxs-lookup"><span data-stu-id="24fe4-112">-Name</span></span>
<span data-ttu-id="24fe4-113">가상 네트워크 피어 링 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24fe4-113">Specifies the virtual network peering name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24fe4-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24fe4-114">-ResourceGroupName</span></span>
<span data-ttu-id="24fe4-115">가상 네트워크 피어 링이 속한 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24fe4-115">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="24fe4-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="24fe4-116">-VirtualNetworkName</span></span>
<span data-ttu-id="24fe4-117">이 cmdlet이 가져오는 가상 네트워크 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24fe4-117">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="24fe4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24fe4-118">CommonParameters</span></span>
<span data-ttu-id="24fe4-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24fe4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24fe4-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24fe4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24fe4-121">입력</span><span class="sxs-lookup"><span data-stu-id="24fe4-121">INPUTS</span></span>

## <span data-ttu-id="24fe4-122">출력</span><span class="sxs-lookup"><span data-stu-id="24fe4-122">OUTPUTS</span></span>

### <span data-ttu-id="24fe4-123">PSVirtualNetworkPeering에 대 한.</span><span class="sxs-lookup"><span data-stu-id="24fe4-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="24fe4-124">상속자</span><span class="sxs-lookup"><span data-stu-id="24fe4-124">NOTES</span></span>

## <span data-ttu-id="24fe4-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24fe4-125">RELATED LINKS</span></span>

[<span data-ttu-id="24fe4-126">추가-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="24fe4-126">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="24fe4-127">제거-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="24fe4-127">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="24fe4-128">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="24fe4-128">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)


