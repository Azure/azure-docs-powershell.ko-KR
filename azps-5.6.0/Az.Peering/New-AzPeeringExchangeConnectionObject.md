---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: c4e57d3d7945f4ae06fc2461e660945bf7edfd6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989361"
---
# <span data-ttu-id="35fb2-101">New-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="35fb2-101">New-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="35fb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35fb2-102">SYNOPSIS</span></span>
<span data-ttu-id="35fb2-103">피어링을 만들거나 수정하는 데 사용할 메모리 내 PSObject를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35fb2-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="35fb2-104">구문</span><span class="sxs-lookup"><span data-stu-id="35fb2-104">SYNTAX</span></span>

### <span data-ttu-id="35fb2-105">IPv4Address(기본값)</span><span class="sxs-lookup"><span data-stu-id="35fb2-105">IPv4Address (Default)</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35fb2-106">IPv6Address</span><span class="sxs-lookup"><span data-stu-id="35fb2-106">IPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35fb2-107">IPv4AddressIPv6Address</span><span class="sxs-lookup"><span data-stu-id="35fb2-107">IPv4AddressIPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 -PeerSessionIPv6Address <String> [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>]
 [-MD5AuthenticationKey <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35fb2-108">설명</span><span class="sxs-lookup"><span data-stu-id="35fb2-108">DESCRIPTION</span></span>
<span data-ttu-id="35fb2-109">메모리 내 PSObject를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35fb2-109">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="35fb2-110">예제</span><span class="sxs-lookup"><span data-stu-id="35fb2-110">EXAMPLES</span></span>

### <span data-ttu-id="35fb2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="35fb2-111">Example 1</span></span>
```powershell
PS C:> $exconnection = New-AzPeeringExchangeConnectionObject -PeeringDBFacilityId 99999 -PeerSessionIPv4Address 10.3.151.99 -MaxPrefixesAdvertisedIPv4 20000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId     : 99999
PeerSessionIPv4Address  : 10.3.151.99
MaxPrefixesAdvertisedV4 : 20000
Md5AuthenticationKey    : 25234523452123411fd234qdwfas3234
```

<span data-ttu-id="35fb2-112">로컬 연결 개체</span><span class="sxs-lookup"><span data-stu-id="35fb2-112">Local connection object</span></span>

## <span data-ttu-id="35fb2-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="35fb2-113">PARAMETERS</span></span>

### <span data-ttu-id="35fb2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35fb2-114">-DefaultProfile</span></span>
<span data-ttu-id="35fb2-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="35fb2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35fb2-116">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="35fb2-116">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="35fb2-117">보급된 최대 IPv4</span><span class="sxs-lookup"><span data-stu-id="35fb2-117">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Address, IPv4AddressIPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35fb2-118">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="35fb2-118">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="35fb2-119">보급된 최대 IPv6</span><span class="sxs-lookup"><span data-stu-id="35fb2-119">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Address, IPv4AddressIPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35fb2-120">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="35fb2-120">-MD5AuthenticationKey</span></span>
<span data-ttu-id="35fb2-121">세션에 대한 MD5 인증 키입니다.</span><span class="sxs-lookup"><span data-stu-id="35fb2-121">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="35fb2-122">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="35fb2-122">-PeeringDBFacilityId</span></span>
<span data-ttu-id="35fb2-123">에 있는 피어링 시설 ID https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="35fb2-123">The peering facility Id found on https://peeringdb.com</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35fb2-124">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="35fb2-124">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="35fb2-125">피어 세션 IPv4 주소</span><span class="sxs-lookup"><span data-stu-id="35fb2-125">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Address, IPv4AddressIPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35fb2-126">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="35fb2-126">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="35fb2-127">피어 세션 IPv6 주소</span><span class="sxs-lookup"><span data-stu-id="35fb2-127">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Address, IPv4AddressIPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35fb2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35fb2-128">CommonParameters</span></span>
<span data-ttu-id="35fb2-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="35fb2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35fb2-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35fb2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35fb2-131">입력</span><span class="sxs-lookup"><span data-stu-id="35fb2-131">INPUTS</span></span>

### <span data-ttu-id="35fb2-132">없음</span><span class="sxs-lookup"><span data-stu-id="35fb2-132">None</span></span>

## <span data-ttu-id="35fb2-133">출력</span><span class="sxs-lookup"><span data-stu-id="35fb2-133">OUTPUTS</span></span>

### <span data-ttu-id="35fb2-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="35fb2-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="35fb2-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="35fb2-135">NOTES</span></span>

## <span data-ttu-id="35fb2-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35fb2-136">RELATED LINKS</span></span>
