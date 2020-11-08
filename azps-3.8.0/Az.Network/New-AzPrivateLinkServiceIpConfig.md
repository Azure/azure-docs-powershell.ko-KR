---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkserviceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
ms.openlocfilehash: e1d7c2d78bf58240cc87e7a224be1632828984d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043257"
---
# <span data-ttu-id="62b1d-101">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="62b1d-101">New-AzPrivateLinkServiceIpConfig</span></span>

## <span data-ttu-id="62b1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62b1d-102">SYNOPSIS</span></span>
<span data-ttu-id="62b1d-103">개인 링크 서비스 ip 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="62b1d-103">Create a private link service ip configuration.</span></span>

## <span data-ttu-id="62b1d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="62b1d-104">SYNTAX</span></span>

```
New-AzPrivateLinkServiceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-PublicIpAddress <PSPublicIpAddress>]
 [-Subnet <PSSubnet>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62b1d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="62b1d-105">DESCRIPTION</span></span>
<span data-ttu-id="62b1d-106">**AzPrivateLinkServiceIpConfig** cmdlet은 개인 링크 서비스 ip 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="62b1d-106">The **New-AzPrivateLinkServiceIpConfig** cmdlet creates a private link service ip configuration.</span></span> <span data-ttu-id="62b1d-107">이 구성은 원본 NAT에 사용 되며, 개인 끝점에서 들어오는 트래픽을 전송 합니다.</span><span class="sxs-lookup"><span data-stu-id="62b1d-107">This configuration is used for source NAT-ing the incoming traffic from private endpoint.</span></span> 

## <span data-ttu-id="62b1d-108">예제의</span><span class="sxs-lookup"><span data-stu-id="62b1d-108">EXAMPLES</span></span>

### <span data-ttu-id="62b1d-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="62b1d-109">Example 1</span></span>
```
New-AzPrivateLinkServiceIpConfig -Name $IpConfigurationName -PrivateIpAddress "10.0.0.5" -Primary
```

<span data-ttu-id="62b1d-110">이 예제에서는 메모리에 개인 링크 서비스 ip 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="62b1d-110">This example create a private link service ip configuration in memory.</span></span>

## <span data-ttu-id="62b1d-111">변수</span><span class="sxs-lookup"><span data-stu-id="62b1d-111">PARAMETERS</span></span>

### <span data-ttu-id="62b1d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62b1d-112">-DefaultProfile</span></span>
<span data-ttu-id="62b1d-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="62b1d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62b1d-114">-이름</span><span class="sxs-lookup"><span data-stu-id="62b1d-114">-Name</span></span>
<span data-ttu-id="62b1d-115">IpConfiguration의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="62b1d-115">The name of the IpConfiguration</span></span>

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

### <span data-ttu-id="62b1d-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="62b1d-116">-PrivateIpAddress</span></span>
<span data-ttu-id="62b1d-117">정적 할당이 지정 된 경우 ipConfiguration의 개인 ip 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="62b1d-117">The private ip address of the ipConfiguration if static allocation is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62b1d-118">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="62b1d-118">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="62b1d-119">Ip 구성의 ip 버전</span><span class="sxs-lookup"><span data-stu-id="62b1d-119">The ip version of the ip configuration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62b1d-120">-기본</span><span class="sxs-lookup"><span data-stu-id="62b1d-120">-Primary</span></span>
<span data-ttu-id="62b1d-121">현재 ip 구성이 기본 설정 인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="62b1d-121">Indicate current ip configuration is primary or not.</span></span>

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

### <span data-ttu-id="62b1d-122">-서브넷</span><span class="sxs-lookup"><span data-stu-id="62b1d-122">-Subnet</span></span>
<span data-ttu-id="62b1d-123">서브넷</span><span class="sxs-lookup"><span data-stu-id="62b1d-123">Subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62b1d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62b1d-124">CommonParameters</span></span>
<span data-ttu-id="62b1d-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="62b1d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62b1d-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="62b1d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62b1d-127">입력</span><span class="sxs-lookup"><span data-stu-id="62b1d-127">INPUTS</span></span>

### <span data-ttu-id="62b1d-128">않아야</span><span class="sxs-lookup"><span data-stu-id="62b1d-128">None</span></span>

## <span data-ttu-id="62b1d-129">출력</span><span class="sxs-lookup"><span data-stu-id="62b1d-129">OUTPUTS</span></span>

### <span data-ttu-id="62b1d-130">PSPrivateLinkServiceIpConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="62b1d-130">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration</span></span>

## <span data-ttu-id="62b1d-131">상속자</span><span class="sxs-lookup"><span data-stu-id="62b1d-131">NOTES</span></span>

## <span data-ttu-id="62b1d-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="62b1d-132">RELATED LINKS</span></span>

[<span data-ttu-id="62b1d-133">새로운 AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="62b1d-133">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)