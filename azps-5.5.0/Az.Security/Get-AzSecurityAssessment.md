---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
ms.openlocfilehash: 524a10f910b6e0d1b247f74a0b99063cbecba65c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208333"
---
# <span data-ttu-id="3276f-101">Get-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="3276f-101">Get-AzSecurityAssessment</span></span>

## <span data-ttu-id="3276f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3276f-102">SYNOPSIS</span></span>
<span data-ttu-id="3276f-103">구독에 대한 보안 평가 및 결과를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3276f-103">Gets security assessments and their results on a subscription</span></span>

## <span data-ttu-id="3276f-104">구문</span><span class="sxs-lookup"><span data-stu-id="3276f-104">SYNTAX</span></span>

### <span data-ttu-id="3276f-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="3276f-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessment [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3276f-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="3276f-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessment -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3276f-107">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="3276f-107">ResourceIdScope</span></span>
```
Get-AzSecurityAssessment -Name <String> -AssessedResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3276f-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3276f-108">ResourceId</span></span>
```
Get-AzSecurityAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3276f-109">설명</span><span class="sxs-lookup"><span data-stu-id="3276f-109">DESCRIPTION</span></span>
<span data-ttu-id="3276f-110">구독에 대한 보안 평가 및 결과를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3276f-110">Gets security assessment and their results on subscription.</span></span> <span data-ttu-id="3276f-111">보안 평가를 통해 Azure 구독에서 완화할 Azure Security Center에서 다시 요구하는 모범 사례를 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3276f-111">Security assessments will let you know which best practices are recommanded by Azure Security Center to be mitigated on your Azure subscription.</span></span>

## <span data-ttu-id="3276f-112">예제</span><span class="sxs-lookup"><span data-stu-id="3276f-112">EXAMPLES</span></span>

### <span data-ttu-id="3276f-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="3276f-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessment
```

<span data-ttu-id="3276f-114">구독의 모든 보안 평가를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3276f-114">Gets all the security assessment in a subscription</span></span>

## <span data-ttu-id="3276f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3276f-115">PARAMETERS</span></span>

### <span data-ttu-id="3276f-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="3276f-116">-AssessedResourceId</span></span>
<span data-ttu-id="3276f-117">평가가 계산된 리소스의 전체 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3276f-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="3276f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3276f-118">-DefaultProfile</span></span>
<span data-ttu-id="3276f-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3276f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3276f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3276f-120">-Name</span></span>
<span data-ttu-id="3276f-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3276f-121">Resource name.</span></span>

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

### <span data-ttu-id="3276f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3276f-122">-ResourceId</span></span>
<span data-ttu-id="3276f-123">명령을 호출하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3276f-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="3276f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3276f-124">CommonParameters</span></span>
<span data-ttu-id="3276f-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3276f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3276f-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3276f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3276f-127">입력</span><span class="sxs-lookup"><span data-stu-id="3276f-127">INPUTS</span></span>

### <span data-ttu-id="3276f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="3276f-128">System.String</span></span>

## <span data-ttu-id="3276f-129">출력</span><span class="sxs-lookup"><span data-stu-id="3276f-129">OUTPUTS</span></span>

### <span data-ttu-id="3276f-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="3276f-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="3276f-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3276f-131">NOTES</span></span>

## <span data-ttu-id="3276f-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3276f-132">RELATED LINKS</span></span>
