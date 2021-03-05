---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySecureScoreControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
ms.openlocfilehash: 497865446e943fc34f45f6c98713d559086cca84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979307"
---
# <span data-ttu-id="2ef09-101">Get-AzSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="2ef09-101">Get-AzSecuritySecureScoreControl</span></span>

## <span data-ttu-id="2ef09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ef09-102">SYNOPSIS</span></span>
<span data-ttu-id="2ef09-103">구독에서 보안 보안 점수 컨트롤 및 그 결과를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef09-103">Gets security secure score controls and their results on a subscription</span></span>

## <span data-ttu-id="2ef09-104">구문</span><span class="sxs-lookup"><span data-stu-id="2ef09-104">SYNTAX</span></span>

### <span data-ttu-id="2ef09-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="2ef09-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControl [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ef09-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="2ef09-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControl -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ef09-107">예제</span><span class="sxs-lookup"><span data-stu-id="2ef09-107">EXAMPLES</span></span>

### <span data-ttu-id="2ef09-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2ef09-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControl
```

<span data-ttu-id="2ef09-109">구독의 모든 보안 보안 점수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef09-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="2ef09-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2ef09-110">PARAMETERS</span></span>

### <span data-ttu-id="2ef09-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ef09-111">-DefaultProfile</span></span>
<span data-ttu-id="2ef09-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2ef09-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ef09-113">-Name</span><span class="sxs-lookup"><span data-stu-id="2ef09-113">-Name</span></span>
<span data-ttu-id="2ef09-114">점수 이름 보호.</span><span class="sxs-lookup"><span data-stu-id="2ef09-114">Secure score name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ef09-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ef09-115">CommonParameters</span></span>
<span data-ttu-id="2ef09-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef09-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ef09-117">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ef09-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ef09-118">입력</span><span class="sxs-lookup"><span data-stu-id="2ef09-118">INPUTS</span></span>

### <span data-ttu-id="2ef09-119">System.String</span><span class="sxs-lookup"><span data-stu-id="2ef09-119">System.String</span></span>

## <span data-ttu-id="2ef09-120">출력</span><span class="sxs-lookup"><span data-stu-id="2ef09-120">OUTPUTS</span></span>

### <span data-ttu-id="2ef09-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="2ef09-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControl</span></span>

## <span data-ttu-id="2ef09-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2ef09-122">NOTES</span></span>

## <span data-ttu-id="2ef09-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2ef09-123">RELATED LINKS</span></span>
