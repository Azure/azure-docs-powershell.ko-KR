---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermipsecpolicy
schema: 2.0.0
ms.openlocfilehash: 642284e7e1aa732983ee660ea323707be030b640
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881366"
---
# <span data-ttu-id="f4707-101">New-AzureRmIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="f4707-101">New-AzureRmIpsecPolicy</span></span>

## <span data-ttu-id="f4707-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4707-102">SYNOPSIS</span></span>
<span data-ttu-id="f4707-103">IPSec 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f4707-103">Creates an IPSec Policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4707-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f4707-104">SYNTAX</span></span>

```
New-AzureRmIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4707-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f4707-105">DESCRIPTION</span></span>
<span data-ttu-id="f4707-106">New-AzureRmIpsecPolicy cmdlet은 가상 네트워크 게이트웨이 연결에 사용 되는 IPSec 정책 제안을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f4707-106">The New-AzureRmIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="f4707-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f4707-107">EXAMPLES</span></span>

### <span data-ttu-id="f4707-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f4707-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzureRmIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="f4707-109">새 가상 네트워크 게이트웨이 연결에 사용할 IPSec 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="f4707-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="f4707-110">변수</span><span class="sxs-lookup"><span data-stu-id="f4707-110">PARAMETERS</span></span>

### <span data-ttu-id="f4707-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4707-111">-DefaultProfile</span></span>
<span data-ttu-id="f4707-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f4707-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4707-113">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="f4707-113">-DhGroup</span></span>
<span data-ttu-id="f4707-114">IKE 단계 1에서 초기 SA 용으로 사용 되는 DH 그룹</span><span class="sxs-lookup"><span data-stu-id="f4707-114">The DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, DHGroup1, DHGroup14, DHGroup2, DHGroup2048, DHGroup24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4707-115">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="f4707-115">-IkeEncryption</span></span>
<span data-ttu-id="f4707-116">IKE 암호화 알고리즘 (IKE 단계 2)</span><span class="sxs-lookup"><span data-stu-id="f4707-116">The IKE encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: DES, DES3, AES128, AES192, AES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4707-117">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="f4707-117">-IkeIntegrity</span></span>
<span data-ttu-id="f4707-118">IKE 무결성 알고리즘 (IKE 단계 2)</span><span class="sxs-lookup"><span data-stu-id="f4707-118">The IKE integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: MD5, SHA1, SHA256, SHA384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4707-119">-암호 암호화</span><span class="sxs-lookup"><span data-stu-id="f4707-119">-IpsecEncryption</span></span>
<span data-ttu-id="f4707-120">IPSec 암호화 알고리즘 (IKE 단계 1)</span><span class="sxs-lookup"><span data-stu-id="f4707-120">The IPSec encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, DES, DES3, AES128, AES192, AES256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4707-121">-계층 무결성</span><span class="sxs-lookup"><span data-stu-id="f4707-121">-IpsecIntegrity</span></span>
<span data-ttu-id="f4707-122">IPSec 무결성 알고리즘 (IKE 단계 1)</span><span class="sxs-lookup"><span data-stu-id="f4707-122">The IPSec integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: MD5, SHA1, SHA256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4707-123">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="f4707-123">-PfsGroup</span></span>
<span data-ttu-id="f4707-124">새 자식 SA에 대 한 IKE 단계 2에 사용 되는 DH 그룹</span><span class="sxs-lookup"><span data-stu-id="f4707-124">The DH Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, PFS1, PFS2, PFS2048, PFS24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4707-125">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="f4707-125">-SADataSizeKilobytes</span></span>
<span data-ttu-id="f4707-126">IPSec 보안 연결 (빠른 모드 또는 2 단계 SA 라고도 함) 페이로드 크기 (KB)</span><span class="sxs-lookup"><span data-stu-id="f4707-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4707-127">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="f4707-127">-SALifeTimeSeconds</span></span>
<span data-ttu-id="f4707-128">IPSec 보안 연결 (빠른 모드 또는 2 단계 SA 라고도 함) 수명 (초)</span><span class="sxs-lookup"><span data-stu-id="f4707-128">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4707-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4707-129">CommonParameters</span></span>
<span data-ttu-id="f4707-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4707-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4707-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4707-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4707-132">입력</span><span class="sxs-lookup"><span data-stu-id="f4707-132">INPUTS</span></span>

### <span data-ttu-id="f4707-133">않아야</span><span class="sxs-lookup"><span data-stu-id="f4707-133">None</span></span>

## <span data-ttu-id="f4707-134">출력</span><span class="sxs-lookup"><span data-stu-id="f4707-134">OUTPUTS</span></span>

### <span data-ttu-id="f4707-135">PSIpsecPolicy에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f4707-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="f4707-136">상속자</span><span class="sxs-lookup"><span data-stu-id="f4707-136">NOTES</span></span>

## <span data-ttu-id="f4707-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f4707-137">RELATED LINKS</span></span>

