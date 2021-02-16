---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySubAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
ms.openlocfilehash: 10808d7e4f6e270801ef56e48b605f4c23cd6246
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183588"
---
# <span data-ttu-id="2b7b5-101">Get-AzSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="2b7b5-101">Get-AzSecuritySubAssessment</span></span>

## <span data-ttu-id="2b7b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b7b5-102">SYNOPSIS</span></span>
<span data-ttu-id="2b7b5-103">구독에서 하위 평가 결과를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-103">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="2b7b5-104">구문</span><span class="sxs-lookup"><span data-stu-id="2b7b5-104">SYNTAX</span></span>

### <span data-ttu-id="2b7b5-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="2b7b5-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySubAssessment [-AssessedResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b7b5-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="2b7b5-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b7b5-107">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="2b7b5-107">ResourceIdLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b7b5-108">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="2b7b5-108">ResourceIdScope</span></span>
```
Get-AzSecuritySubAssessment -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b7b5-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b7b5-109">ResourceId</span></span>
```
Get-AzSecuritySubAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b7b5-110">설명</span><span class="sxs-lookup"><span data-stu-id="2b7b5-110">DESCRIPTION</span></span>
<span data-ttu-id="2b7b5-111">구독에서 하위 평가 결과를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-111">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="2b7b5-112">예제</span><span class="sxs-lookup"><span data-stu-id="2b7b5-112">EXAMPLES</span></span>

### <span data-ttu-id="2b7b5-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="2b7b5-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySubAssessment
```

<span data-ttu-id="2b7b5-114">구독의 모든 하위 평가 결과를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-114">Gets all the sub assessments results in a subscription.</span></span>

## <span data-ttu-id="2b7b5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b7b5-115">PARAMETERS</span></span>

### <span data-ttu-id="2b7b5-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="2b7b5-116">-AssessedResourceId</span></span>
<span data-ttu-id="2b7b5-117">평가가 계산된 리소스의 전체 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="2b7b5-118">-AssessmentName</span><span class="sxs-lookup"><span data-stu-id="2b7b5-118">-AssessmentName</span></span>
<span data-ttu-id="2b7b5-119">평가 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-119">Name of the assessment resource.</span></span>

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

### <span data-ttu-id="2b7b5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b7b5-120">-DefaultProfile</span></span>
<span data-ttu-id="2b7b5-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b7b5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2b7b5-122">-Name</span></span>
<span data-ttu-id="2b7b5-123">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-123">Resource name.</span></span>

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

### <span data-ttu-id="2b7b5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b7b5-124">-ResourceId</span></span>
<span data-ttu-id="2b7b5-125">명령을 호출하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="2b7b5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b7b5-126">CommonParameters</span></span>
<span data-ttu-id="2b7b5-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b7b5-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2b7b5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b7b5-129">입력</span><span class="sxs-lookup"><span data-stu-id="2b7b5-129">INPUTS</span></span>

### <span data-ttu-id="2b7b5-130">System.String</span><span class="sxs-lookup"><span data-stu-id="2b7b5-130">System.String</span></span>

## <span data-ttu-id="2b7b5-131">출력</span><span class="sxs-lookup"><span data-stu-id="2b7b5-131">OUTPUTS</span></span>

### <span data-ttu-id="2b7b5-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="2b7b5-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span></span>

## <span data-ttu-id="2b7b5-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2b7b5-133">NOTES</span></span>

## <span data-ttu-id="2b7b5-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b7b5-134">RELATED LINKS</span></span>
