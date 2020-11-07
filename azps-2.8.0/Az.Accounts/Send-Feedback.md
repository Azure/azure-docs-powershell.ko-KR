---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/send-feedback
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Send-Feedback.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Send-Feedback.md
ms.openlocfilehash: 3dae531f23e5ef5e8ea800cf935a3b9f413ae640
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698226"
---
# <span data-ttu-id="f20de-101">Send-Feedback</span><span class="sxs-lookup"><span data-stu-id="f20de-101">Send-Feedback</span></span>

## <span data-ttu-id="f20de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f20de-102">SYNOPSIS</span></span>
<span data-ttu-id="f20de-103">안내 표시를 통해 Azure PowerShell 팀에 의견을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="f20de-103">Sends feedback to the Azure PowerShell team via a set of guided prompts.</span></span>

## <span data-ttu-id="f20de-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f20de-104">SYNTAX</span></span>

```
Send-Feedback [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f20de-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f20de-105">DESCRIPTION</span></span>
<span data-ttu-id="f20de-106">Send-Feedback cmdlet은 Azure PowerShell 팀에 의견을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="f20de-106">The Send-Feedback cmdlet sends feedback to the Azure PowerShell team.</span></span>

## <span data-ttu-id="f20de-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f20de-107">EXAMPLES</span></span>

### <span data-ttu-id="f20de-108">예제 1:</span><span class="sxs-lookup"><span data-stu-id="f20de-108">Example 1:</span></span>
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

## <span data-ttu-id="f20de-109">변수</span><span class="sxs-lookup"><span data-stu-id="f20de-109">PARAMETERS</span></span>

### <span data-ttu-id="f20de-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f20de-110">-DefaultProfile</span></span>
<span data-ttu-id="f20de-111">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f20de-111">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f20de-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f20de-112">CommonParameters</span></span>
<span data-ttu-id="f20de-113">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f20de-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f20de-114">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f20de-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f20de-115">입력</span><span class="sxs-lookup"><span data-stu-id="f20de-115">INPUTS</span></span>

### <span data-ttu-id="f20de-116">않아야</span><span class="sxs-lookup"><span data-stu-id="f20de-116">None</span></span>

## <span data-ttu-id="f20de-117">출력</span><span class="sxs-lookup"><span data-stu-id="f20de-117">OUTPUTS</span></span>

### <span data-ttu-id="f20de-118">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="f20de-118">System.Void</span></span>

## <span data-ttu-id="f20de-119">상속자</span><span class="sxs-lookup"><span data-stu-id="f20de-119">NOTES</span></span>

## <span data-ttu-id="f20de-120">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f20de-120">RELATED LINKS</span></span>
