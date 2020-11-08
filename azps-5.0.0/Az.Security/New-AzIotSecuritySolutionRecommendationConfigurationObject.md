---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionRecommendationConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
ms.openlocfilehash: 448b72ce068c29e357db69abb45420157c3c1bf0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216194"
---
# <span data-ttu-id="83627-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="83627-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span></span>

## <span data-ttu-id="83627-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83627-102">SYNOPSIS</span></span>
<span data-ttu-id="83627-103">Iot security 솔루션에 대 한 새 권장 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="83627-103">Create new recommendation configuration for iot security solution</span></span>

## <span data-ttu-id="83627-104">구문과</span><span class="sxs-lookup"><span data-stu-id="83627-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83627-105">설명은</span><span class="sxs-lookup"><span data-stu-id="83627-105">DESCRIPTION</span></span>
<span data-ttu-id="83627-106">AzIotSecuritySolutionRecommendationConfigurationObject는 iot security 솔루션에 대 한 새 권장 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="83627-106">The AzIotSecuritySolutionRecommendationConfigurationObject creates a new recommendation configuration object for iot security solution.</span></span>
<span data-ttu-id="83627-107">이 방법으로 사용 여부에 관계 없이 권장 구성의 상태를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83627-107">This way the status of a recommendation is configured, whether it is enabled or disabled.</span></span>

## <span data-ttu-id="83627-108">예제의</span><span class="sxs-lookup"><span data-stu-id="83627-108">EXAMPLES</span></span>

### <span data-ttu-id="83627-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="83627-109">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_ACRAuthentication" -Enabled $false

RecommendationType: "IoT_ACRAuthentication"
Name: "Service prinicpal not used with ACR repository"
Status: "Disabled"
```

<span data-ttu-id="83627-110">제안 유형을 사용 하지 않도록 설정 하 여 "IoT_ACRAuthentication"를 추천 하는 새 권장 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="83627-110">Create new recommendation configuration for recommendation type "IoT_ACRAuthentication" with status set to disable</span></span>

## <span data-ttu-id="83627-111">변수</span><span class="sxs-lookup"><span data-stu-id="83627-111">PARAMETERS</span></span>

### <span data-ttu-id="83627-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83627-112">-DefaultProfile</span></span>
<span data-ttu-id="83627-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="83627-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83627-114">-사용</span><span class="sxs-lookup"><span data-stu-id="83627-114">-Enabled</span></span>
<span data-ttu-id="83627-115">상태.</span><span class="sxs-lookup"><span data-stu-id="83627-115">Status .</span></span>

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

### <span data-ttu-id="83627-116">-RecommendationType</span><span class="sxs-lookup"><span data-stu-id="83627-116">-RecommendationType</span></span>
<span data-ttu-id="83627-117">추천 유형.</span><span class="sxs-lookup"><span data-stu-id="83627-117">Recommendation type.</span></span>

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

### <span data-ttu-id="83627-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83627-118">CommonParameters</span></span>
<span data-ttu-id="83627-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="83627-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83627-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="83627-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83627-121">입력</span><span class="sxs-lookup"><span data-stu-id="83627-121">INPUTS</span></span>

### <span data-ttu-id="83627-122">않아야</span><span class="sxs-lookup"><span data-stu-id="83627-122">None</span></span>

## <span data-ttu-id="83627-123">출력</span><span class="sxs-lookup"><span data-stu-id="83627-123">OUTPUTS</span></span>

### <span data-ttu-id="83627-124">Microsoft. Azure. IPSRecommendationConfiguration Securitysolutions.</span><span class="sxs-lookup"><span data-stu-id="83627-124">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration</span></span>

## <span data-ttu-id="83627-125">상속자</span><span class="sxs-lookup"><span data-stu-id="83627-125">NOTES</span></span>

## <span data-ttu-id="83627-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83627-126">RELATED LINKS</span></span>
