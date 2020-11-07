---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: 75725505e7c5239f1b5dc8f05d4cdfe3cf2b4903
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875503"
---
# <span data-ttu-id="dffb9-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="dffb9-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="dffb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dffb9-102">SYNOPSIS</span></span>
<span data-ttu-id="dffb9-103">가상 네트워크 피어 링을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dffb9-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="dffb9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dffb9-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dffb9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dffb9-105">DESCRIPTION</span></span>
<span data-ttu-id="dffb9-106">**AzVirtualNetworkPeering** cmdlet은 가상 네트워크 피어 링을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dffb9-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="dffb9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dffb9-107">EXAMPLES</span></span>

### <span data-ttu-id="dffb9-108">예제 1: 두 가상 네트워크 간 피어 링 가져오기</span><span class="sxs-lookup"><span data-stu-id="dffb9-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="dffb9-109">변수</span><span class="sxs-lookup"><span data-stu-id="dffb9-109">PARAMETERS</span></span>

### <span data-ttu-id="dffb9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dffb9-110">-DefaultProfile</span></span>
<span data-ttu-id="dffb9-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dffb9-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dffb9-112">-이름</span><span class="sxs-lookup"><span data-stu-id="dffb9-112">-Name</span></span>
<span data-ttu-id="dffb9-113">가상 네트워크 피어 링 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dffb9-113">Specifies the virtual network peering name.</span></span>

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

### <span data-ttu-id="dffb9-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dffb9-114">-ResourceGroupName</span></span>
<span data-ttu-id="dffb9-115">가상 네트워크 피어 링이 속한 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dffb9-115">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="dffb9-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="dffb9-116">-VirtualNetworkName</span></span>
<span data-ttu-id="dffb9-117">이 cmdlet이 가져오는 가상 네트워크 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dffb9-117">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="dffb9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dffb9-118">CommonParameters</span></span>
<span data-ttu-id="dffb9-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dffb9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dffb9-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dffb9-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dffb9-121">입력</span><span class="sxs-lookup"><span data-stu-id="dffb9-121">INPUTS</span></span>

## <span data-ttu-id="dffb9-122">출력</span><span class="sxs-lookup"><span data-stu-id="dffb9-122">OUTPUTS</span></span>

### <span data-ttu-id="dffb9-123">PSVirtualNetworkPeering에 대 한.</span><span class="sxs-lookup"><span data-stu-id="dffb9-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="dffb9-124">상속자</span><span class="sxs-lookup"><span data-stu-id="dffb9-124">NOTES</span></span>

## <span data-ttu-id="dffb9-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dffb9-125">RELATED LINKS</span></span>

[<span data-ttu-id="dffb9-126">추가-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="dffb9-126">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="dffb9-127">제거-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="dffb9-127">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="dffb9-128">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="dffb9-128">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)


