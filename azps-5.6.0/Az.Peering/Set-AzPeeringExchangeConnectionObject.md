---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/set-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: d935f980b776ad6f61fe705a14e0da2a375d1e1e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989212"
---
# <span data-ttu-id="ef9de-101">Set-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="ef9de-101">Set-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="ef9de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef9de-102">SYNOPSIS</span></span>
<span data-ttu-id="ef9de-103">Exchange 연결 정보를 설정하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9de-103">Sets or updates the Exchange Connection information.</span></span> 

## <span data-ttu-id="ef9de-104">구문</span><span class="sxs-lookup"><span data-stu-id="ef9de-104">SYNTAX</span></span>

### <span data-ttu-id="ef9de-105">IPv4Address(기본값)</span><span class="sxs-lookup"><span data-stu-id="ef9de-105">IPv4Address (Default)</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef9de-106">IPv6Address</span><span class="sxs-lookup"><span data-stu-id="ef9de-106">IPv6Address</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef9de-107">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="ef9de-107">Md5Authentication</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef9de-108">설명</span><span class="sxs-lookup"><span data-stu-id="ef9de-108">DESCRIPTION</span></span>
<span data-ttu-id="ef9de-109">Update-AzPeering과 함께 사용되는 이 작업은 메모리 내 작업으로 에서만 `Update-AzPeering` 지속됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef9de-109">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="ef9de-110">예제</span><span class="sxs-lookup"><span data-stu-id="ef9de-110">EXAMPLES</span></span>

### <span data-ttu-id="ef9de-111">Md5 해시 업데이트</span><span class="sxs-lookup"><span data-stu-id="ef9de-111">Update Md5 Hash</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -MD5AuthenticationKey $hash
```

<span data-ttu-id="ef9de-112">메모리의 피어링 개체의 첫 번째 연결에 대해 Md5 해시를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9de-112">Updates the Md5 Hash for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="ef9de-113">Bgp 세션 주소 업데이트</span><span class="sxs-lookup"><span data-stu-id="ef9de-113">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="ef9de-114">메모리의 피어링 개체의 첫 번째 연결에 대한 피어링 주소를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9de-114">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

## <span data-ttu-id="ef9de-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ef9de-115">PARAMETERS</span></span>

### <span data-ttu-id="ef9de-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef9de-116">-DefaultProfile</span></span>
<span data-ttu-id="ef9de-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ef9de-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef9de-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef9de-118">-InputObject</span></span>
<span data-ttu-id="ef9de-119">Exchange 연결 개체</span><span class="sxs-lookup"><span data-stu-id="ef9de-119">The exchange connection object</span></span>

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

### <span data-ttu-id="ef9de-120">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="ef9de-120">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="ef9de-121">보급된 최대 IPv4</span><span class="sxs-lookup"><span data-stu-id="ef9de-121">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="ef9de-122">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="ef9de-122">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="ef9de-123">보급된 최대 IPv6</span><span class="sxs-lookup"><span data-stu-id="ef9de-123">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="ef9de-124">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="ef9de-124">-MD5AuthenticationKey</span></span>
<span data-ttu-id="ef9de-125">세션에 대한 MD5 인증 키입니다.</span><span class="sxs-lookup"><span data-stu-id="ef9de-125">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="ef9de-126">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="ef9de-126">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="ef9de-127">피어 세션 IPv4 주소</span><span class="sxs-lookup"><span data-stu-id="ef9de-127">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="ef9de-128">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="ef9de-128">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="ef9de-129">피어 세션 IPv6 주소</span><span class="sxs-lookup"><span data-stu-id="ef9de-129">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="ef9de-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef9de-130">CommonParameters</span></span>
<span data-ttu-id="ef9de-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ef9de-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef9de-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef9de-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef9de-133">입력</span><span class="sxs-lookup"><span data-stu-id="ef9de-133">INPUTS</span></span>

### <span data-ttu-id="ef9de-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="ef9de-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="ef9de-135">출력</span><span class="sxs-lookup"><span data-stu-id="ef9de-135">OUTPUTS</span></span>

### <span data-ttu-id="ef9de-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="ef9de-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="ef9de-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ef9de-137">NOTES</span></span>

## <span data-ttu-id="ef9de-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef9de-138">RELATED LINKS</span></span>
