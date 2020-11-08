---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySubAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
ms.openlocfilehash: 10808d7e4f6e270801ef56e48b605f4c23cd6246
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218172"
---
# <span data-ttu-id="a6a48-101">Get-AzSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="a6a48-101">Get-AzSecuritySubAssessment</span></span>

## <span data-ttu-id="a6a48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6a48-102">SYNOPSIS</span></span>
<span data-ttu-id="a6a48-103">구독에서 하위 평가 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a6a48-103">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="a6a48-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a6a48-104">SYNTAX</span></span>

### <span data-ttu-id="a6a48-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a6a48-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySubAssessment [-AssessedResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6a48-106">구독 Levelresource</span><span class="sxs-lookup"><span data-stu-id="a6a48-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6a48-107">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="a6a48-107">ResourceIdLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6a48-108">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="a6a48-108">ResourceIdScope</span></span>
```
Get-AzSecuritySubAssessment -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6a48-109">리소스</span><span class="sxs-lookup"><span data-stu-id="a6a48-109">ResourceId</span></span>
```
Get-AzSecuritySubAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a6a48-110">설명은</span><span class="sxs-lookup"><span data-stu-id="a6a48-110">DESCRIPTION</span></span>
<span data-ttu-id="a6a48-111">구독에서 하위 평가 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a6a48-111">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="a6a48-112">예제의</span><span class="sxs-lookup"><span data-stu-id="a6a48-112">EXAMPLES</span></span>

### <span data-ttu-id="a6a48-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="a6a48-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySubAssessment
```

<span data-ttu-id="a6a48-114">구독의 모든 하위 평가 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a6a48-114">Gets all the sub assessments results in a subscription.</span></span>

## <span data-ttu-id="a6a48-115">변수</span><span class="sxs-lookup"><span data-stu-id="a6a48-115">PARAMETERS</span></span>

### <span data-ttu-id="a6a48-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="a6a48-116">-AssessedResourceId</span></span>
<span data-ttu-id="a6a48-117">평가를 계산할 리소스의 전체 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a6a48-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionScope, SubscriptionLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource, ResourceIdScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a48-118">-AssessmentName</span><span class="sxs-lookup"><span data-stu-id="a6a48-118">-AssessmentName</span></span>
<span data-ttu-id="a6a48-119">평가 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a6a48-119">Name of the assessment resource.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource, ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6a48-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6a48-120">-DefaultProfile</span></span>
<span data-ttu-id="a6a48-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a6a48-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6a48-122">-이름</span><span class="sxs-lookup"><span data-stu-id="a6a48-122">-Name</span></span>
<span data-ttu-id="a6a48-123">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a6a48-123">Resource name.</span></span>

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
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a48-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6a48-124">-ResourceId</span></span>
<span data-ttu-id="a6a48-125">명령을 호출 하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a6a48-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="a6a48-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6a48-126">CommonParameters</span></span>
<span data-ttu-id="a6a48-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a48-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6a48-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a6a48-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6a48-129">입력</span><span class="sxs-lookup"><span data-stu-id="a6a48-129">INPUTS</span></span>

### <span data-ttu-id="a6a48-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a6a48-130">System.String</span></span>

## <span data-ttu-id="a6a48-131">출력</span><span class="sxs-lookup"><span data-stu-id="a6a48-131">OUTPUTS</span></span>

### <span data-ttu-id="a6a48-132">Microsoft. Azure. a. m 평가. PSSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="a6a48-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span></span>

## <span data-ttu-id="a6a48-133">상속자</span><span class="sxs-lookup"><span data-stu-id="a6a48-133">NOTES</span></span>

## <span data-ttu-id="a6a48-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a6a48-134">RELATED LINKS</span></span>
