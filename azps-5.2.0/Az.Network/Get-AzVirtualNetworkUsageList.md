---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: 023eb245132a7b451fc6e30351db5751fb754cde
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325919"
---
# <span data-ttu-id="df421-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="df421-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="df421-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df421-102">SYNOPSIS</span></span>
<span data-ttu-id="df421-103">가상 네트워크 현재 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="df421-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="df421-104">구문</span><span class="sxs-lookup"><span data-stu-id="df421-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df421-105">설명</span><span class="sxs-lookup"><span data-stu-id="df421-105">DESCRIPTION</span></span>
<span data-ttu-id="df421-106">**Get-AzVirtualNetworkUsageList** cmdlet은 지정된 가상 네트워크에 대한 서브넷 사용량당 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="df421-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="df421-107">예제</span><span class="sxs-lookup"><span data-stu-id="df421-107">EXAMPLES</span></span>

### <span data-ttu-id="df421-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="df421-108">Example 1</span></span>
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

<span data-ttu-id="df421-109">사용량이 가장 많은 가상 네트워크에 대한 사용 현황의 서브넷당 현재 값을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="df421-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="df421-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df421-110">PARAMETERS</span></span>

### <span data-ttu-id="df421-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df421-111">-DefaultProfile</span></span>
<span data-ttu-id="df421-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="df421-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df421-113">-Name</span><span class="sxs-lookup"><span data-stu-id="df421-113">-Name</span></span>
<span data-ttu-id="df421-114">사용량을 표시하는 가상 네트워크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df421-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="df421-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df421-115">-ResourceGroupName</span></span>
<span data-ttu-id="df421-116">가상 네트워크가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df421-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="df421-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df421-117">CommonParameters</span></span>
<span data-ttu-id="df421-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="df421-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df421-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="df421-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df421-120">입력</span><span class="sxs-lookup"><span data-stu-id="df421-120">INPUTS</span></span>

### <span data-ttu-id="df421-121">System.String</span><span class="sxs-lookup"><span data-stu-id="df421-121">System.String</span></span>

## <span data-ttu-id="df421-122">출력</span><span class="sxs-lookup"><span data-stu-id="df421-122">OUTPUTS</span></span>

### <span data-ttu-id="df421-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="df421-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="df421-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="df421-124">NOTES</span></span>

## <span data-ttu-id="df421-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="df421-125">RELATED LINKS</span></span>
