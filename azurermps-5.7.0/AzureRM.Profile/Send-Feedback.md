---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/send-feedback
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Send-Feedback.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Send-Feedback.md
ms.openlocfilehash: 471178f6b35ea3a382c02a2a0970d0a9466b43ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532692"
---
# <span data-ttu-id="52222-101">Send-Feedback</span><span class="sxs-lookup"><span data-stu-id="52222-101">Send-Feedback</span></span>

## <span data-ttu-id="52222-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52222-102">SYNOPSIS</span></span>
<span data-ttu-id="52222-103">안내 표시를 통해 Azure PowerShell 팀에 의견을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="52222-103">Sends feedback to the Azure PowerShell team via a set of guided prompts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52222-104">구문과</span><span class="sxs-lookup"><span data-stu-id="52222-104">SYNTAX</span></span>

```
Send-Feedback [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52222-105">설명은</span><span class="sxs-lookup"><span data-stu-id="52222-105">DESCRIPTION</span></span>
<span data-ttu-id="52222-106">Send-Feedback cmdlet은 Azure PowerShell 팀에 의견을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="52222-106">The Send-Feedback cmdlet sends feedback to the Azure PowerShell team.</span></span>

## <span data-ttu-id="52222-107">예제의</span><span class="sxs-lookup"><span data-stu-id="52222-107">EXAMPLES</span></span>

### <span data-ttu-id="52222-108">예제 1:</span><span class="sxs-lookup"><span data-stu-id="52222-108">Example 1:</span></span>
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

## <span data-ttu-id="52222-109">변수</span><span class="sxs-lookup"><span data-stu-id="52222-109">PARAMETERS</span></span>

### <span data-ttu-id="52222-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52222-110">-DefaultProfile</span></span>
<span data-ttu-id="52222-111">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="52222-111">The credentials, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52222-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52222-112">CommonParameters</span></span>
<span data-ttu-id="52222-113">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="52222-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52222-114">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52222-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52222-115">입력</span><span class="sxs-lookup"><span data-stu-id="52222-115">INPUTS</span></span>

### <span data-ttu-id="52222-116">않아야</span><span class="sxs-lookup"><span data-stu-id="52222-116">None</span></span>
<span data-ttu-id="52222-117">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="52222-117">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="52222-118">출력</span><span class="sxs-lookup"><span data-stu-id="52222-118">OUTPUTS</span></span>

### <span data-ttu-id="52222-119">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="52222-119">System.Void</span></span>

## <span data-ttu-id="52222-120">상속자</span><span class="sxs-lookup"><span data-stu-id="52222-120">NOTES</span></span>

## <span data-ttu-id="52222-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="52222-121">RELATED LINKS</span></span>

