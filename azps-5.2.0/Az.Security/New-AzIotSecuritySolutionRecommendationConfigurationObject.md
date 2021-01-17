---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionRecommendationConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
ms.openlocfilehash: 448b72ce068c29e357db69abb45420157c3c1bf0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337317"
---
# <span data-ttu-id="b9f44-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="b9f44-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span></span>

## <span data-ttu-id="b9f44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9f44-102">SYNOPSIS</span></span>
<span data-ttu-id="b9f44-103">iot 보안 솔루션에 대한 새 권장 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="b9f44-103">Create new recommendation configuration for iot security solution</span></span>

## <span data-ttu-id="b9f44-104">구문</span><span class="sxs-lookup"><span data-stu-id="b9f44-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9f44-105">설명</span><span class="sxs-lookup"><span data-stu-id="b9f44-105">DESCRIPTION</span></span>
<span data-ttu-id="b9f44-106">AzIotSecuritySolutionRecommendationConfigurationObject는 iot 보안 솔루션에 대한 새 권장 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b9f44-106">The AzIotSecuritySolutionRecommendationConfigurationObject creates a new recommendation configuration object for iot security solution.</span></span>
<span data-ttu-id="b9f44-107">이러한 방식으로 권장 구성 상태는 사용하도록 설정되거나 비활성화되어 있는지 여부에 따라 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9f44-107">This way the status of a recommendation is configured, whether it is enabled or disabled.</span></span>

## <span data-ttu-id="b9f44-108">예제</span><span class="sxs-lookup"><span data-stu-id="b9f44-108">EXAMPLES</span></span>

### <span data-ttu-id="b9f44-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="b9f44-109">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_ACRAuthentication" -Enabled $false

RecommendationType: "IoT_ACRAuthentication"
Name: "Service prinicpal not used with ACR repository"
Status: "Disabled"
```

<span data-ttu-id="b9f44-110">상태가 비활성화로 설정된 "IoT_ACRAuthentication" 권장 유형에 대한 새 권장 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="b9f44-110">Create new recommendation configuration for recommendation type "IoT_ACRAuthentication" with status set to disable</span></span>

## <span data-ttu-id="b9f44-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9f44-111">PARAMETERS</span></span>

### <span data-ttu-id="b9f44-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9f44-112">-DefaultProfile</span></span>
<span data-ttu-id="b9f44-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b9f44-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9f44-114">-Enabled</span><span class="sxs-lookup"><span data-stu-id="b9f44-114">-Enabled</span></span>
<span data-ttu-id="b9f44-115">상태.</span><span class="sxs-lookup"><span data-stu-id="b9f44-115">Status .</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f44-116">-RecommendationType</span><span class="sxs-lookup"><span data-stu-id="b9f44-116">-RecommendationType</span></span>
<span data-ttu-id="b9f44-117">권장 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="b9f44-117">Recommendation type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f44-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9f44-118">CommonParameters</span></span>
<span data-ttu-id="b9f44-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b9f44-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9f44-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b9f44-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9f44-121">입력</span><span class="sxs-lookup"><span data-stu-id="b9f44-121">INPUTS</span></span>

### <span data-ttu-id="b9f44-122">없음</span><span class="sxs-lookup"><span data-stu-id="b9f44-122">None</span></span>

## <span data-ttu-id="b9f44-123">출력</span><span class="sxs-lookup"><span data-stu-id="b9f44-123">OUTPUTS</span></span>

### <span data-ttu-id="b9f44-124">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9f44-124">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration</span></span>

## <span data-ttu-id="b9f44-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b9f44-125">NOTES</span></span>

## <span data-ttu-id="b9f44-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b9f44-126">RELATED LINKS</span></span>
