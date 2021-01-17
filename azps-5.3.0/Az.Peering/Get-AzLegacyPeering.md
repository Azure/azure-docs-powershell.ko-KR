---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azlegacypeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
ms.openlocfilehash: e7b5ef8ef41c66cc3c19fd5ebdcfd53ddcc6f3a9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491734"
---
# <span data-ttu-id="99e77-101">Get-AzLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="99e77-101">Get-AzLegacyPeering</span></span>

## <span data-ttu-id="99e77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99e77-102">SYNOPSIS</span></span>
<span data-ttu-id="99e77-103">레거시 피어링 리소스를 Azure 리소스 관리(ARM) 리소스로 변환하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="99e77-103">Used to Convert Legacy Peering resources to Azure Resource Management (ARM) Resources.</span></span> 

## <span data-ttu-id="99e77-104">구문</span><span class="sxs-lookup"><span data-stu-id="99e77-104">SYNTAX</span></span>

```
Get-AzLegacyPeering [-PeeringLocation] <String> [-Kind] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99e77-105">설명</span><span class="sxs-lookup"><span data-stu-id="99e77-105">DESCRIPTION</span></span>
<span data-ttu-id="99e77-106">이 명령은 Azure 리소스 관리(ARM) 리소스로 변환할 레거시 피어링 리소스를 보는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="99e77-106">The command is used to view legacy Peering resources which all you to convert them to Azure Resource Management (ARM) Resources.</span></span>

## <span data-ttu-id="99e77-107">예제</span><span class="sxs-lookup"><span data-stu-id="99e77-107">EXAMPLES</span></span>

### <span data-ttu-id="99e77-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="99e77-108">Example 1</span></span>
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

<span data-ttu-id="99e77-109">시애틀에 대한 레거시 피어링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="99e77-109">Gets the legacy peering for Seattle</span></span>

## <span data-ttu-id="99e77-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99e77-110">PARAMETERS</span></span>

### <span data-ttu-id="99e77-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99e77-111">-DefaultProfile</span></span>
<span data-ttu-id="99e77-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="99e77-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99e77-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="99e77-113">-Kind</span></span>
<span data-ttu-id="99e77-114">종류에 따라 모든 피어링 리소스를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="99e77-114">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="99e77-115">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="99e77-115">-PeeringLocation</span></span>
<span data-ttu-id="99e77-116">종류에 따라 모든 피어링 리소스를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="99e77-116">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="99e77-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99e77-117">CommonParameters</span></span>
<span data-ttu-id="99e77-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="99e77-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99e77-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="99e77-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99e77-120">입력</span><span class="sxs-lookup"><span data-stu-id="99e77-120">INPUTS</span></span>

### <span data-ttu-id="99e77-121">없음</span><span class="sxs-lookup"><span data-stu-id="99e77-121">None</span></span>

## <span data-ttu-id="99e77-122">출력</span><span class="sxs-lookup"><span data-stu-id="99e77-122">OUTPUTS</span></span>

### <span data-ttu-id="99e77-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="99e77-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="99e77-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="99e77-124">NOTES</span></span>

## <span data-ttu-id="99e77-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99e77-125">RELATED LINKS</span></span>
