---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: e72766e754394bb43775f73072941dc0d3989c3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986547"
---
# <span data-ttu-id="ed0d0-101">Set-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="ed0d0-101">Set-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="ed0d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed0d0-102">SYNOPSIS</span></span>
<span data-ttu-id="ed0d0-103">보안 평가 유형을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ed0d0-103">Creates or updates a security assessment type.</span></span>

## <span data-ttu-id="ed0d0-104">구문</span><span class="sxs-lookup"><span data-stu-id="ed0d0-104">SYNTAX</span></span>

```
Set-AzSecurityAssessmentMetadata -Name <String> -DisplayName <String> [-Description <String>]
 [-RemediationDescription <String>] [-Severity <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed0d0-105">설명</span><span class="sxs-lookup"><span data-stu-id="ed0d0-105">DESCRIPTION</span></span>
<span data-ttu-id="ed0d0-106">보안 평가 메타데이터를 만들거나 업데이트하고, 다양한 평가 속성을 만들고 관리하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed0d0-106">Creates or updates a security assessment metadata, can be used to create and manage various assessment properties.</span></span>
<span data-ttu-id="ed0d0-107">이 작업 후 이 구독의 모든 리소스에 대한 평가 결과를 보고할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed0d0-107">After this action you will be able to report assessment results on any resource in this subscription.</span></span>

## <span data-ttu-id="ed0d0-108">예제</span><span class="sxs-lookup"><span data-stu-id="ed0d0-108">EXAMPLES</span></span>

### <span data-ttu-id="ed0d0-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="ed0d0-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessmentMetadata -Name $assessmentGuid -DisplayName "Resource should be secured" -Severity "High" -Description "The resource should be secured according to my company's security policy"
```

<span data-ttu-id="ed0d0-110">구독에서 새 평가 유형을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed0d0-110">Create a new assessment type in a subscription.</span></span>

## <span data-ttu-id="ed0d0-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ed0d0-111">PARAMETERS</span></span>

### <span data-ttu-id="ed0d0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed0d0-112">-DefaultProfile</span></span>
<span data-ttu-id="ed0d0-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ed0d0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed0d0-114">-Description</span><span class="sxs-lookup"><span data-stu-id="ed0d0-114">-Description</span></span>
<span data-ttu-id="ed0d0-115">사용자가 이 평가의 의미와 계산 방법을 이해하는 데 도움이 되는 자세한 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="ed0d0-115">Detailed string that will help users to understand the meaning of this assessment and how it was calculated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0d0-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ed0d0-116">-DisplayName</span></span>
<span data-ttu-id="ed0d0-117">이 개체에 대해 사람이 읽을 수 있는 제목입니다.</span><span class="sxs-lookup"><span data-stu-id="ed0d0-117">Human readable title for this object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0d0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ed0d0-118">-Name</span></span>
<span data-ttu-id="ed0d0-119">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ed0d0-119">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0d0-120">-RemediationDescription</span><span class="sxs-lookup"><span data-stu-id="ed0d0-120">-RemediationDescription</span></span>
<span data-ttu-id="ed0d0-121">사용자가 보안 문제를 완화하거나 해결하는 다양한 방법을 이해하는 데 도움이 되는 자세한 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="ed0d0-121">Detailed string that will help users to understand the different ways to mitigate or fix the security issue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0d0-122">-심각도</span><span class="sxs-lookup"><span data-stu-id="ed0d0-122">-Severity</span></span>
<span data-ttu-id="ed0d0-123">평가가 안전하지 않은 경우 보안 위험의 중요성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ed0d0-123">Indicates the importance of the security risk if the assessment is unhealthy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0d0-124">-확인</span><span class="sxs-lookup"><span data-stu-id="ed0d0-124">-Confirm</span></span>
<span data-ttu-id="ed0d0-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed0d0-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0d0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed0d0-126">-WhatIf</span></span>
<span data-ttu-id="ed0d0-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ed0d0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed0d0-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed0d0-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0d0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed0d0-129">CommonParameters</span></span>
<span data-ttu-id="ed0d0-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ed0d0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed0d0-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed0d0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed0d0-132">입력</span><span class="sxs-lookup"><span data-stu-id="ed0d0-132">INPUTS</span></span>

### <span data-ttu-id="ed0d0-133">없음</span><span class="sxs-lookup"><span data-stu-id="ed0d0-133">None</span></span>

## <span data-ttu-id="ed0d0-134">출력</span><span class="sxs-lookup"><span data-stu-id="ed0d0-134">OUTPUTS</span></span>

### <span data-ttu-id="ed0d0-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="ed0d0-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="ed0d0-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ed0d0-136">NOTES</span></span>

## <span data-ttu-id="ed0d0-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed0d0-137">RELATED LINKS</span></span>
