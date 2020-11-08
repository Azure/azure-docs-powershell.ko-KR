---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: 023eb245132a7b451fc6e30351db5751fb754cde
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034828"
---
# <span data-ttu-id="9ee26-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="9ee26-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="9ee26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ee26-102">SYNOPSIS</span></span>
<span data-ttu-id="9ee26-103">가상 네트워크의 현재 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ee26-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="9ee26-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9ee26-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ee26-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9ee26-105">DESCRIPTION</span></span>
<span data-ttu-id="9ee26-106">**AzVirtualNetworkUsageList** cmdlet은 지정 된 가상 네트워크에 대 한 각 서브넷 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ee26-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="9ee26-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9ee26-107">EXAMPLES</span></span>

### <span data-ttu-id="9ee26-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9ee26-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Get-AzVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet
CurrentValue : 1
Limit        : 65531
Unit         : Count

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet11
CurrentValue : 0
Limit        : 251
Unit         : Count
```

<span data-ttu-id="9ee26-109">Usagetest 가상 네트워크에 대 한 사용량의 서브넷 별 전류 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ee26-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="9ee26-110">변수</span><span class="sxs-lookup"><span data-stu-id="9ee26-110">PARAMETERS</span></span>

### <span data-ttu-id="9ee26-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ee26-111">-DefaultProfile</span></span>
<span data-ttu-id="9ee26-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ee26-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ee26-113">-이름</span><span class="sxs-lookup"><span data-stu-id="9ee26-113">-Name</span></span>
<span data-ttu-id="9ee26-114">용도를 표시할 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ee26-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="9ee26-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ee26-115">-ResourceGroupName</span></span>
<span data-ttu-id="9ee26-116">가상 네트워크가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ee26-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="9ee26-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ee26-117">CommonParameters</span></span>
<span data-ttu-id="9ee26-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ee26-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ee26-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9ee26-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ee26-120">입력</span><span class="sxs-lookup"><span data-stu-id="9ee26-120">INPUTS</span></span>

### <span data-ttu-id="9ee26-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9ee26-121">System.String</span></span>

## <span data-ttu-id="9ee26-122">출력</span><span class="sxs-lookup"><span data-stu-id="9ee26-122">OUTPUTS</span></span>

### <span data-ttu-id="9ee26-123">PSVirtualNetworkUsage에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9ee26-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="9ee26-124">상속자</span><span class="sxs-lookup"><span data-stu-id="9ee26-124">NOTES</span></span>

## <span data-ttu-id="9ee26-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ee26-125">RELATED LINKS</span></span>
