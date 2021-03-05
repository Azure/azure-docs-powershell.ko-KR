---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: 92858967d460785af151520c504a4e1cbdb4d3d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008523"
---
# <span data-ttu-id="82a82-101">Get-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="82a82-101">Get-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="82a82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82a82-102">SYNOPSIS</span></span>
<span data-ttu-id="82a82-103">구독에서 보안 평가 유형 및 metadta를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="82a82-103">Gets security assessments types and metadta in a subscription.</span></span>

## <span data-ttu-id="82a82-104">구문</span><span class="sxs-lookup"><span data-stu-id="82a82-104">SYNTAX</span></span>

### <span data-ttu-id="82a82-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="82a82-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessmentMetadata [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82a82-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="82a82-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessmentMetadata -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82a82-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="82a82-107">ResourceId</span></span>
```
Get-AzSecurityAssessmentMetadata -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="82a82-108">설명</span><span class="sxs-lookup"><span data-stu-id="82a82-108">DESCRIPTION</span></span>
<span data-ttu-id="82a82-109">구독에서 보안 평가 유형 및 metadta를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="82a82-109">Gets security assessments types and metadta in a subscription.</span></span> <span data-ttu-id="82a82-110">보안 평가 메타데이터에는 사용자가 Built-In 평가 및 사용자 지정 평가 형식이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="82a82-110">Security Assessment metadata include Built-In assessments and custom assessment types that the user can define.</span></span>

## <span data-ttu-id="82a82-111">예제</span><span class="sxs-lookup"><span data-stu-id="82a82-111">EXAMPLES</span></span>

### <span data-ttu-id="82a82-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="82a82-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessmentMetadata
```

<span data-ttu-id="82a82-113">기본 제공 평가 및 현재 구독에 구성된 사용자 지정 평가를 모두 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="82a82-113">Gets all the built in assessments and the custom assessments that were configured on the current subscription.</span></span>

## <span data-ttu-id="82a82-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="82a82-114">PARAMETERS</span></span>

### <span data-ttu-id="82a82-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82a82-115">-DefaultProfile</span></span>
<span data-ttu-id="82a82-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82a82-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82a82-117">-Name</span><span class="sxs-lookup"><span data-stu-id="82a82-117">-Name</span></span>
<span data-ttu-id="82a82-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82a82-118">Resource name.</span></span>

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

### <span data-ttu-id="82a82-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82a82-119">-ResourceId</span></span>
<span data-ttu-id="82a82-120">명령을 호출할 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="82a82-120">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82a82-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82a82-121">CommonParameters</span></span>
<span data-ttu-id="82a82-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="82a82-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82a82-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82a82-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82a82-124">입력</span><span class="sxs-lookup"><span data-stu-id="82a82-124">INPUTS</span></span>

### <span data-ttu-id="82a82-125">System.String</span><span class="sxs-lookup"><span data-stu-id="82a82-125">System.String</span></span>

## <span data-ttu-id="82a82-126">출력</span><span class="sxs-lookup"><span data-stu-id="82a82-126">OUTPUTS</span></span>

### <span data-ttu-id="82a82-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="82a82-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="82a82-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="82a82-128">NOTES</span></span>

## <span data-ttu-id="82a82-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82a82-129">RELATED LINKS</span></span>
