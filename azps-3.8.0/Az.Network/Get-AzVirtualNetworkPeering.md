---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: 0cc6441d77806c28450d50d5f83a7588da1d1d46
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034841"
---
# <span data-ttu-id="dd073-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="dd073-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="dd073-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd073-102">SYNOPSIS</span></span>
<span data-ttu-id="dd073-103">가상 네트워크 피어 링을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dd073-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="dd073-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dd073-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd073-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dd073-105">DESCRIPTION</span></span>
<span data-ttu-id="dd073-106">**AzVirtualNetworkPeering** cmdlet은 가상 네트워크 피어 링을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dd073-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="dd073-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dd073-107">EXAMPLES</span></span>

### <span data-ttu-id="dd073-108">예제 1: 두 가상 네트워크 간 피어 링 가져오기</span><span class="sxs-lookup"><span data-stu-id="dd073-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

### <span data-ttu-id="dd073-109">예제 2: 가상 네트워크의 모든 peerings 가져오기</span><span class="sxs-lookup"><span data-stu-id="dd073-109">Example 2: Get all peerings in virtual network</span></span>
```
# Get all virtual network peerings located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1To*" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="dd073-110">변수</span><span class="sxs-lookup"><span data-stu-id="dd073-110">PARAMETERS</span></span>

### <span data-ttu-id="dd073-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd073-111">-DefaultProfile</span></span>
<span data-ttu-id="dd073-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dd073-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd073-113">-이름</span><span class="sxs-lookup"><span data-stu-id="dd073-113">-Name</span></span>
<span data-ttu-id="dd073-114">가상 네트워크 피어 링 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd073-114">Specifies the virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="dd073-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd073-115">-ResourceGroupName</span></span>
<span data-ttu-id="dd073-116">가상 네트워크 피어 링이 속한 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd073-116">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="dd073-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="dd073-117">-VirtualNetworkName</span></span>
<span data-ttu-id="dd073-118">이 cmdlet이 가져오는 가상 네트워크 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd073-118">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="dd073-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd073-119">CommonParameters</span></span>
<span data-ttu-id="dd073-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd073-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd073-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dd073-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd073-122">입력</span><span class="sxs-lookup"><span data-stu-id="dd073-122">INPUTS</span></span>

### <span data-ttu-id="dd073-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dd073-123">System.String</span></span>

## <span data-ttu-id="dd073-124">출력</span><span class="sxs-lookup"><span data-stu-id="dd073-124">OUTPUTS</span></span>

### <span data-ttu-id="dd073-125">PSVirtualNetworkPeering에 대 한.</span><span class="sxs-lookup"><span data-stu-id="dd073-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="dd073-126">상속자</span><span class="sxs-lookup"><span data-stu-id="dd073-126">NOTES</span></span>

## <span data-ttu-id="dd073-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dd073-127">RELATED LINKS</span></span>

[<span data-ttu-id="dd073-128">추가-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="dd073-128">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="dd073-129">제거-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="dd073-129">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="dd073-130">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="dd073-130">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
