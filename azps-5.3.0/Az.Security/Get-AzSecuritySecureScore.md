---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
ms.openlocfilehash: 5b14298f48c5723b4d84b0f22d799ac0a21699e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494999"
---
# <span data-ttu-id="d5083-101">Get-AzSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="d5083-101">Get-AzSecuritySecureScore</span></span>

## <span data-ttu-id="d5083-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5083-102">SYNOPSIS</span></span>
<span data-ttu-id="d5083-103">구독에서 보안 보안 점수 및 결과를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d5083-103">Gets security secure scores and their results on a subscription</span></span>

## <span data-ttu-id="d5083-104">구문</span><span class="sxs-lookup"><span data-stu-id="d5083-104">SYNTAX</span></span>

### <span data-ttu-id="d5083-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="d5083-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5083-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="d5083-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScore -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5083-107">예제</span><span class="sxs-lookup"><span data-stu-id="d5083-107">EXAMPLES</span></span>

### <span data-ttu-id="d5083-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d5083-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScore
```

<span data-ttu-id="d5083-109">구독의 모든 보안 보안 점수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d5083-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="d5083-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5083-110">PARAMETERS</span></span>

### <span data-ttu-id="d5083-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5083-111">-DefaultProfile</span></span>
<span data-ttu-id="d5083-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d5083-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5083-113">-Name</span><span class="sxs-lookup"><span data-stu-id="d5083-113">-Name</span></span>
<span data-ttu-id="d5083-114">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5083-114">Resource name.</span></span>

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

### <span data-ttu-id="d5083-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5083-115">CommonParameters</span></span>
<span data-ttu-id="d5083-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d5083-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5083-117">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d5083-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5083-118">입력</span><span class="sxs-lookup"><span data-stu-id="d5083-118">INPUTS</span></span>

### <span data-ttu-id="d5083-119">System.String</span><span class="sxs-lookup"><span data-stu-id="d5083-119">System.String</span></span>

## <span data-ttu-id="d5083-120">출력</span><span class="sxs-lookup"><span data-stu-id="d5083-120">OUTPUTS</span></span>

### <span data-ttu-id="d5083-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="d5083-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScore</span></span>

## <span data-ttu-id="d5083-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d5083-122">NOTES</span></span>

## <span data-ttu-id="d5083-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5083-123">RELATED LINKS</span></span>
