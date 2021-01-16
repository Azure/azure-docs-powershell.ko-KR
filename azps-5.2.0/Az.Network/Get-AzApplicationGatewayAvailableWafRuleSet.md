---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: 7cb3f6d015f95ba6a72066714647eb7a0551398b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354098"
---
# <span data-ttu-id="71984-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="71984-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="71984-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71984-102">SYNOPSIS</span></span>
<span data-ttu-id="71984-103">사용 가능한 모든 웹 애플리케이션 방화벽 규칙 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="71984-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="71984-104">구문</span><span class="sxs-lookup"><span data-stu-id="71984-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71984-105">설명</span><span class="sxs-lookup"><span data-stu-id="71984-105">DESCRIPTION</span></span>
<span data-ttu-id="71984-106">**Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet은 사용 가능한 모든 웹 애플리케이션 방화벽 규칙 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="71984-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="71984-107">예제</span><span class="sxs-lookup"><span data-stu-id="71984-107">EXAMPLES</span></span>

### <span data-ttu-id="71984-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="71984-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="71984-109">이 명령은 사용 가능한 모든 웹 애플리케이션 방화벽 규칙 집합을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="71984-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="71984-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71984-110">PARAMETERS</span></span>

### <span data-ttu-id="71984-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71984-111">-DefaultProfile</span></span>
<span data-ttu-id="71984-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="71984-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71984-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71984-113">CommonParameters</span></span>
<span data-ttu-id="71984-114">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="71984-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71984-115">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="71984-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71984-116">입력</span><span class="sxs-lookup"><span data-stu-id="71984-116">INPUTS</span></span>

### <span data-ttu-id="71984-117">없음</span><span class="sxs-lookup"><span data-stu-id="71984-117">None</span></span>

## <span data-ttu-id="71984-118">출력</span><span class="sxs-lookup"><span data-stu-id="71984-118">OUTPUTS</span></span>

### <span data-ttu-id="71984-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="71984-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="71984-120">참고 사항</span><span class="sxs-lookup"><span data-stu-id="71984-120">NOTES</span></span>
<span data-ttu-id="71984-121">**List-AzApplicationGatewayAvailableWafRuleSets는** **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet의 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="71984-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="71984-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71984-122">RELATED LINKS</span></span>
