---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: 9f4ceb2ac0bc84198e7fcfb71114c12e48a5616e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189372"
---
# <span data-ttu-id="0885e-101">Set-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="0885e-101">Set-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="0885e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0885e-102">SYNOPSIS</span></span>
<span data-ttu-id="0885e-103">Exchange 연결 정보를 설정하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0885e-103">Sets or updates the Exchange Connection information.</span></span> 

## <span data-ttu-id="0885e-104">구문</span><span class="sxs-lookup"><span data-stu-id="0885e-104">SYNTAX</span></span>

### <span data-ttu-id="0885e-105">IPv4Address(기본값)</span><span class="sxs-lookup"><span data-stu-id="0885e-105">IPv4Address (Default)</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0885e-106">IPv6Address</span><span class="sxs-lookup"><span data-stu-id="0885e-106">IPv6Address</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0885e-107">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="0885e-107">Md5Authentication</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0885e-108">설명</span><span class="sxs-lookup"><span data-stu-id="0885e-108">DESCRIPTION</span></span>
<span data-ttu-id="0885e-109">Update-AzPeering과 함께 사용하며 메모리 내 작업으로, 에서만 `Update-AzPeering` 지속됩니다.</span><span class="sxs-lookup"><span data-stu-id="0885e-109">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="0885e-110">예제</span><span class="sxs-lookup"><span data-stu-id="0885e-110">EXAMPLES</span></span>

### <span data-ttu-id="0885e-111">Md5 해시 업데이트</span><span class="sxs-lookup"><span data-stu-id="0885e-111">Update Md5 Hash</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -MD5AuthenticationKey $hash
```

<span data-ttu-id="0885e-112">메모리의 피어링 개체에서 첫 번째 연결에 대한 Md5 해시를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0885e-112">Updates the Md5 Hash for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="0885e-113">Bgp 세션 주소 업데이트</span><span class="sxs-lookup"><span data-stu-id="0885e-113">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="0885e-114">메모리의 피어링 개체에서 첫 번째 연결에 대한 피어링 주소를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0885e-114">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

## <span data-ttu-id="0885e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0885e-115">PARAMETERS</span></span>

### <span data-ttu-id="0885e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0885e-116">-DefaultProfile</span></span>
<span data-ttu-id="0885e-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0885e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0885e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0885e-118">-InputObject</span></span>
<span data-ttu-id="0885e-119">Exchange 연결 개체</span><span class="sxs-lookup"><span data-stu-id="0885e-119">The exchange connection object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0885e-120">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="0885e-120">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="0885e-121">보급된 최대 IPv4</span><span class="sxs-lookup"><span data-stu-id="0885e-121">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0885e-122">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="0885e-122">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="0885e-123">보급된 최대 IPv6</span><span class="sxs-lookup"><span data-stu-id="0885e-123">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0885e-124">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="0885e-124">-MD5AuthenticationKey</span></span>
<span data-ttu-id="0885e-125">세션에 대한 MD5 인증 키입니다.</span><span class="sxs-lookup"><span data-stu-id="0885e-125">The MD5 authentication key for session.</span></span>

```yaml
Type: System.String
Parameter Sets: Md5Authentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0885e-126">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="0885e-126">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="0885e-127">피어 세션 IPv4 주소</span><span class="sxs-lookup"><span data-stu-id="0885e-127">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0885e-128">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="0885e-128">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="0885e-129">피어 세션 IPv6 주소</span><span class="sxs-lookup"><span data-stu-id="0885e-129">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0885e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0885e-130">CommonParameters</span></span>
<span data-ttu-id="0885e-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0885e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0885e-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0885e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0885e-133">입력</span><span class="sxs-lookup"><span data-stu-id="0885e-133">INPUTS</span></span>

### <span data-ttu-id="0885e-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="0885e-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="0885e-135">출력</span><span class="sxs-lookup"><span data-stu-id="0885e-135">OUTPUTS</span></span>

### <span data-ttu-id="0885e-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="0885e-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="0885e-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0885e-137">NOTES</span></span>

## <span data-ttu-id="0885e-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0885e-138">RELATED LINKS</span></span>
