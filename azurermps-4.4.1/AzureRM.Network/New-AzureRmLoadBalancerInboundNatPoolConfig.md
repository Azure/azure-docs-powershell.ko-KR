---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 85d58154d8dd1d93e37a55b9fd0b9d306283b899
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536275"
---
# <span data-ttu-id="5684e-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="5684e-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="5684e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5684e-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5684e-103">구문과</span><span class="sxs-lookup"><span data-stu-id="5684e-103">SYNTAX</span></span>

### <span data-ttu-id="5684e-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5684e-104">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> [-FrontendIpConfigurationId <String>]
 -Protocol <String> -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5684e-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5684e-105">SetByResource</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5684e-106">설명은</span><span class="sxs-lookup"><span data-stu-id="5684e-106">DESCRIPTION</span></span>

## <span data-ttu-id="5684e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5684e-107">EXAMPLES</span></span>

## <span data-ttu-id="5684e-108">변수</span><span class="sxs-lookup"><span data-stu-id="5684e-108">PARAMETERS</span></span>

### <span data-ttu-id="5684e-109">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="5684e-109">-BackendPort</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5684e-110">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="5684e-110">-FrontendIpConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5684e-111">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5684e-111">-FrontendIpConfigurationId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5684e-112">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="5684e-112">-FrontendPortRangeEnd</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5684e-113">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="5684e-113">-FrontendPortRangeStart</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5684e-114">-이름</span><span class="sxs-lookup"><span data-stu-id="5684e-114">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5684e-115">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="5684e-115">-Protocol</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5684e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5684e-116">-DefaultProfile</span></span>
<span data-ttu-id="5684e-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5684e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5684e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5684e-118">CommonParameters</span></span>
<span data-ttu-id="5684e-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5684e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5684e-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5684e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5684e-121">입력</span><span class="sxs-lookup"><span data-stu-id="5684e-121">INPUTS</span></span>

## <span data-ttu-id="5684e-122">출력</span><span class="sxs-lookup"><span data-stu-id="5684e-122">OUTPUTS</span></span>

### <span data-ttu-id="5684e-123">PSInboundNatPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5684e-123">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="5684e-124">상속자</span><span class="sxs-lookup"><span data-stu-id="5684e-124">NOTES</span></span>

## <span data-ttu-id="5684e-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5684e-125">RELATED LINKS</span></span>

