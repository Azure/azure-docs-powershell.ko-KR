---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 63859bb6b7520264671a9190919c43e1f79e0341
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532146"
---
# <span data-ttu-id="19bb7-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="19bb7-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="19bb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19bb7-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19bb7-103">구문과</span><span class="sxs-lookup"><span data-stu-id="19bb7-103">SYNTAX</span></span>

### <span data-ttu-id="19bb7-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="19bb7-104">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="19bb7-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="19bb7-105">SetByResource</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="19bb7-106">설명은</span><span class="sxs-lookup"><span data-stu-id="19bb7-106">DESCRIPTION</span></span>

## <span data-ttu-id="19bb7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="19bb7-107">EXAMPLES</span></span>

### <span data-ttu-id="19bb7-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="19bb7-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="19bb7-109">변수</span><span class="sxs-lookup"><span data-stu-id="19bb7-109">PARAMETERS</span></span>

### <span data-ttu-id="19bb7-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="19bb7-110">-BackendPort</span></span>
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

### <span data-ttu-id="19bb7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19bb7-111">-DefaultProfile</span></span>
<span data-ttu-id="19bb7-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="19bb7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19bb7-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="19bb7-113">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="19bb7-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="19bb7-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="19bb7-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="19bb7-115">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="19bb7-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="19bb7-116">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="19bb7-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="19bb7-117">-LoadBalancer</span></span>
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

### <span data-ttu-id="19bb7-118">-이름</span><span class="sxs-lookup"><span data-stu-id="19bb7-118">-Name</span></span>
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

### <span data-ttu-id="19bb7-119">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="19bb7-119">-Protocol</span></span>
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

### <span data-ttu-id="19bb7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19bb7-120">CommonParameters</span></span>
<span data-ttu-id="19bb7-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bb7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19bb7-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19bb7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19bb7-123">입력</span><span class="sxs-lookup"><span data-stu-id="19bb7-123">INPUTS</span></span>

### <span data-ttu-id="19bb7-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="19bb7-124">PSLoadBalancer</span></span>
<span data-ttu-id="19bb7-125">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bb7-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="19bb7-126">출력</span><span class="sxs-lookup"><span data-stu-id="19bb7-126">OUTPUTS</span></span>

### <span data-ttu-id="19bb7-127">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="19bb7-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="19bb7-128">상속자</span><span class="sxs-lookup"><span data-stu-id="19bb7-128">NOTES</span></span>

## <span data-ttu-id="19bb7-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19bb7-129">RELATED LINKS</span></span>

