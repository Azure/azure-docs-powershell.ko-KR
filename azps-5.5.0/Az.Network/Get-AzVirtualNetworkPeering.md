---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: 0cc6441d77806c28450d50d5f83a7588da1d1d46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193705"
---
# <span data-ttu-id="b1620-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b1620-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="b1620-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1620-102">SYNOPSIS</span></span>
<span data-ttu-id="b1620-103">가상 네트워크 피어링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b1620-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="b1620-104">구문</span><span class="sxs-lookup"><span data-stu-id="b1620-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1620-105">설명</span><span class="sxs-lookup"><span data-stu-id="b1620-105">DESCRIPTION</span></span>
<span data-ttu-id="b1620-106">**Get-AzVirtualNetworkPeering** cmdlet은 가상 네트워크 피어링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b1620-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="b1620-107">예제</span><span class="sxs-lookup"><span data-stu-id="b1620-107">EXAMPLES</span></span>

### <span data-ttu-id="b1620-108">예제 1: 두 가상 네트워크 간의 피어링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b1620-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

### <span data-ttu-id="b1620-109">예제 2: 가상 네트워크의 모든 피어링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b1620-109">Example 2: Get all peerings in virtual network</span></span>
```
# Get all virtual network peerings located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1To*" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="b1620-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1620-110">PARAMETERS</span></span>

### <span data-ttu-id="b1620-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1620-111">-DefaultProfile</span></span>
<span data-ttu-id="b1620-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b1620-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1620-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b1620-113">-Name</span></span>
<span data-ttu-id="b1620-114">가상 네트워크 피어링 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b1620-114">Specifies the virtual network peering name.</span></span>

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

### <span data-ttu-id="b1620-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1620-115">-ResourceGroupName</span></span>
<span data-ttu-id="b1620-116">가상 네트워크 피어링이 속한 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b1620-116">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="b1620-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="b1620-117">-VirtualNetworkName</span></span>
<span data-ttu-id="b1620-118">이 cmdlet이 얻을 가상 네트워크 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b1620-118">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b1620-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1620-119">CommonParameters</span></span>
<span data-ttu-id="b1620-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b1620-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1620-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b1620-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1620-122">입력</span><span class="sxs-lookup"><span data-stu-id="b1620-122">INPUTS</span></span>

### <span data-ttu-id="b1620-123">System.String</span><span class="sxs-lookup"><span data-stu-id="b1620-123">System.String</span></span>

## <span data-ttu-id="b1620-124">출력</span><span class="sxs-lookup"><span data-stu-id="b1620-124">OUTPUTS</span></span>

### <span data-ttu-id="b1620-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b1620-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="b1620-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b1620-126">NOTES</span></span>

## <span data-ttu-id="b1620-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1620-127">RELATED LINKS</span></span>

[<span data-ttu-id="b1620-128">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b1620-128">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="b1620-129">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b1620-129">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="b1620-130">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b1620-130">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
