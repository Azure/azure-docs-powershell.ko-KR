---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: 3d58834dbd80549aed52104e84099544a427fa1d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212938"
---
# <span data-ttu-id="dfa8b-101">New-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="dfa8b-101">New-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="dfa8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfa8b-102">SYNOPSIS</span></span>
<span data-ttu-id="dfa8b-103">피어 링을 만들거나 수정 하는 데 사용할 메모리 PSObject를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dfa8b-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="dfa8b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dfa8b-104">SYNTAX</span></span>

### <span data-ttu-id="dfa8b-105">IPv4PrefixIPv6Prefix (기본값)</span><span class="sxs-lookup"><span data-stu-id="dfa8b-105">IPv4PrefixIPv6Prefix (Default)</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-SessionPrefixV4 <String>]
 [-SessionPrefixV6 <String>] -BandwidthInMbps <Int32> [-UseForPeeringService]
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfa8b-106">ParameterSetNameMicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="dfa8b-106">ParameterSetNameMicrosoftProvidedIPAddress</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-MicrosoftProvidedIPAddress]
 -BandwidthInMbps <Int32> [-UseForPeeringService] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dfa8b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="dfa8b-107">DESCRIPTION</span></span>
<span data-ttu-id="dfa8b-108">메모리 PSObject를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dfa8b-108">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="dfa8b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="dfa8b-109">EXAMPLES</span></span>

### <span data-ttu-id="dfa8b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="dfa8b-110">Example 1</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000 -SessionPrefixV4 192.168.1.0/31 -SessionPrefixV6 fe01::0/127 -MaxPrefixesAdvertisedIPv4 20000 -MaxPrefixesAdvertisedIPv6 2000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId    : 99999
UseForPeeringService   : False
SessionAddressProvider : Peer
SessionPrefixV4        : 192.168.1.0/31
ConnectionIdentifier   : 6d771cef-7169-4b0a-b028-c7270054bd31
SessionPrefixV6        : fe01::0/127
BandwidthInMbps        : 30000
Md5AuthenticationKey   : 25234523452123411fd234qdwfas3234
SessionStateV4         :
SessionStateV6         :
```

<span data-ttu-id="dfa8b-111">새 로컬 연결</span><span class="sxs-lookup"><span data-stu-id="dfa8b-111">New local connection</span></span>

### <span data-ttu-id="dfa8b-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="dfa8b-112">Example 2</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -MicrosoftProvidedIPAddress -BandwidthInMbps 30000 -UseForPeeringService

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 1de364bf-74ea-4088-ad17-bb79c16cfa81
BandwidthInMbps        : 30000
```

<span data-ttu-id="dfa8b-113">피어 링 서비스를 사용할 수 있는 직접적인 피어 링 연결 및 Microsoft 제공 IP 주소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dfa8b-113">Create direct peering connection with use for peering service enabled and Microsoft provided IP addresses</span></span>

### <span data-ttu-id="dfa8b-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="dfa8b-114">Example 3</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000 -SessionPrefixV4 192.168.1.0/31 -SessionPrefixV6 fe01::0/127 -UseForPeeringService

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Peer
SessionPrefixV4        : 192.168.1.0/31
ConnectionIdentifier   : 74ea6eab-5625-4170-a642-822e85d97566
SessionPrefixV6        : fe01::0/127
BandwidthInMbps        : 30000
SessionStateV4         :
SessionStateV6         :
```

<span data-ttu-id="dfa8b-115">피어 링 서비스를 사용 하 여 직접 피어 링 연결 만들기 및 피어 제공 IP 주소</span><span class="sxs-lookup"><span data-stu-id="dfa8b-115">Create direct peering connection with use for peering service enabled and peer provided IP Addresses</span></span>

### <span data-ttu-id="dfa8b-116">예제 4</span><span class="sxs-lookup"><span data-stu-id="dfa8b-116">Example 4</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000

PeeringDBFacilityId    : 99999
UseForPeeringService   : False
SessionAddressProvider : Peer
ConnectionIdentifier   : 920f128a-c9d8-4514-a2e0-c533ab1a550c
BandwidthInMbps        : 30000
```

<span data-ttu-id="dfa8b-117">Bgp 세션 IP 주소 없이 직접 피어 링 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dfa8b-117">Create direct peering connection without bgp session IP addresses.</span></span> <span data-ttu-id="dfa8b-118">피어는 bgp 세션을 구성할 수 있으려면 먼저 IP 주소를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfa8b-118">The peer will have to set the IP addresses before the bgp session can be configured.</span></span>

## <span data-ttu-id="dfa8b-119">변수</span><span class="sxs-lookup"><span data-stu-id="dfa8b-119">PARAMETERS</span></span>

### <span data-ttu-id="dfa8b-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="dfa8b-120">-BandwidthInMbps</span></span>
<span data-ttu-id="dfa8b-121">이 위치에서 제공 되는 대역폭 (Mbps 단위)입니다.</span><span class="sxs-lookup"><span data-stu-id="dfa8b-121">The Bandwidth offered at this location in Mbps.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfa8b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfa8b-122">-DefaultProfile</span></span>
<span data-ttu-id="dfa8b-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dfa8b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfa8b-124">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="dfa8b-124">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="dfa8b-125">알려진 최대 IPv4</span><span class="sxs-lookup"><span data-stu-id="dfa8b-125">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfa8b-126">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="dfa8b-126">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="dfa8b-127">알려진 최대 IPv6</span><span class="sxs-lookup"><span data-stu-id="dfa8b-127">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfa8b-128">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="dfa8b-128">-MD5AuthenticationKey</span></span>
<span data-ttu-id="dfa8b-129">세션에 대 한 MD5 인증 키입니다.</span><span class="sxs-lookup"><span data-stu-id="dfa8b-129">The MD5 authentication key for session.</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfa8b-130">-MicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="dfa8b-130">-MicrosoftProvidedIPAddress</span></span>
<span data-ttu-id="dfa8b-131">Microsoft에 BGP 세션 주소를 제공 하도록 알리는 플래그를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfa8b-131">Enable flag that tells Microsoft to provide the BGP session addresses.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ParameterSetNameMicrosoftProvidedIPAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfa8b-132">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="dfa8b-132">-PeeringDBFacilityId</span></span>
<span data-ttu-id="dfa8b-133">에서 찾은 피어 링 기능 Id https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="dfa8b-133">The peering facility Id found on https://peeringdb.com</span></span>

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

### <span data-ttu-id="dfa8b-134">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="dfa8b-134">-SessionPrefixV4</span></span>
<span data-ttu-id="dfa8b-135">피어 세션 IPv4 주소</span><span class="sxs-lookup"><span data-stu-id="dfa8b-135">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfa8b-136">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="dfa8b-136">-SessionPrefixV6</span></span>
<span data-ttu-id="dfa8b-137">피어 세션 IPv6 주소</span><span class="sxs-lookup"><span data-stu-id="dfa8b-137">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfa8b-138">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="dfa8b-138">-UseForPeeringService</span></span>
<span data-ttu-id="dfa8b-139">MPS (Microsoft 피어 링 서비스)에 사용할 수 있도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfa8b-139">Enable for use with Microsoft Peering Service (MPS).</span></span>

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

### <span data-ttu-id="dfa8b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfa8b-140">CommonParameters</span></span>
<span data-ttu-id="dfa8b-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfa8b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfa8b-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dfa8b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfa8b-143">입력</span><span class="sxs-lookup"><span data-stu-id="dfa8b-143">INPUTS</span></span>

### <span data-ttu-id="dfa8b-144">않아야</span><span class="sxs-lookup"><span data-stu-id="dfa8b-144">None</span></span>

## <span data-ttu-id="dfa8b-145">출력</span><span class="sxs-lookup"><span data-stu-id="dfa8b-145">OUTPUTS</span></span>

### <span data-ttu-id="dfa8b-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="dfa8b-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="dfa8b-147">상속자</span><span class="sxs-lookup"><span data-stu-id="dfa8b-147">NOTES</span></span>

## <span data-ttu-id="dfa8b-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dfa8b-148">RELATED LINKS</span></span>
