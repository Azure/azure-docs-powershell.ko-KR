---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: a5cd44d1b4b7ac1a1494047affa721dd21d85919
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875677"
---
# <span data-ttu-id="c84e1-101">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c84e1-101">Add-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="c84e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c84e1-102">SYNOPSIS</span></span>

## <span data-ttu-id="c84e1-103">구문과</span><span class="sxs-lookup"><span data-stu-id="c84e1-103">SYNTAX</span></span>

### <span data-ttu-id="c84e1-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c84e1-104">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c84e1-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c84e1-105">SetByResource</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c84e1-106">설명은</span><span class="sxs-lookup"><span data-stu-id="c84e1-106">DESCRIPTION</span></span>

## <span data-ttu-id="c84e1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c84e1-107">EXAMPLES</span></span>

### <span data-ttu-id="c84e1-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="c84e1-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="c84e1-109">변수</span><span class="sxs-lookup"><span data-stu-id="c84e1-109">PARAMETERS</span></span>

### <span data-ttu-id="c84e1-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="c84e1-110">-BackendPort</span></span>
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

### <span data-ttu-id="c84e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c84e1-111">-DefaultProfile</span></span>
<span data-ttu-id="c84e1-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c84e1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c84e1-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c84e1-113">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="c84e1-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c84e1-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="c84e1-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="c84e1-115">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="c84e1-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="c84e1-116">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="c84e1-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c84e1-117">-LoadBalancer</span></span>
```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c84e1-118">-이름</span><span class="sxs-lookup"><span data-stu-id="c84e1-118">-Name</span></span>
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

### <span data-ttu-id="c84e1-119">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="c84e1-119">-Protocol</span></span>
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

### <span data-ttu-id="c84e1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c84e1-120">CommonParameters</span></span>
<span data-ttu-id="c84e1-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c84e1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c84e1-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c84e1-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c84e1-123">입력</span><span class="sxs-lookup"><span data-stu-id="c84e1-123">INPUTS</span></span>

### <span data-ttu-id="c84e1-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c84e1-124">PSLoadBalancer</span></span>
<span data-ttu-id="c84e1-125">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c84e1-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="c84e1-126">출력</span><span class="sxs-lookup"><span data-stu-id="c84e1-126">OUTPUTS</span></span>

### <span data-ttu-id="c84e1-127">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c84e1-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c84e1-128">상속자</span><span class="sxs-lookup"><span data-stu-id="c84e1-128">NOTES</span></span>

## <span data-ttu-id="c84e1-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c84e1-129">RELATED LINKS</span></span>

