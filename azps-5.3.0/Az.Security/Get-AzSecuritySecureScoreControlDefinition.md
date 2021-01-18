---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScoreControlDefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
ms.openlocfilehash: 557e048dcce528b4c84f6d1b74915d81d6c6f0c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494998"
---
# <span data-ttu-id="46fb3-101">Get-AzSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="46fb3-101">Get-AzSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="46fb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46fb3-102">SYNOPSIS</span></span>
<span data-ttu-id="46fb3-103">구독에서 보안 보안 점수 제어 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="46fb3-103">Gets security secure score control definitions on a subscription</span></span>

## <span data-ttu-id="46fb3-104">구문</span><span class="sxs-lookup"><span data-stu-id="46fb3-104">SYNTAX</span></span>

### <span data-ttu-id="46fb3-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="46fb3-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControlDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46fb3-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="46fb3-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControlDefinition -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46fb3-107">예제</span><span class="sxs-lookup"><span data-stu-id="46fb3-107">EXAMPLES</span></span>

### <span data-ttu-id="46fb3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="46fb3-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControlDefinition
```

<span data-ttu-id="46fb3-109">구독의 모든 보안 보안 점수 제어 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="46fb3-109">Gets all the security secure score control definitions in a subscription</span></span>

## <span data-ttu-id="46fb3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46fb3-110">PARAMETERS</span></span>

### <span data-ttu-id="46fb3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46fb3-111">-DefaultProfile</span></span>
<span data-ttu-id="46fb3-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="46fb3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46fb3-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46fb3-113">CommonParameters</span></span>
<span data-ttu-id="46fb3-114">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="46fb3-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46fb3-115">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="46fb3-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46fb3-116">입력</span><span class="sxs-lookup"><span data-stu-id="46fb3-116">INPUTS</span></span>

### <span data-ttu-id="46fb3-117">System.String</span><span class="sxs-lookup"><span data-stu-id="46fb3-117">System.String</span></span>

## <span data-ttu-id="46fb3-118">출력</span><span class="sxs-lookup"><span data-stu-id="46fb3-118">OUTPUTS</span></span>

### <span data-ttu-id="46fb3-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="46fb3-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="46fb3-120">참고 사항</span><span class="sxs-lookup"><span data-stu-id="46fb3-120">NOTES</span></span>

## <span data-ttu-id="46fb3-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46fb3-121">RELATED LINKS</span></span>
