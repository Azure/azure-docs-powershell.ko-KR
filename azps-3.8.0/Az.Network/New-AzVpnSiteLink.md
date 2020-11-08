---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
ms.openlocfilehash: 68df4cd7dc1149b7bb62a148ff7c649ed2418db8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034477"
---
# <span data-ttu-id="7f514-101">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="7f514-101">New-AzVpnSiteLink</span></span>

## <span data-ttu-id="7f514-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f514-102">SYNOPSIS</span></span>
<span data-ttu-id="7f514-103">Azure VpnSiteLink 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7f514-103">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="7f514-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7f514-104">SYNTAX</span></span>

### <span data-ttu-id="7f514-105">ByVpnSiteLinkIpAddress</span><span class="sxs-lookup"><span data-stu-id="7f514-105">ByVpnSiteLinkIpAddress</span></span>
```
New-AzVpnSiteLink -Name <String> -IPAddress <String> [-LinkProviderName <String>] [-LinkSpeedInMbps <UInt32>]
 [-BGPAsn <UInt32>] [-BGPPeeringAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f514-106">ByVpnSiteLinkFqdn</span><span class="sxs-lookup"><span data-stu-id="7f514-106">ByVpnSiteLinkFqdn</span></span>
```
New-AzVpnSiteLink -Name <String> -Fqdn <String> [-LinkProviderName <String>] [-LinkSpeedInMbps <UInt32>]
 [-BGPAsn <UInt32>] [-BGPPeeringAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f514-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7f514-107">DESCRIPTION</span></span>
<span data-ttu-id="7f514-108">Azure VpnSiteLink 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7f514-108">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="7f514-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7f514-109">EXAMPLES</span></span>

### <span data-ttu-id="7f514-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7f514-110">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)
```

<span data-ttu-id="7f514-111">위의 작업을 통해 Azure의 "testRG" 리소스 그룹에 "VpnSiteLinks" 인 리소스 그룹, 가상 WAN 및 VpnSite를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7f514-111">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>

## <span data-ttu-id="7f514-112">변수</span><span class="sxs-lookup"><span data-stu-id="7f514-112">PARAMETERS</span></span>

### <span data-ttu-id="7f514-113">-BGPAsn</span><span class="sxs-lookup"><span data-stu-id="7f514-113">-BGPAsn</span></span>
<span data-ttu-id="7f514-114">이 VpnSiteLink의 BGP ASN입니다.</span><span class="sxs-lookup"><span data-stu-id="7f514-114">The BGP ASN for this VpnSiteLink.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f514-115">-BGPPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="7f514-115">-BGPPeeringAddress</span></span>
<span data-ttu-id="7f514-116">이 VpnSiteLink의 BGP 피어 링 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="7f514-116">The BGP Peering Address for this VpnSiteLink.</span></span>

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

### <span data-ttu-id="7f514-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f514-117">-DefaultProfile</span></span>
<span data-ttu-id="7f514-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7f514-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f514-119">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="7f514-119">-Fqdn</span></span>
<span data-ttu-id="7f514-120">다음 홉 Fqdn.</span><span class="sxs-lookup"><span data-stu-id="7f514-120">The Next Hop Fqdn.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteLinkFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f514-121">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="7f514-121">-IPAddress</span></span>
<span data-ttu-id="7f514-122">다음 홉 IpAddress.</span><span class="sxs-lookup"><span data-stu-id="7f514-122">The Next Hop IpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteLinkIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f514-123">-LinkProviderName</span><span class="sxs-lookup"><span data-stu-id="7f514-123">-LinkProviderName</span></span>
<span data-ttu-id="7f514-124">링크 공급자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f514-124">Link Provider Name.</span></span>

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

### <span data-ttu-id="7f514-125">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="7f514-125">-LinkSpeedInMbps</span></span>
<span data-ttu-id="7f514-126">연결 속도 (Mbps 단위)입니다.</span><span class="sxs-lookup"><span data-stu-id="7f514-126">Link Speed In Mbps.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f514-127">-이름</span><span class="sxs-lookup"><span data-stu-id="7f514-127">-Name</span></span>
<span data-ttu-id="7f514-128">성을</span><span class="sxs-lookup"><span data-stu-id="7f514-128">Name</span></span>

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

### <span data-ttu-id="7f514-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f514-129">CommonParameters</span></span>
<span data-ttu-id="7f514-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f514-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f514-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7f514-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f514-132">입력</span><span class="sxs-lookup"><span data-stu-id="7f514-132">INPUTS</span></span>

### <span data-ttu-id="7f514-133">않아야</span><span class="sxs-lookup"><span data-stu-id="7f514-133">None</span></span>

## <span data-ttu-id="7f514-134">출력</span><span class="sxs-lookup"><span data-stu-id="7f514-134">OUTPUTS</span></span>

### <span data-ttu-id="7f514-135">PSVpnSiteLink에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7f514-135">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="7f514-136">상속자</span><span class="sxs-lookup"><span data-stu-id="7f514-136">NOTES</span></span>

## <span data-ttu-id="7f514-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f514-137">RELATED LINKS</span></span>

[<span data-ttu-id="7f514-138">새로운 AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="7f514-138">New-AzVpnSite</span></span>](./New-AzVpnSite.md)