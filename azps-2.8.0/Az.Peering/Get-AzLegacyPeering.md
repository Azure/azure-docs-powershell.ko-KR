---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azlegacypeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
ms.openlocfilehash: 9a2fcb87b05d4478ab7b3e3490feae92fd727ce7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872401"
---
# <span data-ttu-id="f755d-101">Get-AzLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="f755d-101">Get-AzLegacyPeering</span></span>

## <span data-ttu-id="f755d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f755d-102">SYNOPSIS</span></span>
<span data-ttu-id="f755d-103">레거시 피어 링 리소스를 ARM (Azure Resource Management) 리소스로 변환 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f755d-103">Used to Convert Legacy Peering resources to Azure Resource Management (ARM) Resources.</span></span> 

## <span data-ttu-id="f755d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f755d-104">SYNTAX</span></span>

```
Get-AzLegacyPeering [-PeeringLocation] <String> [-Kind] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f755d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f755d-105">DESCRIPTION</span></span>
<span data-ttu-id="f755d-106">명령은이 명령을 사용 하 여 ARM (Azure Resource Management) 리소스로 변환 하는 레거시 피어 링 리소스를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f755d-106">The command is used to view legacy Peering resources which all you to convert them to Azure Resource Management (ARM) Resources.</span></span>

## <span data-ttu-id="f755d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f755d-107">EXAMPLES</span></span>

### <span data-ttu-id="f755d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f755d-108">Example 1</span></span>
```powershell
PS C:> Get-AzLegacyPeering -PeeringLocation "Seattle" -Kind Direct

Name                       :
Sku                        : Basic_Direct_Free
Kind                       : Direct
PeeringLocation            : Seattle
UseForPeeringService       : False
PeerAsn.Id                 :
Connection                 : ------------------------
PeeringDBFacilityId        : 71
SessionPrefixIPv4          : 173.205.50.236/30
PeerSessionIPv4Address     : 173.205.50.237
MicrosoftIPv4Address       : 173.205.50.238
SessionStateV4             : Established
MaxPrefixesAdvertisedV4    : 20000
SessionPrefixIPv6          : 2001:668:0:3:ffff:0:adcd:32ec/126
PeerSessionIPv6Address     : 2001:668:0:3:ffff:0:adcd:32ed
MicrosoftIPv6Address       : 2001:668:0:3:ffff:0:adcd:32ee
SessionStateV6             : Established
MaxPrefixesAdvertisedV6    : 2000
ConnectionState            : Active
BandwidthInMbps            : 0
ProvisionedBandwidthInMbps : 20000
ProvisioningState          : Succeeded
```

<span data-ttu-id="f755d-109">시애틀의 레거시 피어 링을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f755d-109">Gets the legacy peering for Seattle</span></span>

## <span data-ttu-id="f755d-110">변수</span><span class="sxs-lookup"><span data-stu-id="f755d-110">PARAMETERS</span></span>

### <span data-ttu-id="f755d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f755d-111">-DefaultProfile</span></span>
<span data-ttu-id="f755d-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f755d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f755d-113">-종류</span><span class="sxs-lookup"><span data-stu-id="f755d-113">-Kind</span></span>
<span data-ttu-id="f755d-114">모든 피어 링 리소스를 종류별로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f755d-114">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f755d-115">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="f755d-115">-PeeringLocation</span></span>
<span data-ttu-id="f755d-116">모든 피어 링 리소스를 종류별로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f755d-116">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="f755d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f755d-117">CommonParameters</span></span>
<span data-ttu-id="f755d-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f755d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f755d-119">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f755d-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f755d-120">입력</span><span class="sxs-lookup"><span data-stu-id="f755d-120">INPUTS</span></span>

### <span data-ttu-id="f755d-121">않아야</span><span class="sxs-lookup"><span data-stu-id="f755d-121">None</span></span>

## <span data-ttu-id="f755d-122">출력</span><span class="sxs-lookup"><span data-stu-id="f755d-122">OUTPUTS</span></span>

### <span data-ttu-id="f755d-123">PSPeering (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f755d-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="f755d-124">상속자</span><span class="sxs-lookup"><span data-stu-id="f755d-124">NOTES</span></span>

## <span data-ttu-id="f755d-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f755d-125">RELATED LINKS</span></span>
