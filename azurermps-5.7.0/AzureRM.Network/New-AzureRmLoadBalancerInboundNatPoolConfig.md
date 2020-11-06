---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 875a42742c153bf6a1fad8e2ae1ad2b0e025c833
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532110"
---
# <span data-ttu-id="c3b91-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c3b91-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="c3b91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3b91-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3b91-103">구문과</span><span class="sxs-lookup"><span data-stu-id="c3b91-103">SYNTAX</span></span>

### <span data-ttu-id="c3b91-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c3b91-104">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> [-FrontendIpConfigurationId <String>]
 -Protocol <String> -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3b91-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c3b91-105">SetByResource</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c3b91-106">설명은</span><span class="sxs-lookup"><span data-stu-id="c3b91-106">DESCRIPTION</span></span>

## <span data-ttu-id="c3b91-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c3b91-107">EXAMPLES</span></span>

## <span data-ttu-id="c3b91-108">변수</span><span class="sxs-lookup"><span data-stu-id="c3b91-108">PARAMETERS</span></span>

### <span data-ttu-id="c3b91-109">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="c3b91-109">-BackendPort</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b91-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3b91-110">-DefaultProfile</span></span>
<span data-ttu-id="c3b91-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c3b91-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3b91-112">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3b91-112">-FrontendIpConfiguration</span></span>
```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b91-113">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c3b91-113">-FrontendIpConfigurationId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b91-114">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="c3b91-114">-FrontendPortRangeEnd</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b91-115">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="c3b91-115">-FrontendPortRangeStart</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b91-116">-이름</span><span class="sxs-lookup"><span data-stu-id="c3b91-116">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b91-117">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="c3b91-117">-Protocol</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b91-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3b91-118">CommonParameters</span></span>
<span data-ttu-id="c3b91-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3b91-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3b91-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3b91-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3b91-121">입력</span><span class="sxs-lookup"><span data-stu-id="c3b91-121">INPUTS</span></span>

### <span data-ttu-id="c3b91-122">않아야</span><span class="sxs-lookup"><span data-stu-id="c3b91-122">None</span></span>
<span data-ttu-id="c3b91-123">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c3b91-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c3b91-124">출력</span><span class="sxs-lookup"><span data-stu-id="c3b91-124">OUTPUTS</span></span>

### <span data-ttu-id="c3b91-125">PSInboundNatPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="c3b91-125">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="c3b91-126">상속자</span><span class="sxs-lookup"><span data-stu-id="c3b91-126">NOTES</span></span>

## <span data-ttu-id="c3b91-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c3b91-127">RELATED LINKS</span></span>

