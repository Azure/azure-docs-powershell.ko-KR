---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: 04da18bcd50fa547f1a59142682c93b4e3e5ab62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974784"
---
# <span data-ttu-id="a6c2f-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="a6c2f-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="a6c2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6c2f-102">SYNOPSIS</span></span>
<span data-ttu-id="a6c2f-103">애플리케이션 게이트웨이에 대해 Health Probe에서 사용하는 상태 프로브 응답 일치를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a6c2f-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="a6c2f-104">구문</span><span class="sxs-lookup"><span data-stu-id="a6c2f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>] [-StatusCode <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6c2f-105">설명</span><span class="sxs-lookup"><span data-stu-id="a6c2f-105">DESCRIPTION</span></span>
<span data-ttu-id="a6c2f-106">**Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet은 애플리케이션 게이트웨이에 대해 Health Probe에서 사용하는 상태 프로브 응답 일치를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a6c2f-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="a6c2f-107">예제</span><span class="sxs-lookup"><span data-stu-id="a6c2f-107">EXAMPLES</span></span>

### <span data-ttu-id="a6c2f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a6c2f-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="a6c2f-109">이 명령은 ProbeConfig에 매개 변수로 전달할 수 있는 상태 응답 일치를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a6c2f-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="a6c2f-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a6c2f-110">PARAMETERS</span></span>

### <span data-ttu-id="a6c2f-111">-Body</span><span class="sxs-lookup"><span data-stu-id="a6c2f-111">-Body</span></span>
<span data-ttu-id="a6c2f-112">상태 응답에 포함되어야 하는 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="a6c2f-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="a6c2f-113">기본값이 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6c2f-113">Default value is empty</span></span>

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

### <span data-ttu-id="a6c2f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6c2f-114">-DefaultProfile</span></span>
<span data-ttu-id="a6c2f-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a6c2f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6c2f-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="a6c2f-116">-StatusCode</span></span>
<span data-ttu-id="a6c2f-117">허용되는 범위의 정상 상태 코드입니다. 정상 상태 코드의 기본 범위는 200 - 399입니다.</span><span class="sxs-lookup"><span data-stu-id="a6c2f-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c2f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6c2f-118">CommonParameters</span></span>
<span data-ttu-id="a6c2f-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a6c2f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6c2f-120">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a6c2f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6c2f-121">입력</span><span class="sxs-lookup"><span data-stu-id="a6c2f-121">INPUTS</span></span>

### <span data-ttu-id="a6c2f-122">없음</span><span class="sxs-lookup"><span data-stu-id="a6c2f-122">None</span></span>

## <span data-ttu-id="a6c2f-123">출력</span><span class="sxs-lookup"><span data-stu-id="a6c2f-123">OUTPUTS</span></span>

### <span data-ttu-id="a6c2f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="a6c2f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="a6c2f-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a6c2f-125">NOTES</span></span>

## <span data-ttu-id="a6c2f-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a6c2f-126">RELATED LINKS</span></span>
