---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: 0b72cd501f9e003e39fc3dd4f4e90bbd85331180
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384623"
---
# <span data-ttu-id="c0064-101">Set-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="c0064-101">Set-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="c0064-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0064-102">SYNOPSIS</span></span>
<span data-ttu-id="c0064-103">직접 연결 정보를 설정하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c0064-103">Sets or updates the Direct Connection information.</span></span> 

## <span data-ttu-id="c0064-104">구문</span><span class="sxs-lookup"><span data-stu-id="c0064-104">SYNTAX</span></span>

### <span data-ttu-id="c0064-105">대역폭(기본값)</span><span class="sxs-lookup"><span data-stu-id="c0064-105">Bandwidth (Default)</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -BandwidthInMbps <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0064-106">IPv4Prefix</span><span class="sxs-lookup"><span data-stu-id="c0064-106">IPv4Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV4 <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0064-107">IPv6Prefix</span><span class="sxs-lookup"><span data-stu-id="c0064-107">IPv6Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV6 <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0064-108">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="c0064-108">Md5Authentication</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0064-109">ParameterSetNameUseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="c0064-109">ParameterSetNameUseForPeeringService</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -UseForPeeringService <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0064-110">설명</span><span class="sxs-lookup"><span data-stu-id="c0064-110">DESCRIPTION</span></span>
<span data-ttu-id="c0064-111">Update-AzPeering과 함께 사용하며 메모리 내 작업으로, 에서만 `Update-AzPeering` 지속됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0064-111">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="c0064-112">예제</span><span class="sxs-lookup"><span data-stu-id="c0064-112">EXAMPLES</span></span>

### <span data-ttu-id="c0064-113">업그레이드 대역폭</span><span class="sxs-lookup"><span data-stu-id="c0064-113">Upgrade Bandwidth</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -BandwidthInMbps 30000
```

<span data-ttu-id="c0064-114">메모리의 피어링 개체에서 첫 번째 연결에 대한 대역폭을 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="c0064-114">Upgrades the bandwidth for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="c0064-115">Bgp 세션 주소 업데이트</span><span class="sxs-lookup"><span data-stu-id="c0064-115">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -SessionPrefixV4 "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="c0064-116">메모리의 피어링 개체에서 첫 번째 연결에 대한 피어링 주소를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c0064-116">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="c0064-117">피어링 서비스에 대한 업데이트 사용</span><span class="sxs-lookup"><span data-stu-id="c0064-117">Update Use for peering service</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -UseForPeeringService $true

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 16c24fd5-89aa-48d7-a101-38ca68a4ce6d
BandwidthInMbps        : 30000
```

<span data-ttu-id="c0064-118">피어링 서비스에서 사용할 연결을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c0064-118">Updates the connection for use with peering service</span></span>

## <span data-ttu-id="c0064-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0064-119">PARAMETERS</span></span>

### <span data-ttu-id="c0064-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="c0064-120">-BandwidthInMbps</span></span>
<span data-ttu-id="c0064-121">이 위치에서 제공되는 대역폭(Mbps)입니다.</span><span class="sxs-lookup"><span data-stu-id="c0064-121">The Bandwidth offered at this location in Mbps.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Bandwidth
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0064-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0064-122">-DefaultProfile</span></span>
<span data-ttu-id="c0064-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c0064-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0064-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0064-124">-InputObject</span></span>
<span data-ttu-id="c0064-125">직접 연결 개체</span><span class="sxs-lookup"><span data-stu-id="c0064-125">The direct connection Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0064-126">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="c0064-126">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="c0064-127">보급된 최대 IPv4</span><span class="sxs-lookup"><span data-stu-id="c0064-127">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0064-128">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="c0064-128">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="c0064-129">보급된 최대 IPv6</span><span class="sxs-lookup"><span data-stu-id="c0064-129">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0064-130">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="c0064-130">-MD5AuthenticationKey</span></span>
<span data-ttu-id="c0064-131">세션에 대한 MD5 인증 키입니다.</span><span class="sxs-lookup"><span data-stu-id="c0064-131">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="c0064-132">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="c0064-132">-SessionPrefixV4</span></span>
<span data-ttu-id="c0064-133">피어 세션 IPv4 주소</span><span class="sxs-lookup"><span data-stu-id="c0064-133">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Prefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0064-134">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="c0064-134">-SessionPrefixV6</span></span>
<span data-ttu-id="c0064-135">피어 세션 IPv6 주소</span><span class="sxs-lookup"><span data-stu-id="c0064-135">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Prefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0064-136">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="c0064-136">-UseForPeeringService</span></span>
<span data-ttu-id="c0064-137">Microsoft MPS(피어링 서비스)에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0064-137">Enable for use with Microsoft Peering Service (MPS).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: ParameterSetNameUseForPeeringService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0064-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0064-138">CommonParameters</span></span>
<span data-ttu-id="c0064-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c0064-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0064-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c0064-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0064-141">입력</span><span class="sxs-lookup"><span data-stu-id="c0064-141">INPUTS</span></span>

### <span data-ttu-id="c0064-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDectConnection</span><span class="sxs-lookup"><span data-stu-id="c0064-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="c0064-143">출력</span><span class="sxs-lookup"><span data-stu-id="c0064-143">OUTPUTS</span></span>

### <span data-ttu-id="c0064-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDectConnection</span><span class="sxs-lookup"><span data-stu-id="c0064-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="c0064-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c0064-145">NOTES</span></span>

## <span data-ttu-id="c0064-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0064-146">RELATED LINKS</span></span>
