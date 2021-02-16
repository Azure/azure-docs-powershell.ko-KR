---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/send-feedback
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Send-Feedback.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Send-Feedback.md
ms.openlocfilehash: 1405886572efabf1ffc91f071f262ca98515d141
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176524"
---
# <span data-ttu-id="f197b-101">Send-Feedback</span><span class="sxs-lookup"><span data-stu-id="f197b-101">Send-Feedback</span></span>

## <span data-ttu-id="f197b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f197b-102">SYNOPSIS</span></span>
<span data-ttu-id="f197b-103">안내된 프롬프트 집합을 통해 Azure PowerShell 팀에 피드백을 전송합니다.</span><span class="sxs-lookup"><span data-stu-id="f197b-103">Sends feedback to the Azure PowerShell team via a set of guided prompts.</span></span>

## <span data-ttu-id="f197b-104">구문</span><span class="sxs-lookup"><span data-stu-id="f197b-104">SYNTAX</span></span>

```
Send-Feedback [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f197b-105">설명</span><span class="sxs-lookup"><span data-stu-id="f197b-105">DESCRIPTION</span></span>
<span data-ttu-id="f197b-106">Send-Feedback cmdlet은 Azure PowerShell 팀에 피드백을 전송합니다.</span><span class="sxs-lookup"><span data-stu-id="f197b-106">The Send-Feedback cmdlet sends feedback to the Azure PowerShell team.</span></span>

## <span data-ttu-id="f197b-107">예제</span><span class="sxs-lookup"><span data-stu-id="f197b-107">EXAMPLES</span></span>

### <span data-ttu-id="f197b-108">예제 1:</span><span class="sxs-lookup"><span data-stu-id="f197b-108">Example 1:</span></span>
```
PS C:\> Send-Feedback

With zero (0) being the least and ten (10) being the most, how likely are you to recommend Azure PowerShell to a friend or colleague?

10

What does Azure PowerShell do well?

Response.

Upon what could Azure PowerShell improve?

Response.

Please enter your email if you are interested in providing follow up information:

your@email.com
```

## <span data-ttu-id="f197b-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f197b-109">PARAMETERS</span></span>

### <span data-ttu-id="f197b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f197b-110">-DefaultProfile</span></span>
<span data-ttu-id="f197b-111">Azure와의 통신에 사용되는 자격 증명, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f197b-111">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f197b-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f197b-112">CommonParameters</span></span>
<span data-ttu-id="f197b-113">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f197b-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f197b-114">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f197b-114">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f197b-115">입력</span><span class="sxs-lookup"><span data-stu-id="f197b-115">INPUTS</span></span>

### <span data-ttu-id="f197b-116">없음</span><span class="sxs-lookup"><span data-stu-id="f197b-116">None</span></span>

## <span data-ttu-id="f197b-117">출력</span><span class="sxs-lookup"><span data-stu-id="f197b-117">OUTPUTS</span></span>

### <span data-ttu-id="f197b-118">System.Void</span><span class="sxs-lookup"><span data-stu-id="f197b-118">System.Void</span></span>

## <span data-ttu-id="f197b-119">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f197b-119">NOTES</span></span>

## <span data-ttu-id="f197b-120">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f197b-120">RELATED LINKS</span></span>
