---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: 8dc88ab423c28abf1c68d18c22f6715c292bfadd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872329"
---
# <span data-ttu-id="c677b-101">Set-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="c677b-101">Set-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="c677b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c677b-102">SYNOPSIS</span></span>
<span data-ttu-id="c677b-103">Exchange 연결 정보를 설정 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c677b-103">Sets or updates the Exchange Connection information.</span></span> 

## <span data-ttu-id="c677b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c677b-104">SYNTAX</span></span>

### <span data-ttu-id="c677b-105">IPv6Address (기본값)</span><span class="sxs-lookup"><span data-stu-id="c677b-105">IPv6Address (Default)</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c677b-106">IPv4Address</span><span class="sxs-lookup"><span data-stu-id="c677b-106">IPv4Address</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c677b-107">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="c677b-107">Md5Authentication</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c677b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c677b-108">DESCRIPTION</span></span>
<span data-ttu-id="c677b-109">AzPeering와 함께 사용 되는 경우이는 메모리 내 작업 이므로만 유지 됩니다 `Update-AzPeering` .</span><span class="sxs-lookup"><span data-stu-id="c677b-109">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="c677b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c677b-110">EXAMPLES</span></span>

### <span data-ttu-id="c677b-111">Md5 해시 업데이트</span><span class="sxs-lookup"><span data-stu-id="c677b-111">Update Md5 Hash</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -MD5AuthenticationKey $hash
```

<span data-ttu-id="c677b-112">메모리에서 피어 링 개체의 첫 번째 연결에 대 한 Md5 해시를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c677b-112">Updates the Md5 Hash for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="c677b-113">Bgp 세션 주소 업데이트</span><span class="sxs-lookup"><span data-stu-id="c677b-113">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="c677b-114">메모리에서 피어 링 개체의 첫 번째 연결에 대 한 피어 링 주소를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c677b-114">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

## <span data-ttu-id="c677b-115">변수</span><span class="sxs-lookup"><span data-stu-id="c677b-115">PARAMETERS</span></span>

### <span data-ttu-id="c677b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c677b-116">-DefaultProfile</span></span>
<span data-ttu-id="c677b-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c677b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c677b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c677b-118">-InputObject</span></span>
<span data-ttu-id="c677b-119">Exchange 연결 개체</span><span class="sxs-lookup"><span data-stu-id="c677b-119">The exchange connection object</span></span>

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

### <span data-ttu-id="c677b-120">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="c677b-120">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="c677b-121">알려진 최대 IPv4</span><span class="sxs-lookup"><span data-stu-id="c677b-121">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="c677b-122">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="c677b-122">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="c677b-123">알려진 최대 IPv6</span><span class="sxs-lookup"><span data-stu-id="c677b-123">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="c677b-124">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="c677b-124">-MD5AuthenticationKey</span></span>
<span data-ttu-id="c677b-125">세션에 대 한 MD5 인증 키입니다.</span><span class="sxs-lookup"><span data-stu-id="c677b-125">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="c677b-126">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="c677b-126">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="c677b-127">피어 세션 IPv4 주소</span><span class="sxs-lookup"><span data-stu-id="c677b-127">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="c677b-128">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="c677b-128">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="c677b-129">피어 세션 IPv6 주소</span><span class="sxs-lookup"><span data-stu-id="c677b-129">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="c677b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c677b-130">CommonParameters</span></span>
<span data-ttu-id="c677b-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c677b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c677b-132">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c677b-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c677b-133">입력</span><span class="sxs-lookup"><span data-stu-id="c677b-133">INPUTS</span></span>

### <span data-ttu-id="c677b-134">PSExchangeConnection (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c677b-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="c677b-135">출력</span><span class="sxs-lookup"><span data-stu-id="c677b-135">OUTPUTS</span></span>

### <span data-ttu-id="c677b-136">PSExchangeConnection (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c677b-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="c677b-137">상속자</span><span class="sxs-lookup"><span data-stu-id="c677b-137">NOTES</span></span>

## <span data-ttu-id="c677b-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c677b-138">RELATED LINKS</span></span>
