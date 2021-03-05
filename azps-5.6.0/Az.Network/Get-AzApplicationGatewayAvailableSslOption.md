---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: 8d2022f79dff5263f07737d525169dad3566fcda
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003643"
---
# <span data-ttu-id="c2da5-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="c2da5-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="c2da5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2da5-102">SYNOPSIS</span></span>
<span data-ttu-id="c2da5-103">Application Gateway에 대한 ssl 정책에 사용할 수 있는 모든 ssl 옵션을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c2da5-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="c2da5-104">구문</span><span class="sxs-lookup"><span data-stu-id="c2da5-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2da5-105">설명</span><span class="sxs-lookup"><span data-stu-id="c2da5-105">DESCRIPTION</span></span>
<span data-ttu-id="c2da5-106">**Get-AzApplicationGatewayAvailableSslOption** cmdlet은 ssl 정책에 사용할 수 있는 모든 ssl 옵션을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c2da5-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="c2da5-107">예제</span><span class="sxs-lookup"><span data-stu-id="c2da5-107">EXAMPLES</span></span>

### <span data-ttu-id="c2da5-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c2da5-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="c2da5-109">이 명령은 ssl 정책에 사용할 수 있는 모든 ssl 옵션을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c2da5-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="c2da5-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c2da5-110">PARAMETERS</span></span>

### <span data-ttu-id="c2da5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2da5-111">-DefaultProfile</span></span>
<span data-ttu-id="c2da5-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2da5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2da5-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2da5-113">CommonParameters</span></span>
<span data-ttu-id="c2da5-114">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c2da5-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2da5-115">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2da5-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2da5-116">입력</span><span class="sxs-lookup"><span data-stu-id="c2da5-116">INPUTS</span></span>

### <span data-ttu-id="c2da5-117">없음</span><span class="sxs-lookup"><span data-stu-id="c2da5-117">None</span></span>

## <span data-ttu-id="c2da5-118">출력</span><span class="sxs-lookup"><span data-stu-id="c2da5-118">OUTPUTS</span></span>

### <span data-ttu-id="c2da5-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="c2da5-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="c2da5-120">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c2da5-120">NOTES</span></span>

## <span data-ttu-id="c2da5-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2da5-121">RELATED LINKS</span></span>
