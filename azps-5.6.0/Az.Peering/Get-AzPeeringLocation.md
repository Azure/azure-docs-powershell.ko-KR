---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
ms.openlocfilehash: a4367087bd248589f3345c14f6c7681be5eae9ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989585"
---
# <span data-ttu-id="aa03e-101">Get-AzPeeringLocation</span><span class="sxs-lookup"><span data-stu-id="aa03e-101">Get-AzPeeringLocation</span></span>

## <span data-ttu-id="aa03e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa03e-102">SYNOPSIS</span></span>
<span data-ttu-id="aa03e-103">Microsoft에서 제공하는 피어링 위치를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aa03e-103">Gets the Peering locations offered by Microsoft</span></span>

## <span data-ttu-id="aa03e-104">구문</span><span class="sxs-lookup"><span data-stu-id="aa03e-104">SYNTAX</span></span>

### <span data-ttu-id="aa03e-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="aa03e-105">Default (Default)</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aa03e-106">LocationByFacilityId</span><span class="sxs-lookup"><span data-stu-id="aa03e-106">LocationByFacilityId</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringDbFacilityId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa03e-107">LocationByDirectType</span><span class="sxs-lookup"><span data-stu-id="aa03e-107">LocationByDirectType</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DirectPeeringType <String>]
 [-PeeringDbFacilityId <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa03e-108">설명</span><span class="sxs-lookup"><span data-stu-id="aa03e-108">DESCRIPTION</span></span>
<span data-ttu-id="aa03e-109">사용자가 사용자와 연결할 수 있는 피어링 ARM.</span><span class="sxs-lookup"><span data-stu-id="aa03e-109">Gets the Peering Facilities where users can connect with ARM.</span></span>

## <span data-ttu-id="aa03e-110">예제</span><span class="sxs-lookup"><span data-stu-id="aa03e-110">EXAMPLES</span></span>

### <span data-ttu-id="aa03e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="aa03e-111">Example 1</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Direct

#...More above
PeeringLocation       : Dublin
Address               : Unit 2, North West Business Park
Country               : IE
PeeringDBFacilityId   : 1065
PeeringDBFacilityLink : https://www.peeringdb.com/fac/1065
BandwidthOffers       : {10Gbps, 100Gbps}

PeeringLocation       : Frankfurt
Address               : Hanauer Landstrasse 298
Country               : DE
PeeringDBFacilityId   : 58
PeeringDBFacilityLink : https://www.peeringdb.com/fac/58
BandwidthOffers       : {10Gbps, 100Gbps}
#...More below
```

<span data-ttu-id="aa03e-112">위치의 긴 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="aa03e-112">Its a long list of locations.</span></span> <span data-ttu-id="aa03e-113">모든 직접 피어링 시설을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aa03e-113">Gets the all the Direct Peering Facilities.</span></span>

### <span data-ttu-id="aa03e-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="aa03e-114">Example 2</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Exchange -PeeringLocation "Honolulu" 

ExchangeName          : DRF IX
PeeringLocation       : Honolulu
Country               : US
PeeringDBFacilityId   : 267
PeeringDBFacilityLink : https://www.peeringdb.com/ix/267
MicrosoftIPv4Address  : 206.197.210.37
MicrosoftIPv6Address  : 2606:7c80:3375:50::37
FacilityIPv4Prefix    : 206.197.210.0/24
FacilityIPv6Prefix    : 2606:7c80:3375:50::/64
```

<span data-ttu-id="aa03e-115">Honolulu에 대한 Exchange 피어링 위치를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aa03e-115">Gets the exchange peering location for Honolulu.</span></span> 

### <span data-ttu-id="aa03e-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="aa03e-116">Example 3</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Exchange -PeeringDbFacilityId 71 

ExchangeName          : NIX.CZ
PeeringLocation       : Prague
Country               : CZ
PeeringDBFacilityId   : 71
PeeringDBFacilityLink : https://www.peeringdb.com/ix/71
MicrosoftIPv4Address  : 91.210.16.115
MicrosoftIPv6Address  : 2001:7f8:14::6b:1
FacilityIPv4Prefix    : 91.210.16.0/22
FacilityIPv6Prefix    : 2001:7f8:14::/64
```

<span data-ttu-id="aa03e-117">피어링 시설 ID 71에 대한 교환 피어링 위치를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aa03e-117">Gets the exchange peering location for peering facility id 71.</span></span> 

## <span data-ttu-id="aa03e-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="aa03e-118">PARAMETERS</span></span>

### <span data-ttu-id="aa03e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa03e-119">-DefaultProfile</span></span>
<span data-ttu-id="aa03e-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aa03e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa03e-121">-DirectPeeringType</span><span class="sxs-lookup"><span data-stu-id="aa03e-121">-DirectPeeringType</span></span>
<span data-ttu-id="aa03e-122">'Edge', 'CDN', 'Transit'을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="aa03e-122">Select 'Edge', 'CDN', and 'Transit'.</span></span>

```yaml
Type: System.String
Parameter Sets: LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa03e-123">-Kind</span><span class="sxs-lookup"><span data-stu-id="aa03e-123">-Kind</span></span>
<span data-ttu-id="aa03e-124">종류에 따라 모든 피어링 리소스를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="aa03e-124">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa03e-125">-PeeringDbFacilityId</span><span class="sxs-lookup"><span data-stu-id="aa03e-125">-PeeringDbFacilityId</span></span>
<span data-ttu-id="aa03e-126">PeeringDB.com 시설 ID</span><span class="sxs-lookup"><span data-stu-id="aa03e-126">The PeeringDB.com Facility ID</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: LocationByFacilityId, LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa03e-127">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="aa03e-127">-PeeringLocation</span></span>
<span data-ttu-id="aa03e-128">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="aa03e-128">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa03e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa03e-129">CommonParameters</span></span>
<span data-ttu-id="aa03e-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aa03e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa03e-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa03e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa03e-132">입력</span><span class="sxs-lookup"><span data-stu-id="aa03e-132">INPUTS</span></span>

### <span data-ttu-id="aa03e-133">없음</span><span class="sxs-lookup"><span data-stu-id="aa03e-133">None</span></span>

## <span data-ttu-id="aa03e-134">출력</span><span class="sxs-lookup"><span data-stu-id="aa03e-134">OUTPUTS</span></span>

### <span data-ttu-id="aa03e-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringLocation</span><span class="sxs-lookup"><span data-stu-id="aa03e-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringLocation</span></span>

## <span data-ttu-id="aa03e-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aa03e-136">NOTES</span></span>

## <span data-ttu-id="aa03e-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa03e-137">RELATED LINKS</span></span>
