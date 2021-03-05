---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/send-feedback
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Send-Feedback.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Send-Feedback.md
ms.openlocfilehash: 2aa11756187df613f0f78bcfbe9592ba19b41caa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963355"
---
# <span data-ttu-id="97095-101">Send-Feedback</span><span class="sxs-lookup"><span data-stu-id="97095-101">Send-Feedback</span></span>

## <span data-ttu-id="97095-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97095-102">SYNOPSIS</span></span>
<span data-ttu-id="97095-103">가이드 프롬프트 집합을 통해 Azure PowerShell 팀에 피드백을 전송합니다.</span><span class="sxs-lookup"><span data-stu-id="97095-103">Sends feedback to the Azure PowerShell team via a set of guided prompts.</span></span>

## <span data-ttu-id="97095-104">구문</span><span class="sxs-lookup"><span data-stu-id="97095-104">SYNTAX</span></span>

```
Send-Feedback [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97095-105">설명</span><span class="sxs-lookup"><span data-stu-id="97095-105">DESCRIPTION</span></span>
<span data-ttu-id="97095-106">Send-Feedback cmdlet은 Azure PowerShell 팀에 피드백을 전송합니다.</span><span class="sxs-lookup"><span data-stu-id="97095-106">The Send-Feedback cmdlet sends feedback to the Azure PowerShell team.</span></span>

## <span data-ttu-id="97095-107">예제</span><span class="sxs-lookup"><span data-stu-id="97095-107">EXAMPLES</span></span>

### <span data-ttu-id="97095-108">예제 1:</span><span class="sxs-lookup"><span data-stu-id="97095-108">Example 1:</span></span>
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

## <span data-ttu-id="97095-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="97095-109">PARAMETERS</span></span>

### <span data-ttu-id="97095-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97095-110">-DefaultProfile</span></span>
<span data-ttu-id="97095-111">Azure와 통신하는 데 사용되는 자격 증명, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="97095-111">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97095-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97095-112">CommonParameters</span></span>
<span data-ttu-id="97095-113">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="97095-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97095-114">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97095-114">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97095-115">입력</span><span class="sxs-lookup"><span data-stu-id="97095-115">INPUTS</span></span>

### <span data-ttu-id="97095-116">없음</span><span class="sxs-lookup"><span data-stu-id="97095-116">None</span></span>

## <span data-ttu-id="97095-117">출력</span><span class="sxs-lookup"><span data-stu-id="97095-117">OUTPUTS</span></span>

### <span data-ttu-id="97095-118">System.Void</span><span class="sxs-lookup"><span data-stu-id="97095-118">System.Void</span></span>

## <span data-ttu-id="97095-119">참고 사항</span><span class="sxs-lookup"><span data-stu-id="97095-119">NOTES</span></span>

## <span data-ttu-id="97095-120">관련 링크</span><span class="sxs-lookup"><span data-stu-id="97095-120">RELATED LINKS</span></span>
