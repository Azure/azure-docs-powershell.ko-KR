---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkusagelist
schema: 2.0.0
ms.openlocfilehash: 61717f314629259caca9329c2ef1a458aa9a0e0f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880378"
---
# <span data-ttu-id="24c9f-101">Get-AzureRmVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="24c9f-101">Get-AzureRmVirtualNetworkUsageList</span></span>

## <span data-ttu-id="24c9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24c9f-102">SYNOPSIS</span></span>
<span data-ttu-id="24c9f-103">가상 네트워크의 현재 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24c9f-103">Gets virtual network current usage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24c9f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24c9f-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24c9f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="24c9f-105">DESCRIPTION</span></span>
<span data-ttu-id="24c9f-106">**AzureRmVirtualNetworkUsageList** cmdlet은 지정 된 가상 네트워크에 대 한 각 서브넷 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24c9f-106">The **Get-AzureRmVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="24c9f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="24c9f-107">EXAMPLES</span></span>

### <span data-ttu-id="24c9f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="24c9f-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Get-AzureRmVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

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

<span data-ttu-id="24c9f-109">Usagetest 가상 네트워크에 대 한 사용량의 서브넷 별 전류 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24c9f-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="24c9f-110">변수</span><span class="sxs-lookup"><span data-stu-id="24c9f-110">PARAMETERS</span></span>

### <span data-ttu-id="24c9f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24c9f-111">-DefaultProfile</span></span>
<span data-ttu-id="24c9f-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24c9f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24c9f-113">-이름</span><span class="sxs-lookup"><span data-stu-id="24c9f-113">-Name</span></span>
<span data-ttu-id="24c9f-114">용도를 표시할 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c9f-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="24c9f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24c9f-115">-ResourceGroupName</span></span>
<span data-ttu-id="24c9f-116">가상 네트워크가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c9f-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="24c9f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24c9f-117">CommonParameters</span></span>
<span data-ttu-id="24c9f-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c9f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24c9f-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24c9f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24c9f-120">입력</span><span class="sxs-lookup"><span data-stu-id="24c9f-120">INPUTS</span></span>

### <span data-ttu-id="24c9f-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="24c9f-121">System.String</span></span>

## <span data-ttu-id="24c9f-122">출력</span><span class="sxs-lookup"><span data-stu-id="24c9f-122">OUTPUTS</span></span>

### <span data-ttu-id="24c9f-123">PSVirtualNetworkUsage에 대 한.</span><span class="sxs-lookup"><span data-stu-id="24c9f-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="24c9f-124">상속자</span><span class="sxs-lookup"><span data-stu-id="24c9f-124">NOTES</span></span>

## <span data-ttu-id="24c9f-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24c9f-125">RELATED LINKS</span></span>

