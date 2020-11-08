---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
ms.openlocfilehash: 524a10f910b6e0d1b247f74a0b99063cbecba65c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048758"
---
# <span data-ttu-id="12a9e-101">Get-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="12a9e-101">Get-AzSecurityAssessment</span></span>

## <span data-ttu-id="12a9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12a9e-102">SYNOPSIS</span></span>
<span data-ttu-id="12a9e-103">구독에서 보안 평가 및 해당 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="12a9e-103">Gets security assessments and their results on a subscription</span></span>

## <span data-ttu-id="12a9e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="12a9e-104">SYNTAX</span></span>

### <span data-ttu-id="12a9e-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="12a9e-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessment [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12a9e-106">구독 Levelresource</span><span class="sxs-lookup"><span data-stu-id="12a9e-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessment -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12a9e-107">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="12a9e-107">ResourceIdScope</span></span>
```
Get-AzSecurityAssessment -Name <String> -AssessedResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12a9e-108">리소스</span><span class="sxs-lookup"><span data-stu-id="12a9e-108">ResourceId</span></span>
```
Get-AzSecurityAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12a9e-109">설명은</span><span class="sxs-lookup"><span data-stu-id="12a9e-109">DESCRIPTION</span></span>
<span data-ttu-id="12a9e-110">구독에서 보안 평가 및 해당 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="12a9e-110">Gets security assessment and their results on subscription.</span></span> <span data-ttu-id="12a9e-111">보안 평가를 통해 azure 구독에서 완화 하기 위해 Azure 보안 센터에서 다시 실행 하는 모범 사례를 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="12a9e-111">Security assessments will let you know which best practices are recommanded by Azure Security Center to be mitigated on your Azure subscription.</span></span>

## <span data-ttu-id="12a9e-112">예제의</span><span class="sxs-lookup"><span data-stu-id="12a9e-112">EXAMPLES</span></span>

### <span data-ttu-id="12a9e-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="12a9e-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessment
```

<span data-ttu-id="12a9e-114">구독의 모든 보안 평가를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="12a9e-114">Gets all the security assessment in a subscription</span></span>

## <span data-ttu-id="12a9e-115">변수</span><span class="sxs-lookup"><span data-stu-id="12a9e-115">PARAMETERS</span></span>

### <span data-ttu-id="12a9e-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="12a9e-116">-AssessedResourceId</span></span>
<span data-ttu-id="12a9e-117">평가를 계산할 리소스의 전체 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="12a9e-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="12a9e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12a9e-118">-DefaultProfile</span></span>
<span data-ttu-id="12a9e-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="12a9e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12a9e-120">-이름</span><span class="sxs-lookup"><span data-stu-id="12a9e-120">-Name</span></span>
<span data-ttu-id="12a9e-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="12a9e-121">Resource name.</span></span>

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

### <span data-ttu-id="12a9e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12a9e-122">-ResourceId</span></span>
<span data-ttu-id="12a9e-123">명령을 호출 하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="12a9e-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="12a9e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12a9e-124">CommonParameters</span></span>
<span data-ttu-id="12a9e-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="12a9e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12a9e-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="12a9e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12a9e-127">입력</span><span class="sxs-lookup"><span data-stu-id="12a9e-127">INPUTS</span></span>

### <span data-ttu-id="12a9e-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="12a9e-128">System.String</span></span>

## <span data-ttu-id="12a9e-129">출력</span><span class="sxs-lookup"><span data-stu-id="12a9e-129">OUTPUTS</span></span>

### <span data-ttu-id="12a9e-130">Microsoft. Azure. a. PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="12a9e-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="12a9e-131">상속자</span><span class="sxs-lookup"><span data-stu-id="12a9e-131">NOTES</span></span>

## <span data-ttu-id="12a9e-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="12a9e-132">RELATED LINKS</span></span>
