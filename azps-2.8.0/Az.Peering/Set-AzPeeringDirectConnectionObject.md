---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: ca9235ddfb4b16b80cd0df9ad61bd6936672b889
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872346"
---
# <span data-ttu-id="3047e-101">Set-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="3047e-101">Set-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="3047e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3047e-102">SYNOPSIS</span></span>
<span data-ttu-id="3047e-103">직접 연결 정보를 설정 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3047e-103">Sets or updates the Direct Connection information.</span></span> 

## <span data-ttu-id="3047e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3047e-104">SYNTAX</span></span>

### <span data-ttu-id="3047e-105">대역폭 (기본값)</span><span class="sxs-lookup"><span data-stu-id="3047e-105">Bandwidth (Default)</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -BandwidthInMbps <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3047e-106">IPv4Prefix</span><span class="sxs-lookup"><span data-stu-id="3047e-106">IPv4Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV4 <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3047e-107">IPv6Prefix</span><span class="sxs-lookup"><span data-stu-id="3047e-107">IPv6Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV6 <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3047e-108">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="3047e-108">Md5Authentication</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3047e-109">ParameterSetNameUseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="3047e-109">ParameterSetNameUseForPeeringService</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -UseForPeeringService <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3047e-110">설명은</span><span class="sxs-lookup"><span data-stu-id="3047e-110">DESCRIPTION</span></span>
<span data-ttu-id="3047e-111">AzPeering와 함께 사용 되는 경우이는 메모리 내 작업 이므로만 유지 됩니다 `Update-AzPeering` .</span><span class="sxs-lookup"><span data-stu-id="3047e-111">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="3047e-112">예제의</span><span class="sxs-lookup"><span data-stu-id="3047e-112">EXAMPLES</span></span>

### <span data-ttu-id="3047e-113">대역폭 업그레이드</span><span class="sxs-lookup"><span data-stu-id="3047e-113">Upgrade Bandwidth</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -BandwidthInMbps 30000
```

<span data-ttu-id="3047e-114">메모리에서 피어 링 개체의 첫 번째 연결에 대 한 대역폭을 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="3047e-114">Upgrades the bandwidth for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="3047e-115">Bgp 세션 주소 업데이트</span><span class="sxs-lookup"><span data-stu-id="3047e-115">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -SessionPrefixV4 "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="3047e-116">메모리에서 피어 링 개체의 첫 번째 연결에 대 한 피어 링 주소를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3047e-116">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="3047e-117">피어 링 서비스에 대 한 업데이트 사용</span><span class="sxs-lookup"><span data-stu-id="3047e-117">Update Use for peering service</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -UseForPeeringService $true

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 16c24fd5-89aa-48d7-a101-38ca68a4ce6d
BandwidthInMbps        : 30000
```

<span data-ttu-id="3047e-118">피어 링 서비스에 사용 하기 위해 연결을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3047e-118">Updates the connection for use with peering service</span></span>

## <span data-ttu-id="3047e-119">변수</span><span class="sxs-lookup"><span data-stu-id="3047e-119">PARAMETERS</span></span>

### <span data-ttu-id="3047e-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="3047e-120">-BandwidthInMbps</span></span>
<span data-ttu-id="3047e-121">이 위치에서 제공 되는 대역폭 (Mbps 단위)입니다.</span><span class="sxs-lookup"><span data-stu-id="3047e-121">The Bandwidth offered at this location in Mbps.</span></span>

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

### <span data-ttu-id="3047e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3047e-122">-DefaultProfile</span></span>
<span data-ttu-id="3047e-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3047e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3047e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3047e-124">-InputObject</span></span>
<span data-ttu-id="3047e-125">직접 연결 개체</span><span class="sxs-lookup"><span data-stu-id="3047e-125">The direct connection Object</span></span>

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

### <span data-ttu-id="3047e-126">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="3047e-126">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="3047e-127">알려진 최대 IPv4</span><span class="sxs-lookup"><span data-stu-id="3047e-127">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="3047e-128">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="3047e-128">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="3047e-129">알려진 최대 IPv6</span><span class="sxs-lookup"><span data-stu-id="3047e-129">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="3047e-130">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="3047e-130">-MD5AuthenticationKey</span></span>
<span data-ttu-id="3047e-131">세션에 대 한 MD5 인증 키입니다.</span><span class="sxs-lookup"><span data-stu-id="3047e-131">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="3047e-132">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="3047e-132">-SessionPrefixV4</span></span>
<span data-ttu-id="3047e-133">피어 세션 IPv4 주소</span><span class="sxs-lookup"><span data-stu-id="3047e-133">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="3047e-134">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="3047e-134">-SessionPrefixV6</span></span>
<span data-ttu-id="3047e-135">피어 세션 IPv6 주소</span><span class="sxs-lookup"><span data-stu-id="3047e-135">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="3047e-136">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="3047e-136">-UseForPeeringService</span></span>
<span data-ttu-id="3047e-137">MPS (Microsoft 피어 링 서비스)에 사용할 수 있도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3047e-137">Enable for use with Microsoft Peering Service (MPS).</span></span>

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

### <span data-ttu-id="3047e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3047e-138">CommonParameters</span></span>
<span data-ttu-id="3047e-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3047e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3047e-140">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3047e-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3047e-141">입력</span><span class="sxs-lookup"><span data-stu-id="3047e-141">INPUTS</span></span>

### <span data-ttu-id="3047e-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="3047e-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="3047e-143">출력</span><span class="sxs-lookup"><span data-stu-id="3047e-143">OUTPUTS</span></span>

### <span data-ttu-id="3047e-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="3047e-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="3047e-145">상속자</span><span class="sxs-lookup"><span data-stu-id="3047e-145">NOTES</span></span>

## <span data-ttu-id="3047e-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3047e-146">RELATED LINKS</span></span>
