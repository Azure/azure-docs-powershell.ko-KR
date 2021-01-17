---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: c3ff96a2c1d06fdfba5879244b058ef1a7845f40
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346634"
---
# <span data-ttu-id="a67fc-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="a67fc-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="a67fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a67fc-102">SYNOPSIS</span></span>
<span data-ttu-id="a67fc-103">방화벽 조건에 대한 일치 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a67fc-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="a67fc-104">구문</span><span class="sxs-lookup"><span data-stu-id="a67fc-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a67fc-105">설명</span><span class="sxs-lookup"><span data-stu-id="a67fc-105">DESCRIPTION</span></span>
<span data-ttu-id="a67fc-106">**New-AzApplicationGatewayFirewallMatchVariable은** 방화벽 조건에 대한 일치 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a67fc-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="a67fc-107">예제</span><span class="sxs-lookup"><span data-stu-id="a67fc-107">EXAMPLES</span></span>

### <span data-ttu-id="a67fc-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a67fc-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="a67fc-109">이 명령은 요청 헤더의 이름을 사용하여 새 일치 변수를 만들고 선택기에서 Content-Length 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="a67fc-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="a67fc-110">새 일치 변수는 새 일치 $variable.</span><span class="sxs-lookup"><span data-stu-id="a67fc-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="a67fc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a67fc-111">PARAMETERS</span></span>

### <span data-ttu-id="a67fc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a67fc-112">-DefaultProfile</span></span>
<span data-ttu-id="a67fc-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a67fc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a67fc-114">-Selector</span><span class="sxs-lookup"><span data-stu-id="a67fc-114">-Selector</span></span>
<span data-ttu-id="a67fc-115">matchVariable 컬렉션의 필드를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="a67fc-115">Describes field of the matchVariable collection.</span></span>

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

### <span data-ttu-id="a67fc-116">-VariableName</span><span class="sxs-lookup"><span data-stu-id="a67fc-116">-VariableName</span></span>
<span data-ttu-id="a67fc-117">변수 일치.</span><span class="sxs-lookup"><span data-stu-id="a67fc-117">Match Variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestHeaders, RequestBody, RequestCookies

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a67fc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a67fc-118">CommonParameters</span></span>
<span data-ttu-id="a67fc-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a67fc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a67fc-120">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a67fc-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a67fc-121">입력</span><span class="sxs-lookup"><span data-stu-id="a67fc-121">INPUTS</span></span>

### <span data-ttu-id="a67fc-122">없음</span><span class="sxs-lookup"><span data-stu-id="a67fc-122">None</span></span>

## <span data-ttu-id="a67fc-123">출력</span><span class="sxs-lookup"><span data-stu-id="a67fc-123">OUTPUTS</span></span>

### <span data-ttu-id="a67fc-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="a67fc-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="a67fc-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a67fc-125">NOTES</span></span>

## <span data-ttu-id="a67fc-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a67fc-126">RELATED LINKS</span></span>
