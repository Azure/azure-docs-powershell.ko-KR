---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: c3ff96a2c1d06fdfba5879244b058ef1a7845f40
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202961"
---
# <span data-ttu-id="13a4d-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="13a4d-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="13a4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13a4d-102">SYNOPSIS</span></span>
<span data-ttu-id="13a4d-103">방화벽 조건에 대한 일치 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13a4d-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="13a4d-104">구문</span><span class="sxs-lookup"><span data-stu-id="13a4d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13a4d-105">설명</span><span class="sxs-lookup"><span data-stu-id="13a4d-105">DESCRIPTION</span></span>
<span data-ttu-id="13a4d-106">**New-AzApplicationGatewayFirewallMatchVariable은** 방화벽 조건에 대한 일치 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13a4d-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="13a4d-107">예제</span><span class="sxs-lookup"><span data-stu-id="13a4d-107">EXAMPLES</span></span>

### <span data-ttu-id="13a4d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="13a4d-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="13a4d-109">이 명령은 요청 헤더의 이름으로 새 일치 변수를 만들고 선택기에서 Content-Length 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="13a4d-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="13a4d-110">새 일치 변수는 새 일치 $variable.</span><span class="sxs-lookup"><span data-stu-id="13a4d-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="13a4d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13a4d-111">PARAMETERS</span></span>

### <span data-ttu-id="13a4d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13a4d-112">-DefaultProfile</span></span>
<span data-ttu-id="13a4d-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13a4d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13a4d-114">-Selector</span><span class="sxs-lookup"><span data-stu-id="13a4d-114">-Selector</span></span>
<span data-ttu-id="13a4d-115">matchVariable 컬렉션의 필드를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="13a4d-115">Describes field of the matchVariable collection.</span></span>

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

### <span data-ttu-id="13a4d-116">-VariableName</span><span class="sxs-lookup"><span data-stu-id="13a4d-116">-VariableName</span></span>
<span data-ttu-id="13a4d-117">변수 일치.</span><span class="sxs-lookup"><span data-stu-id="13a4d-117">Match Variable.</span></span>

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

### <span data-ttu-id="13a4d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13a4d-118">CommonParameters</span></span>
<span data-ttu-id="13a4d-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="13a4d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13a4d-120">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="13a4d-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13a4d-121">입력</span><span class="sxs-lookup"><span data-stu-id="13a4d-121">INPUTS</span></span>

### <span data-ttu-id="13a4d-122">없음</span><span class="sxs-lookup"><span data-stu-id="13a4d-122">None</span></span>

## <span data-ttu-id="13a4d-123">출력</span><span class="sxs-lookup"><span data-stu-id="13a4d-123">OUTPUTS</span></span>

### <span data-ttu-id="13a4d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="13a4d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="13a4d-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="13a4d-125">NOTES</span></span>

## <span data-ttu-id="13a4d-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13a4d-126">RELATED LINKS</span></span>
