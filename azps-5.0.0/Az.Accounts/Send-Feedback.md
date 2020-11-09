---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/send-feedback
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Send-Feedback.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Send-Feedback.md
ms.openlocfilehash: 1405886572efabf1ffc91f071f262ca98515d141
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307769"
---
# <span data-ttu-id="91ce4-101">Send-Feedback</span><span class="sxs-lookup"><span data-stu-id="91ce4-101">Send-Feedback</span></span>

## <span data-ttu-id="91ce4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91ce4-102">SYNOPSIS</span></span>
<span data-ttu-id="91ce4-103">안내 표시를 통해 Azure PowerShell 팀에 의견을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="91ce4-103">Sends feedback to the Azure PowerShell team via a set of guided prompts.</span></span>

## <span data-ttu-id="91ce4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="91ce4-104">SYNTAX</span></span>

```
Send-Feedback [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91ce4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="91ce4-105">DESCRIPTION</span></span>
<span data-ttu-id="91ce4-106">Send-Feedback cmdlet은 Azure PowerShell 팀에 의견을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="91ce4-106">The Send-Feedback cmdlet sends feedback to the Azure PowerShell team.</span></span>

## <span data-ttu-id="91ce4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="91ce4-107">EXAMPLES</span></span>

### <span data-ttu-id="91ce4-108">예제 1:</span><span class="sxs-lookup"><span data-stu-id="91ce4-108">Example 1:</span></span>
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

## <span data-ttu-id="91ce4-109">변수</span><span class="sxs-lookup"><span data-stu-id="91ce4-109">PARAMETERS</span></span>

### <span data-ttu-id="91ce4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91ce4-110">-DefaultProfile</span></span>
<span data-ttu-id="91ce4-111">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91ce4-111">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91ce4-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91ce4-112">CommonParameters</span></span>
<span data-ttu-id="91ce4-113">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="91ce4-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91ce4-114">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91ce4-114">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91ce4-115">입력</span><span class="sxs-lookup"><span data-stu-id="91ce4-115">INPUTS</span></span>

### <span data-ttu-id="91ce4-116">않아야</span><span class="sxs-lookup"><span data-stu-id="91ce4-116">None</span></span>

## <span data-ttu-id="91ce4-117">출력</span><span class="sxs-lookup"><span data-stu-id="91ce4-117">OUTPUTS</span></span>

### <span data-ttu-id="91ce4-118">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="91ce4-118">System.Void</span></span>

## <span data-ttu-id="91ce4-119">상속자</span><span class="sxs-lookup"><span data-stu-id="91ce4-119">NOTES</span></span>

## <span data-ttu-id="91ce4-120">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91ce4-120">RELATED LINKS</span></span>
