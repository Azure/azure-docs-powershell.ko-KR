---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/send-feedback
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Send-Feedback.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Send-Feedback.md
ms.openlocfilehash: 2541b4fb50decd83f2130a2d960fc4ecde007c57
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875264"
---
# <span data-ttu-id="2c313-101">Send-Feedback</span><span class="sxs-lookup"><span data-stu-id="2c313-101">Send-Feedback</span></span>

## <span data-ttu-id="2c313-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c313-102">SYNOPSIS</span></span>
<span data-ttu-id="2c313-103">안내 표시를 통해 Azure PowerShell 팀에 의견을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="2c313-103">Sends feedback to the Azure PowerShell team via a set of guided prompts.</span></span>

## <span data-ttu-id="2c313-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2c313-104">SYNTAX</span></span>

```
Send-Feedback [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c313-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2c313-105">DESCRIPTION</span></span>
<span data-ttu-id="2c313-106">Send-Feedback cmdlet은 Azure PowerShell 팀에 의견을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="2c313-106">The Send-Feedback cmdlet sends feedback to the Azure PowerShell team.</span></span>

## <span data-ttu-id="2c313-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2c313-107">EXAMPLES</span></span>

### <span data-ttu-id="2c313-108">예제 1:</span><span class="sxs-lookup"><span data-stu-id="2c313-108">Example 1:</span></span>
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

## <span data-ttu-id="2c313-109">변수</span><span class="sxs-lookup"><span data-stu-id="2c313-109">PARAMETERS</span></span>

### <span data-ttu-id="2c313-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c313-110">-DefaultProfile</span></span>
<span data-ttu-id="2c313-111">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c313-111">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c313-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c313-112">CommonParameters</span></span>
<span data-ttu-id="2c313-113">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c313-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c313-114">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2c313-114">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c313-115">입력</span><span class="sxs-lookup"><span data-stu-id="2c313-115">INPUTS</span></span>

### <span data-ttu-id="2c313-116">않아야</span><span class="sxs-lookup"><span data-stu-id="2c313-116">None</span></span>

## <span data-ttu-id="2c313-117">출력</span><span class="sxs-lookup"><span data-stu-id="2c313-117">OUTPUTS</span></span>

### <span data-ttu-id="2c313-118">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="2c313-118">System.Void</span></span>

## <span data-ttu-id="2c313-119">상속자</span><span class="sxs-lookup"><span data-stu-id="2c313-119">NOTES</span></span>

## <span data-ttu-id="2c313-120">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c313-120">RELATED LINKS</span></span>
