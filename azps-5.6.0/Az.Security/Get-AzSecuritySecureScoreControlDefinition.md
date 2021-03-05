---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySecureScoreControlDefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
ms.openlocfilehash: e8ec0073eef8b8db95197e19f2bfd61d0bbcdafd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995913"
---
# <span data-ttu-id="b5fc8-101">Get-AzSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="b5fc8-101">Get-AzSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="b5fc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5fc8-102">SYNOPSIS</span></span>
<span data-ttu-id="b5fc8-103">구독에서 보안 보안 점수 제어 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b5fc8-103">Gets security secure score control definitions on a subscription</span></span>

## <span data-ttu-id="b5fc8-104">구문</span><span class="sxs-lookup"><span data-stu-id="b5fc8-104">SYNTAX</span></span>

### <span data-ttu-id="b5fc8-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="b5fc8-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControlDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5fc8-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="b5fc8-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControlDefinition -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5fc8-107">예제</span><span class="sxs-lookup"><span data-stu-id="b5fc8-107">EXAMPLES</span></span>

### <span data-ttu-id="b5fc8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b5fc8-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControlDefinition
```

<span data-ttu-id="b5fc8-109">구독의 모든 보안 보안 점수 제어 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b5fc8-109">Gets all the security secure score control definitions in a subscription</span></span>

## <span data-ttu-id="b5fc8-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b5fc8-110">PARAMETERS</span></span>

### <span data-ttu-id="b5fc8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5fc8-111">-DefaultProfile</span></span>
<span data-ttu-id="b5fc8-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b5fc8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fc8-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5fc8-113">CommonParameters</span></span>
<span data-ttu-id="b5fc8-114">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b5fc8-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5fc8-115">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5fc8-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5fc8-116">입력</span><span class="sxs-lookup"><span data-stu-id="b5fc8-116">INPUTS</span></span>

### <span data-ttu-id="b5fc8-117">System.String</span><span class="sxs-lookup"><span data-stu-id="b5fc8-117">System.String</span></span>

## <span data-ttu-id="b5fc8-118">출력</span><span class="sxs-lookup"><span data-stu-id="b5fc8-118">OUTPUTS</span></span>

### <span data-ttu-id="b5fc8-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="b5fc8-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="b5fc8-120">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b5fc8-120">NOTES</span></span>

## <span data-ttu-id="b5fc8-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b5fc8-121">RELATED LINKS</span></span>
