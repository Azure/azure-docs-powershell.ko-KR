---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: fffc77c4cfdd74a910086befb88d665351ae36a8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870061"
---
# <span data-ttu-id="f10af-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="f10af-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="f10af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f10af-102">SYNOPSIS</span></span>
<span data-ttu-id="f10af-103">가상 네트워크의 현재 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f10af-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="f10af-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f10af-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f10af-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f10af-105">DESCRIPTION</span></span>
<span data-ttu-id="f10af-106">**AzVirtualNetworkUsageList** cmdlet은 지정 된 가상 네트워크에 대 한 각 서브넷 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f10af-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="f10af-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f10af-107">EXAMPLES</span></span>

### <span data-ttu-id="f10af-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f10af-108">Example 1</span></span>
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

<span data-ttu-id="f10af-109">Usagetest 가상 네트워크에 대 한 사용량의 서브넷 별 전류 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f10af-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="f10af-110">변수</span><span class="sxs-lookup"><span data-stu-id="f10af-110">PARAMETERS</span></span>

### <span data-ttu-id="f10af-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f10af-111">-DefaultProfile</span></span>
<span data-ttu-id="f10af-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f10af-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f10af-113">-이름</span><span class="sxs-lookup"><span data-stu-id="f10af-113">-Name</span></span>
<span data-ttu-id="f10af-114">용도를 표시할 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f10af-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="f10af-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f10af-115">-ResourceGroupName</span></span>
<span data-ttu-id="f10af-116">가상 네트워크가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f10af-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="f10af-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f10af-117">CommonParameters</span></span>
<span data-ttu-id="f10af-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f10af-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f10af-119">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f10af-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f10af-120">입력</span><span class="sxs-lookup"><span data-stu-id="f10af-120">INPUTS</span></span>

### <span data-ttu-id="f10af-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f10af-121">System.String</span></span>

## <span data-ttu-id="f10af-122">출력</span><span class="sxs-lookup"><span data-stu-id="f10af-122">OUTPUTS</span></span>

### <span data-ttu-id="f10af-123">PSVirtualNetworkUsage에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f10af-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="f10af-124">상속자</span><span class="sxs-lookup"><span data-stu-id="f10af-124">NOTES</span></span>

## <span data-ttu-id="f10af-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f10af-125">RELATED LINKS</span></span>
