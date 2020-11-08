---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
ms.openlocfilehash: 246675a2473bb20e5040f3898b6931f1b3ee6933
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043359"
---
# <span data-ttu-id="f5492-101">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="f5492-101">Get-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="f5492-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5492-102">SYNOPSIS</span></span>
<span data-ttu-id="f5492-103">ExpressRoutePort에 할당 된 id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f5492-103">Get identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="f5492-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f5492-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5492-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f5492-105">DESCRIPTION</span></span>
<span data-ttu-id="f5492-106">**AzExpressRoutePortIdentity** cmdlet은 로컬 Azure ExpressRoutePort 개체에 할당 된 id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f5492-106">The **Get-AzExpressRoutePortIdentity** cmdlet gets identity assigned to a local Azure ExpressRoutePort object.</span></span>

## <span data-ttu-id="f5492-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f5492-107">EXAMPLES</span></span>

### <span data-ttu-id="f5492-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f5492-108">Example 1</span></span>
```powershell
PS C:\> $exrPort = Get-AzExpressRoutePort -Name $exrPortName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzExpressRoutePortIdentity -ExpressRoutePort $exrPort
```

## <span data-ttu-id="f5492-109">변수</span><span class="sxs-lookup"><span data-stu-id="f5492-109">PARAMETERS</span></span>

### <span data-ttu-id="f5492-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5492-110">-DefaultProfile</span></span>
<span data-ttu-id="f5492-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5492-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5492-112">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f5492-112">-ExpressRoutePort</span></span>
<span data-ttu-id="f5492-113">(Express 경로 포트)</span><span class="sxs-lookup"><span data-stu-id="f5492-113">The ExpressRoute Port</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5492-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5492-114">CommonParameters</span></span>
<span data-ttu-id="f5492-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5492-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5492-116">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f5492-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5492-117">입력</span><span class="sxs-lookup"><span data-stu-id="f5492-117">INPUTS</span></span>

### <span data-ttu-id="f5492-118">PSExpressRoutePort에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f5492-118">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="f5492-119">출력</span><span class="sxs-lookup"><span data-stu-id="f5492-119">OUTPUTS</span></span>

### <span data-ttu-id="f5492-120">PSManagedServiceIdentity에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f5492-120">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="f5492-121">상속자</span><span class="sxs-lookup"><span data-stu-id="f5492-121">NOTES</span></span>

## <span data-ttu-id="f5492-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5492-122">RELATED LINKS</span></span>
[<span data-ttu-id="f5492-123">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="f5492-123">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="f5492-124">새로운 AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="f5492-124">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="f5492-125">제거-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="f5492-125">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)