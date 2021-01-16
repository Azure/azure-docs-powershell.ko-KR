---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
ms.openlocfilehash: 524a10f910b6e0d1b247f74a0b99063cbecba65c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360704"
---
# <span data-ttu-id="b450e-101">Get-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="b450e-101">Get-AzSecurityAssessment</span></span>

## <span data-ttu-id="b450e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b450e-102">SYNOPSIS</span></span>
<span data-ttu-id="b450e-103">구독에 대한 보안 평가 및 결과를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b450e-103">Gets security assessments and their results on a subscription</span></span>

## <span data-ttu-id="b450e-104">구문</span><span class="sxs-lookup"><span data-stu-id="b450e-104">SYNTAX</span></span>

### <span data-ttu-id="b450e-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="b450e-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessment [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b450e-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="b450e-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessment -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b450e-107">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="b450e-107">ResourceIdScope</span></span>
```
Get-AzSecurityAssessment -Name <String> -AssessedResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b450e-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b450e-108">ResourceId</span></span>
```
Get-AzSecurityAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b450e-109">설명</span><span class="sxs-lookup"><span data-stu-id="b450e-109">DESCRIPTION</span></span>
<span data-ttu-id="b450e-110">구독에 대한 보안 평가 및 결과를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b450e-110">Gets security assessment and their results on subscription.</span></span> <span data-ttu-id="b450e-111">보안 평가를 통해 Azure 구독에서 완화할 Azure Security Center에서 다시 요구하는 모범 사례를 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b450e-111">Security assessments will let you know which best practices are recommanded by Azure Security Center to be mitigated on your Azure subscription.</span></span>

## <span data-ttu-id="b450e-112">예제</span><span class="sxs-lookup"><span data-stu-id="b450e-112">EXAMPLES</span></span>

### <span data-ttu-id="b450e-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="b450e-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessment
```

<span data-ttu-id="b450e-114">구독의 모든 보안 평가를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b450e-114">Gets all the security assessment in a subscription</span></span>

## <span data-ttu-id="b450e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b450e-115">PARAMETERS</span></span>

### <span data-ttu-id="b450e-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="b450e-116">-AssessedResourceId</span></span>
<span data-ttu-id="b450e-117">평가가 계산된 리소스의 전체 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b450e-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b450e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b450e-118">-DefaultProfile</span></span>
<span data-ttu-id="b450e-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b450e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b450e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b450e-120">-Name</span></span>
<span data-ttu-id="b450e-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b450e-121">Resource name.</span></span>

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

```yaml
Type: String
Parameter Sets: ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b450e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b450e-122">-ResourceId</span></span>
<span data-ttu-id="b450e-123">명령을 호출하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b450e-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="b450e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b450e-124">CommonParameters</span></span>
<span data-ttu-id="b450e-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b450e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b450e-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b450e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b450e-127">입력</span><span class="sxs-lookup"><span data-stu-id="b450e-127">INPUTS</span></span>

### <span data-ttu-id="b450e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b450e-128">System.String</span></span>

## <span data-ttu-id="b450e-129">출력</span><span class="sxs-lookup"><span data-stu-id="b450e-129">OUTPUTS</span></span>

### <span data-ttu-id="b450e-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="b450e-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="b450e-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b450e-131">NOTES</span></span>

## <span data-ttu-id="b450e-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b450e-132">RELATED LINKS</span></span>
