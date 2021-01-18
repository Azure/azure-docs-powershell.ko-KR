---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
ms.openlocfilehash: 5a6cbbc007c372d2e1765e4e2369d2f3d60d0a07
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492600"
---
# <span data-ttu-id="fa030-101">New-AzIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="fa030-101">New-AzIpsecPolicy</span></span>

## <span data-ttu-id="fa030-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa030-102">SYNOPSIS</span></span>
<span data-ttu-id="fa030-103">IPSec 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fa030-103">Creates an IPSec Policy.</span></span>

## <span data-ttu-id="fa030-104">구문</span><span class="sxs-lookup"><span data-stu-id="fa030-104">SYNTAX</span></span>

```
New-AzIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa030-105">설명</span><span class="sxs-lookup"><span data-stu-id="fa030-105">DESCRIPTION</span></span>
<span data-ttu-id="fa030-106">New-AzIpsecPolicy cmdlet은 가상 네트워크 게이트웨이 연결에 사용할 IPSec 정책 제안을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fa030-106">The New-AzIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="fa030-107">예제</span><span class="sxs-lookup"><span data-stu-id="fa030-107">EXAMPLES</span></span>

### <span data-ttu-id="fa030-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fa030-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="fa030-109">새 가상 네트워크 게이트웨이 연결에 사용할 IPSec 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="fa030-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="fa030-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa030-110">PARAMETERS</span></span>

### <span data-ttu-id="fa030-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa030-111">-DefaultProfile</span></span>
<span data-ttu-id="fa030-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fa030-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa030-113">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="fa030-113">-DhGroup</span></span>
<span data-ttu-id="fa030-114">IKE 1단계에서 초기 SA에 사용되는 DH 그룹</span><span class="sxs-lookup"><span data-stu-id="fa030-114">The DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, DHGroup1, DHGroup14, DHGroup2, DHGroup2048, DHGroup24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa030-115">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="fa030-115">-IkeEncryption</span></span>
<span data-ttu-id="fa030-116">IKE 암호화 알고리즘(IKE 1단계)</span><span class="sxs-lookup"><span data-stu-id="fa030-116">The IKE encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DES, DES3, AES128, AES192, AES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa030-117">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="fa030-117">-IkeIntegrity</span></span>
<span data-ttu-id="fa030-118">IKE 무결성 알고리즘(IKE 1단계)</span><span class="sxs-lookup"><span data-stu-id="fa030-118">The IKE integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MD5, SHA1, SHA256, SHA384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa030-119">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="fa030-119">-IpsecEncryption</span></span>
<span data-ttu-id="fa030-120">IPSec 암호화 알고리즘(IKE 2단계)</span><span class="sxs-lookup"><span data-stu-id="fa030-120">The IPSec encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, DES, DES3, AES128, AES192, AES256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa030-121">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="fa030-121">-IpsecIntegrity</span></span>
<span data-ttu-id="fa030-122">IPSec 무결성 알고리즘(IKE 2단계)</span><span class="sxs-lookup"><span data-stu-id="fa030-122">The IPSec integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MD5, SHA1, SHA256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa030-123">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="fa030-123">-PfsGroup</span></span>
<span data-ttu-id="fa030-124">새 자식 SA에 대한 IKE 2단계에서 사용되는 DH 그룹</span><span class="sxs-lookup"><span data-stu-id="fa030-124">The DH Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, PFS1, PFS2, PFS2048, PFS24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa030-125">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="fa030-125">-SADataSizeKilobytes</span></span>
<span data-ttu-id="fa030-126">IPSec 보안 연결(빠른 모드 또는 2단계 SA라고도 하는) 페이로드 크기(KB)</span><span class="sxs-lookup"><span data-stu-id="fa030-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa030-127">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="fa030-127">-SALifeTimeSeconds</span></span>
<span data-ttu-id="fa030-128">IPSec 보안 연결(빠른 모드 또는 2단계 SA라고도 하는) 수명(초)</span><span class="sxs-lookup"><span data-stu-id="fa030-128">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa030-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa030-129">CommonParameters</span></span>
<span data-ttu-id="fa030-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fa030-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa030-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fa030-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa030-132">입력</span><span class="sxs-lookup"><span data-stu-id="fa030-132">INPUTS</span></span>

### <span data-ttu-id="fa030-133">없음</span><span class="sxs-lookup"><span data-stu-id="fa030-133">None</span></span>

## <span data-ttu-id="fa030-134">출력</span><span class="sxs-lookup"><span data-stu-id="fa030-134">OUTPUTS</span></span>

### <span data-ttu-id="fa030-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="fa030-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="fa030-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fa030-136">NOTES</span></span>

## <span data-ttu-id="fa030-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fa030-137">RELATED LINKS</span></span>
