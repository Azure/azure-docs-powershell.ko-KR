---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: c98d36e7f08d16f12581c340b875e26f5a393f1b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700395"
---
# <span data-ttu-id="ff0bc-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="ff0bc-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="ff0bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff0bc-102">SYNOPSIS</span></span>
<span data-ttu-id="ff0bc-103">응용 프로그램 게이트웨이에 대 한 상태 프로브에 사용 되는 상태 프로브 응답 일치를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ff0bc-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="ff0bc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ff0bc-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>] [-StatusCode <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff0bc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ff0bc-105">DESCRIPTION</span></span>
<span data-ttu-id="ff0bc-106">**AzApplicationGatewayProbeHealthResponseMatch Cmdlet은** 응용 프로그램 게이트웨이에 대 한 상태 프로브에 사용 되는 상태 프로브 응답 일치를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ff0bc-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="ff0bc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ff0bc-107">EXAMPLES</span></span>

### <span data-ttu-id="ff0bc-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ff0bc-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="ff0bc-109">이 명령은 ProbeConfig에 매개 변수로 전달 될 수 있는 상태 응답 일치를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ff0bc-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="ff0bc-110">변수</span><span class="sxs-lookup"><span data-stu-id="ff0bc-110">PARAMETERS</span></span>

### <span data-ttu-id="ff0bc-111">-본문</span><span class="sxs-lookup"><span data-stu-id="ff0bc-111">-Body</span></span>
<span data-ttu-id="ff0bc-112">상태 응답에 포함 해야 하는 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="ff0bc-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="ff0bc-113">Default 값이 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ff0bc-113">Default value is empty</span></span>

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

### <span data-ttu-id="ff0bc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff0bc-114">-DefaultProfile</span></span>
<span data-ttu-id="ff0bc-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ff0bc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff0bc-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="ff0bc-116">-StatusCode</span></span>
<span data-ttu-id="ff0bc-117">허용 되는 정상 상태 코드 범위입니다. 정상 상태 코드의 기본 범위는 200-399입니다.</span><span class="sxs-lookup"><span data-stu-id="ff0bc-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

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

### <span data-ttu-id="ff0bc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff0bc-118">CommonParameters</span></span>
<span data-ttu-id="ff0bc-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff0bc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff0bc-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff0bc-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff0bc-121">입력</span><span class="sxs-lookup"><span data-stu-id="ff0bc-121">INPUTS</span></span>

### <span data-ttu-id="ff0bc-122">않아야</span><span class="sxs-lookup"><span data-stu-id="ff0bc-122">None</span></span>

## <span data-ttu-id="ff0bc-123">출력</span><span class="sxs-lookup"><span data-stu-id="ff0bc-123">OUTPUTS</span></span>

### <span data-ttu-id="ff0bc-124">PSApplicationGatewayProbeHealthResponseMatch에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ff0bc-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="ff0bc-125">상속자</span><span class="sxs-lookup"><span data-stu-id="ff0bc-125">NOTES</span></span>

## <span data-ttu-id="ff0bc-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff0bc-126">RELATED LINKS</span></span>
