---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 15aed0e5a4cca1b67c85cbe651453d64cecc13ee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489923"
---
# <span data-ttu-id="de1ca-101">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="de1ca-101">Get-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="de1ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de1ca-102">SYNOPSIS</span></span>
<span data-ttu-id="de1ca-103">ExpressRoute 교차 연결 피어링 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="de1ca-103">Gets an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="de1ca-104">구문</span><span class="sxs-lookup"><span data-stu-id="de1ca-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnectionPeering [-Name <String>]
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de1ca-105">설명</span><span class="sxs-lookup"><span data-stu-id="de1ca-105">DESCRIPTION</span></span>
<span data-ttu-id="de1ca-106">**Get-AzExpressRouteCrossConnectionPeering** cmdlet은 ExpressRoute 교차 연결에 대한 피어링 관계의 구성을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="de1ca-106">The **Get-AzExpressRouteCrossConnectionPeering** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="de1ca-107">예제</span><span class="sxs-lookup"><span data-stu-id="de1ca-107">EXAMPLES</span></span>

### <span data-ttu-id="de1ca-108">예제 1: ExpressRoute 교차 연결에 대한 피어링 구성 표시</span><span class="sxs-lookup"><span data-stu-id="de1ca-108">Example 1: Display the peering configuration for an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $RG
Get-AzExpressRouteCrossConnectionPeering -Name "AzurePrivatePeering" -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="de1ca-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de1ca-109">PARAMETERS</span></span>

### <span data-ttu-id="de1ca-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de1ca-110">-DefaultProfile</span></span>
<span data-ttu-id="de1ca-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="de1ca-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de1ca-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="de1ca-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="de1ca-113">피어링 구성을 포함하는 ExpressRoute 교차 연결 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="de1ca-113">The ExpressRoute cross connection object containing the peering configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de1ca-114">-Name</span><span class="sxs-lookup"><span data-stu-id="de1ca-114">-Name</span></span>
<span data-ttu-id="de1ca-115">검색할 피어링 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="de1ca-115">The name of the peering configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de1ca-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de1ca-116">CommonParameters</span></span>
<span data-ttu-id="de1ca-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="de1ca-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de1ca-118">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="de1ca-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de1ca-119">입력</span><span class="sxs-lookup"><span data-stu-id="de1ca-119">INPUTS</span></span>

### <span data-ttu-id="de1ca-120">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="de1ca-120">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="de1ca-121">'ExpressRouteCrossConnection' 매개 변수는 파이프라인에서 'PSExpressRouteCrossConnection' 형식의 값을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="de1ca-121">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="de1ca-122">출력</span><span class="sxs-lookup"><span data-stu-id="de1ca-122">OUTPUTS</span></span>

### <span data-ttu-id="de1ca-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="de1ca-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="de1ca-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="de1ca-124">NOTES</span></span>

## <span data-ttu-id="de1ca-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="de1ca-125">RELATED LINKS</span></span>

[<span data-ttu-id="de1ca-126">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="de1ca-126">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="de1ca-127">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="de1ca-127">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="de1ca-128">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="de1ca-128">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="de1ca-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="de1ca-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
