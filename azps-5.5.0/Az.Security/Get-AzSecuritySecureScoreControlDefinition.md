---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScoreControlDefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
ms.openlocfilehash: 557e048dcce528b4c84f6d1b74915d81d6c6f0c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189140"
---
# <span data-ttu-id="fd40e-101">Get-AzSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="fd40e-101">Get-AzSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="fd40e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd40e-102">SYNOPSIS</span></span>
<span data-ttu-id="fd40e-103">구독에서 보안 보안 점수 제어 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fd40e-103">Gets security secure score control definitions on a subscription</span></span>

## <span data-ttu-id="fd40e-104">구문</span><span class="sxs-lookup"><span data-stu-id="fd40e-104">SYNTAX</span></span>

### <span data-ttu-id="fd40e-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="fd40e-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControlDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd40e-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="fd40e-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControlDefinition -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd40e-107">예제</span><span class="sxs-lookup"><span data-stu-id="fd40e-107">EXAMPLES</span></span>

### <span data-ttu-id="fd40e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fd40e-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControlDefinition
```

<span data-ttu-id="fd40e-109">구독의 모든 보안 보안 점수 제어 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fd40e-109">Gets all the security secure score control definitions in a subscription</span></span>

## <span data-ttu-id="fd40e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd40e-110">PARAMETERS</span></span>

### <span data-ttu-id="fd40e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd40e-111">-DefaultProfile</span></span>
<span data-ttu-id="fd40e-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd40e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd40e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd40e-113">CommonParameters</span></span>
<span data-ttu-id="fd40e-114">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fd40e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd40e-115">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fd40e-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd40e-116">입력</span><span class="sxs-lookup"><span data-stu-id="fd40e-116">INPUTS</span></span>

### <span data-ttu-id="fd40e-117">System.String</span><span class="sxs-lookup"><span data-stu-id="fd40e-117">System.String</span></span>

## <span data-ttu-id="fd40e-118">출력</span><span class="sxs-lookup"><span data-stu-id="fd40e-118">OUTPUTS</span></span>

### <span data-ttu-id="fd40e-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="fd40e-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="fd40e-120">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fd40e-120">NOTES</span></span>

## <span data-ttu-id="fd40e-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd40e-121">RELATED LINKS</span></span>
