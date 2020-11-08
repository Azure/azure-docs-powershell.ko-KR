---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: 6b2819041b9fd136ee1ecc65b9d8b36132af5317
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048757"
---
# <span data-ttu-id="88f47-101">Get-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="88f47-101">Get-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="88f47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88f47-102">SYNOPSIS</span></span>
<span data-ttu-id="88f47-103">구독에서 보안 평가 유형 및 metadta를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="88f47-103">Gets security assessments types and metadta in a subscription.</span></span>

## <span data-ttu-id="88f47-104">구문과</span><span class="sxs-lookup"><span data-stu-id="88f47-104">SYNTAX</span></span>

### <span data-ttu-id="88f47-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="88f47-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessmentMetadata [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88f47-106">구독 Levelresource</span><span class="sxs-lookup"><span data-stu-id="88f47-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessmentMetadata -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88f47-107">리소스</span><span class="sxs-lookup"><span data-stu-id="88f47-107">ResourceId</span></span>
```
Get-AzSecurityAssessmentMetadata -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88f47-108">설명은</span><span class="sxs-lookup"><span data-stu-id="88f47-108">DESCRIPTION</span></span>
<span data-ttu-id="88f47-109">구독에서 보안 평가 유형 및 metadta를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="88f47-109">Gets security assessments types and metadta in a subscription.</span></span> <span data-ttu-id="88f47-110">보안 평가 메타 데이터에는 사용자가 정의할 수 있는 Built-In 평가 및 사용자 지정 평가 유형이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="88f47-110">Security Assessment metadata include Built-In assessments and custom assessment types that the user can define.</span></span>

## <span data-ttu-id="88f47-111">예제의</span><span class="sxs-lookup"><span data-stu-id="88f47-111">EXAMPLES</span></span>

### <span data-ttu-id="88f47-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="88f47-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessmentMetadata
```

<span data-ttu-id="88f47-113">기본 제공 되는 모든 평가 및 현재 구독에 구성 된 사용자 지정 평가를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="88f47-113">Gets all the built in assessments and the custom assessments that were configured on the current subscription.</span></span>

## <span data-ttu-id="88f47-114">변수</span><span class="sxs-lookup"><span data-stu-id="88f47-114">PARAMETERS</span></span>

### <span data-ttu-id="88f47-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88f47-115">-DefaultProfile</span></span>
<span data-ttu-id="88f47-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88f47-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88f47-117">-이름</span><span class="sxs-lookup"><span data-stu-id="88f47-117">-Name</span></span>
<span data-ttu-id="88f47-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88f47-118">Resource name.</span></span>

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

### <span data-ttu-id="88f47-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88f47-119">-ResourceId</span></span>
<span data-ttu-id="88f47-120">명령을 호출 하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="88f47-120">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="88f47-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88f47-121">CommonParameters</span></span>
<span data-ttu-id="88f47-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="88f47-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88f47-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="88f47-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88f47-124">입력</span><span class="sxs-lookup"><span data-stu-id="88f47-124">INPUTS</span></span>

### <span data-ttu-id="88f47-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="88f47-125">System.String</span></span>

## <span data-ttu-id="88f47-126">출력</span><span class="sxs-lookup"><span data-stu-id="88f47-126">OUTPUTS</span></span>

### <span data-ttu-id="88f47-127">AssessmentMetadata. PSSecurityAssessmentMetadata에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="88f47-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="88f47-128">상속자</span><span class="sxs-lookup"><span data-stu-id="88f47-128">NOTES</span></span>

## <span data-ttu-id="88f47-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88f47-129">RELATED LINKS</span></span>
