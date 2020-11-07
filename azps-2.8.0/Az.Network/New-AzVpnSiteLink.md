---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
ms.openlocfilehash: 7e53c6828fa5c7bae40037f2fd64bb06ddf0be45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869798"
---
# <span data-ttu-id="aa87b-101">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="aa87b-101">New-AzVpnSiteLink</span></span>

## <span data-ttu-id="aa87b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa87b-102">SYNOPSIS</span></span>
<span data-ttu-id="aa87b-103">Azure VpnSiteLink 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aa87b-103">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="aa87b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aa87b-104">SYNTAX</span></span>

```
New-AzVpnSiteLink -Name <String> -IPAddress <String> [-LinkProviderName <String>] [-LinkSpeedInMbps <UInt32>]
 [-BGPAsn <UInt32>] [-BGPPeeringAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa87b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="aa87b-105">DESCRIPTION</span></span>
<span data-ttu-id="aa87b-106">Azure VpnSiteLink 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aa87b-106">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="aa87b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="aa87b-107">EXAMPLES</span></span>

### <span data-ttu-id="aa87b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="aa87b-108">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)
```

<span data-ttu-id="aa87b-109">위의 작업을 통해 Azure의 "testRG" 리소스 그룹에 "VpnSiteLinks" 인 리소스 그룹, 가상 WAN 및 VpnSite를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa87b-109">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>

## <span data-ttu-id="aa87b-110">변수</span><span class="sxs-lookup"><span data-stu-id="aa87b-110">PARAMETERS</span></span>

### <span data-ttu-id="aa87b-111">-BGPAsn</span><span class="sxs-lookup"><span data-stu-id="aa87b-111">-BGPAsn</span></span>
<span data-ttu-id="aa87b-112">이 VpnSiteLink의 BGP ASN입니다.</span><span class="sxs-lookup"><span data-stu-id="aa87b-112">The BGP ASN for this VpnSiteLink.</span></span>

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

### <span data-ttu-id="aa87b-113">-BGPPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="aa87b-113">-BGPPeeringAddress</span></span>
<span data-ttu-id="aa87b-114">이 VpnSiteLink의 BGP 피어 링 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="aa87b-114">The BGP Peering Address for this VpnSiteLink.</span></span>

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

### <span data-ttu-id="aa87b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa87b-115">-DefaultProfile</span></span>
<span data-ttu-id="aa87b-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aa87b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa87b-117">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="aa87b-117">-IPAddress</span></span>
<span data-ttu-id="aa87b-118">다음 홉 IpAddress.</span><span class="sxs-lookup"><span data-stu-id="aa87b-118">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="aa87b-119">-LinkProviderName</span><span class="sxs-lookup"><span data-stu-id="aa87b-119">-LinkProviderName</span></span>
<span data-ttu-id="aa87b-120">링크 공급자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa87b-120">Link Provider Name.</span></span>

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

### <span data-ttu-id="aa87b-121">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="aa87b-121">-LinkSpeedInMbps</span></span>
<span data-ttu-id="aa87b-122">연결 속도 (Mbps 단위)입니다.</span><span class="sxs-lookup"><span data-stu-id="aa87b-122">Link Speed In Mbps.</span></span>

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

### <span data-ttu-id="aa87b-123">-이름</span><span class="sxs-lookup"><span data-stu-id="aa87b-123">-Name</span></span>
<span data-ttu-id="aa87b-124">성을</span><span class="sxs-lookup"><span data-stu-id="aa87b-124">Name</span></span>

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

### <span data-ttu-id="aa87b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa87b-125">CommonParameters</span></span>
<span data-ttu-id="aa87b-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa87b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa87b-127">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="aa87b-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa87b-128">입력</span><span class="sxs-lookup"><span data-stu-id="aa87b-128">INPUTS</span></span>

### <span data-ttu-id="aa87b-129">않아야</span><span class="sxs-lookup"><span data-stu-id="aa87b-129">None</span></span>

## <span data-ttu-id="aa87b-130">출력</span><span class="sxs-lookup"><span data-stu-id="aa87b-130">OUTPUTS</span></span>

### <span data-ttu-id="aa87b-131">PSVpnSiteLink에 대 한.</span><span class="sxs-lookup"><span data-stu-id="aa87b-131">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="aa87b-132">상속자</span><span class="sxs-lookup"><span data-stu-id="aa87b-132">NOTES</span></span>

## <span data-ttu-id="aa87b-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa87b-133">RELATED LINKS</span></span>

[<span data-ttu-id="aa87b-134">새로운 AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="aa87b-134">New-AzVpnSite</span></span>](./New-AzVpnSite.md)