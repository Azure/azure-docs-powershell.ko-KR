---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: f2175583aaaf3af04120e22e32db79d7b20f1e30
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354122"
---
# <span data-ttu-id="01ede-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="01ede-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="01ede-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01ede-102">SYNOPSIS</span></span>
<span data-ttu-id="01ede-103">Application Gateway에 대한 ssl 정책에 사용 가능한 모든 ssl 옵션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="01ede-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="01ede-104">구문</span><span class="sxs-lookup"><span data-stu-id="01ede-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01ede-105">설명</span><span class="sxs-lookup"><span data-stu-id="01ede-105">DESCRIPTION</span></span>
<span data-ttu-id="01ede-106">**Get-AzApplicationGatewayAvailableSslOption** cmdlet은 ssl 정책에 사용 가능한 모든 ssl 옵션을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="01ede-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="01ede-107">예제</span><span class="sxs-lookup"><span data-stu-id="01ede-107">EXAMPLES</span></span>

### <span data-ttu-id="01ede-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="01ede-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="01ede-109">이 명령은 ssl 정책에 사용 가능한 모든 ssl 옵션을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="01ede-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="01ede-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01ede-110">PARAMETERS</span></span>

### <span data-ttu-id="01ede-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01ede-111">-DefaultProfile</span></span>
<span data-ttu-id="01ede-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="01ede-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01ede-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01ede-113">CommonParameters</span></span>
<span data-ttu-id="01ede-114">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="01ede-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01ede-115">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="01ede-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01ede-116">입력</span><span class="sxs-lookup"><span data-stu-id="01ede-116">INPUTS</span></span>

### <span data-ttu-id="01ede-117">없음</span><span class="sxs-lookup"><span data-stu-id="01ede-117">None</span></span>

## <span data-ttu-id="01ede-118">출력</span><span class="sxs-lookup"><span data-stu-id="01ede-118">OUTPUTS</span></span>

### <span data-ttu-id="01ede-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="01ede-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="01ede-120">참고 사항</span><span class="sxs-lookup"><span data-stu-id="01ede-120">NOTES</span></span>

## <span data-ttu-id="01ede-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01ede-121">RELATED LINKS</span></span>