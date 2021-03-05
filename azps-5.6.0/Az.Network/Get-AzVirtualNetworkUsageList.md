---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: b4daa24f787633d2f18896910faed340a969a0f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997710"
---
# <span data-ttu-id="b236b-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="b236b-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="b236b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b236b-102">SYNOPSIS</span></span>
<span data-ttu-id="b236b-103">가상 네트워크 현재 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b236b-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="b236b-104">구문</span><span class="sxs-lookup"><span data-stu-id="b236b-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b236b-105">설명</span><span class="sxs-lookup"><span data-stu-id="b236b-105">DESCRIPTION</span></span>
<span data-ttu-id="b236b-106">**Get-AzVirtualNetworkUsageList** cmdlet은 지정된 가상 네트워크에 대한 서브넷 사용량당 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b236b-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="b236b-107">예제</span><span class="sxs-lookup"><span data-stu-id="b236b-107">EXAMPLES</span></span>

### <span data-ttu-id="b236b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b236b-108">Example 1</span></span>
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

<span data-ttu-id="b236b-109">사용량이 가장 많은 가상 네트워크에 대한 서브넷 현재 값당 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b236b-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="b236b-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b236b-110">PARAMETERS</span></span>

### <span data-ttu-id="b236b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b236b-111">-DefaultProfile</span></span>
<span data-ttu-id="b236b-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b236b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b236b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b236b-113">-Name</span></span>
<span data-ttu-id="b236b-114">에 대한 사용량을 표시하기 위해 가상 네트워크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b236b-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="b236b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b236b-115">-ResourceGroupName</span></span>
<span data-ttu-id="b236b-116">가상 네트워크가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b236b-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="b236b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b236b-117">CommonParameters</span></span>
<span data-ttu-id="b236b-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b236b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b236b-119">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b236b-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b236b-120">입력</span><span class="sxs-lookup"><span data-stu-id="b236b-120">INPUTS</span></span>

### <span data-ttu-id="b236b-121">System.String</span><span class="sxs-lookup"><span data-stu-id="b236b-121">System.String</span></span>

## <span data-ttu-id="b236b-122">출력</span><span class="sxs-lookup"><span data-stu-id="b236b-122">OUTPUTS</span></span>

### <span data-ttu-id="b236b-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="b236b-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="b236b-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b236b-124">NOTES</span></span>

## <span data-ttu-id="b236b-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b236b-125">RELATED LINKS</span></span>
