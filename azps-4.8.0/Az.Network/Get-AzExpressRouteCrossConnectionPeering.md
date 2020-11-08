---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 15aed0e5a4cca1b67c85cbe651453d64cecc13ee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204552"
---
# <span data-ttu-id="bc2e0-101">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="bc2e0-101">Get-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="bc2e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc2e0-102">SYNOPSIS</span></span>
<span data-ttu-id="bc2e0-103">Express 간 연결 피어 링 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bc2e0-103">Gets an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="bc2e0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bc2e0-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnectionPeering [-Name <String>]
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc2e0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bc2e0-105">DESCRIPTION</span></span>
<span data-ttu-id="bc2e0-106">**AzExpressRouteCrossConnectionPeering** Cmdlet은 express 경로 간 연결에 대 한 피어 링 관계의 구성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc2e0-106">The **Get-AzExpressRouteCrossConnectionPeering** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="bc2e0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bc2e0-107">EXAMPLES</span></span>

### <span data-ttu-id="bc2e0-108">예제 1: Express 경로 간 연결에 대 한 피어 링 구성 표시</span><span class="sxs-lookup"><span data-stu-id="bc2e0-108">Example 1: Display the peering configuration for an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $RG
Get-AzExpressRouteCrossConnectionPeering -Name "AzurePrivatePeering" -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="bc2e0-109">변수</span><span class="sxs-lookup"><span data-stu-id="bc2e0-109">PARAMETERS</span></span>

### <span data-ttu-id="bc2e0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc2e0-110">-DefaultProfile</span></span>
<span data-ttu-id="bc2e0-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bc2e0-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc2e0-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="bc2e0-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="bc2e0-113">피어 링 구성을 포함 하는 Express 경로 간 연결 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="bc2e0-113">The ExpressRoute cross connection object containing the peering configuration.</span></span>

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

### <span data-ttu-id="bc2e0-114">-이름</span><span class="sxs-lookup"><span data-stu-id="bc2e0-114">-Name</span></span>
<span data-ttu-id="bc2e0-115">검색할 피어 링 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc2e0-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="bc2e0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc2e0-116">CommonParameters</span></span>
<span data-ttu-id="bc2e0-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc2e0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc2e0-118">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc2e0-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc2e0-119">입력</span><span class="sxs-lookup"><span data-stu-id="bc2e0-119">INPUTS</span></span>

### <span data-ttu-id="bc2e0-120">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="bc2e0-120">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="bc2e0-121">' ExpressRouteCrossConnection ' 매개 변수는 파이프라인에서 ' PSExpressRouteCrossConnection ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc2e0-121">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="bc2e0-122">출력</span><span class="sxs-lookup"><span data-stu-id="bc2e0-122">OUTPUTS</span></span>

### <span data-ttu-id="bc2e0-123">PSPeering에 대 한.</span><span class="sxs-lookup"><span data-stu-id="bc2e0-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="bc2e0-124">상속자</span><span class="sxs-lookup"><span data-stu-id="bc2e0-124">NOTES</span></span>

## <span data-ttu-id="bc2e0-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bc2e0-125">RELATED LINKS</span></span>

[<span data-ttu-id="bc2e0-126">추가-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="bc2e0-126">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="bc2e0-127">제거-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="bc2e0-127">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="bc2e0-128">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="bc2e0-128">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="bc2e0-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="bc2e0-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
