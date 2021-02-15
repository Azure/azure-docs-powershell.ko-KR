---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaylearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: 69665b57e1c378b6a5b134228da479096ba45445
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193708"
---
# <span data-ttu-id="77525-101">Get-AzVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="77525-101">Get-AzVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="77525-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77525-102">SYNOPSIS</span></span>
<span data-ttu-id="77525-103">Azure 가상 네트워크 게이트웨이에서 학습한 경로를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="77525-103">Lists routes learned by an Azure virtual network gateway</span></span>

## <span data-ttu-id="77525-104">구문</span><span class="sxs-lookup"><span data-stu-id="77525-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77525-105">설명</span><span class="sxs-lookup"><span data-stu-id="77525-105">DESCRIPTION</span></span>
<span data-ttu-id="77525-106">다양한 원본에서 Azure 가상 네트워크 게이트웨이에서 학습한 경로를 열회합니다.</span><span class="sxs-lookup"><span data-stu-id="77525-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="77525-107">여기에는 정적 경로뿐만 아니라 BGP를 통해 학습된 경로도 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="77525-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="77525-108">예제</span><span class="sxs-lookup"><span data-stu-id="77525-108">EXAMPLES</span></span>

### <span data-ttu-id="77525-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="77525-109">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayLearnedRoute -ResourceGroupName resourceGroup -VirtualNetworkGatewayname gatewayName

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.1.0.0/16
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.0.0.254/32
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       : 65515
LocalAddress : 10.1.0.254
Network      : 10.0.0.0/16
NextHop      : 10.0.0.254
Origin       : EBgp
SourcePeer   : 10.0.0.254
Weight       : 32768
```

<span data-ttu-id="77525-110">리소스 그룹 resourceGroup에서 게이트웨이 이름이라는 Azure 가상 네트워크 게이트웨이의 경우 Azure 게이트웨이가 알고 있는 경로를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="77525-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> <span data-ttu-id="77525-111">이 경우 Azure 가상 네트워크 게이트웨이에는 두 개의 정적 경로(10.1.0.0/16 및 10.0.0.254/32)와 BGP를 통해 학습된 하나의 경로(10.0.0.0/16)가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77525-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="77525-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77525-112">PARAMETERS</span></span>

### <span data-ttu-id="77525-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77525-113">-AsJob</span></span>
<span data-ttu-id="77525-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="77525-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77525-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77525-115">-DefaultProfile</span></span>
<span data-ttu-id="77525-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="77525-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77525-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77525-117">-ResourceGroupName</span></span>
<span data-ttu-id="77525-118">가상 네트워크 게이트웨이 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="77525-118">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="77525-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="77525-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="77525-120">가상 네트워크 게이트웨이 이름</span><span class="sxs-lookup"><span data-stu-id="77525-120">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77525-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77525-121">CommonParameters</span></span>
<span data-ttu-id="77525-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="77525-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77525-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="77525-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77525-124">입력</span><span class="sxs-lookup"><span data-stu-id="77525-124">INPUTS</span></span>

### <span data-ttu-id="77525-125">System.String</span><span class="sxs-lookup"><span data-stu-id="77525-125">System.String</span></span>

## <span data-ttu-id="77525-126">출력</span><span class="sxs-lookup"><span data-stu-id="77525-126">OUTPUTS</span></span>

### <span data-ttu-id="77525-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="77525-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="77525-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="77525-128">NOTES</span></span>

## <span data-ttu-id="77525-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77525-129">RELATED LINKS</span></span>
