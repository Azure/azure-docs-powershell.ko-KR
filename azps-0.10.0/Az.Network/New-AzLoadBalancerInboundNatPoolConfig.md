---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 9a6879d2b5ad18c33ca53befd94d5e8dc03225df
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875429"
---
# <span data-ttu-id="fc7f4-101">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="fc7f4-101">New-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="fc7f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc7f4-102">SYNOPSIS</span></span>

## <span data-ttu-id="fc7f4-103">구문과</span><span class="sxs-lookup"><span data-stu-id="fc7f4-103">SYNTAX</span></span>

### <span data-ttu-id="fc7f4-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fc7f4-104">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> [-FrontendIpConfigurationId <String>]
 -Protocol <String> -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc7f4-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="fc7f4-105">SetByResource</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc7f4-106">설명은</span><span class="sxs-lookup"><span data-stu-id="fc7f4-106">DESCRIPTION</span></span>

## <span data-ttu-id="fc7f4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fc7f4-107">EXAMPLES</span></span>

### <span data-ttu-id="fc7f4-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="fc7f4-108">1:</span></span>
```

```

## <span data-ttu-id="fc7f4-109">변수</span><span class="sxs-lookup"><span data-stu-id="fc7f4-109">PARAMETERS</span></span>

### <span data-ttu-id="fc7f4-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="fc7f4-110">-BackendPort</span></span>
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

### <span data-ttu-id="fc7f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc7f4-111">-DefaultProfile</span></span>
<span data-ttu-id="fc7f4-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fc7f4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc7f4-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc7f4-113">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="fc7f4-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="fc7f4-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="fc7f4-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="fc7f4-115">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="fc7f4-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="fc7f4-116">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="fc7f4-117">-이름</span><span class="sxs-lookup"><span data-stu-id="fc7f4-117">-Name</span></span>
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

### <span data-ttu-id="fc7f4-118">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="fc7f4-118">-Protocol</span></span>
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

### <span data-ttu-id="fc7f4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc7f4-119">CommonParameters</span></span>
<span data-ttu-id="fc7f4-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc7f4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc7f4-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc7f4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc7f4-122">입력</span><span class="sxs-lookup"><span data-stu-id="fc7f4-122">INPUTS</span></span>

## <span data-ttu-id="fc7f4-123">출력</span><span class="sxs-lookup"><span data-stu-id="fc7f4-123">OUTPUTS</span></span>

### <span data-ttu-id="fc7f4-124">PSInboundNatPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="fc7f4-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="fc7f4-125">상속자</span><span class="sxs-lookup"><span data-stu-id="fc7f4-125">NOTES</span></span>

## <span data-ttu-id="fc7f4-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc7f4-126">RELATED LINKS</span></span>

