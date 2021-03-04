---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
ms.openlocfilehash: a64bbe0dfad8e9e82138c50e6ff436a445f68392
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957019"
---
# <span data-ttu-id="22ac6-101">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="22ac6-101">Get-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="22ac6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22ac6-102">SYNOPSIS</span></span>
<span data-ttu-id="22ac6-103">ExpressRoutePort에 ID를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="22ac6-103">Get identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="22ac6-104">구문</span><span class="sxs-lookup"><span data-stu-id="22ac6-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22ac6-105">설명</span><span class="sxs-lookup"><span data-stu-id="22ac6-105">DESCRIPTION</span></span>
<span data-ttu-id="22ac6-106">**Get-AzExpressRoutePortIdentity** cmdlet은 로컬 Azure ExpressRoutePort 개체에 할당된 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="22ac6-106">The **Get-AzExpressRoutePortIdentity** cmdlet gets identity assigned to a local Azure ExpressRoutePort object.</span></span>

## <span data-ttu-id="22ac6-107">예제</span><span class="sxs-lookup"><span data-stu-id="22ac6-107">EXAMPLES</span></span>

### <span data-ttu-id="22ac6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="22ac6-108">Example 1</span></span>
```powershell
PS C:\> $exrPort = Get-AzExpressRoutePort -Name $exrPortName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzExpressRoutePortIdentity -ExpressRoutePort $exrPort
```

## <span data-ttu-id="22ac6-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="22ac6-109">PARAMETERS</span></span>

### <span data-ttu-id="22ac6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22ac6-110">-DefaultProfile</span></span>
<span data-ttu-id="22ac6-111">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="22ac6-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22ac6-112">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="22ac6-112">-ExpressRoutePort</span></span>
<span data-ttu-id="22ac6-113">ExpressRoute 포트</span><span class="sxs-lookup"><span data-stu-id="22ac6-113">The ExpressRoute Port</span></span>

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

### <span data-ttu-id="22ac6-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22ac6-114">CommonParameters</span></span>
<span data-ttu-id="22ac6-115">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="22ac6-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22ac6-116">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22ac6-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22ac6-117">입력</span><span class="sxs-lookup"><span data-stu-id="22ac6-117">INPUTS</span></span>

### <span data-ttu-id="22ac6-118">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="22ac6-118">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="22ac6-119">출력</span><span class="sxs-lookup"><span data-stu-id="22ac6-119">OUTPUTS</span></span>

### <span data-ttu-id="22ac6-120">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="22ac6-120">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="22ac6-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="22ac6-121">NOTES</span></span>

## <span data-ttu-id="22ac6-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22ac6-122">RELATED LINKS</span></span>
[<span data-ttu-id="22ac6-123">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="22ac6-123">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="22ac6-124">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="22ac6-124">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="22ac6-125">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="22ac6-125">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)