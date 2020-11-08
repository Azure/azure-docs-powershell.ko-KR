---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: d65cd0a5f29f15d2d82227aad6520df34fd4357f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218002"
---
# <span data-ttu-id="ae59c-101">Set-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="ae59c-101">Set-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="ae59c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae59c-102">SYNOPSIS</span></span>
<span data-ttu-id="ae59c-103">보안 평가 유형을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae59c-103">Creates or updates a security assessment type.</span></span>

## <span data-ttu-id="ae59c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ae59c-104">SYNTAX</span></span>

```
Set-AzSecurityAssessmentMetadata -Name <String> -DisplayName <String> [-Description <String>]
 [-RemediationDescription <String>] [-Severity <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae59c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ae59c-105">DESCRIPTION</span></span>
<span data-ttu-id="ae59c-106">보안 평가 메타 데이터를 만들거나 업데이트 하 여 다양 한 평가 속성을 만들고 관리 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae59c-106">Creates or updates a security assessment metadata, can be used to create and manage various assessment properties.</span></span>
<span data-ttu-id="ae59c-107">이 작업을 수행한 후에는이 구독의 모든 리소스에서 평가 결과를 보고할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae59c-107">After this action you will be able to report assessment results on any resource in this subscription.</span></span>

## <span data-ttu-id="ae59c-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ae59c-108">EXAMPLES</span></span>

### <span data-ttu-id="ae59c-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="ae59c-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessmentMetadata -Name $assessmentGuid -DisplayName "Resource should be secured" -Severity "High" -Description "The resource should be secured according to my company's security policy"
```

<span data-ttu-id="ae59c-110">구독에서 새 평가 유형을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ae59c-110">Create a new assessment type in a subscription.</span></span>

## <span data-ttu-id="ae59c-111">변수</span><span class="sxs-lookup"><span data-stu-id="ae59c-111">PARAMETERS</span></span>

### <span data-ttu-id="ae59c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae59c-112">-DefaultProfile</span></span>
<span data-ttu-id="ae59c-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ae59c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae59c-114">-설명</span><span class="sxs-lookup"><span data-stu-id="ae59c-114">-Description</span></span>
<span data-ttu-id="ae59c-115">이 평가의 의미와 계산 방법을 이해 하는 데 도움이 되는 자세한 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="ae59c-115">Detailed string that will help users to understand the meaning of this assessment and how it was calculated.</span></span>

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

### <span data-ttu-id="ae59c-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ae59c-116">-DisplayName</span></span>
<span data-ttu-id="ae59c-117">이 개체에 대 한 사람이 읽을 수 있는 제목입니다.</span><span class="sxs-lookup"><span data-stu-id="ae59c-117">Human readable title for this object.</span></span>

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

### <span data-ttu-id="ae59c-118">-이름</span><span class="sxs-lookup"><span data-stu-id="ae59c-118">-Name</span></span>
<span data-ttu-id="ae59c-119">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae59c-119">Resource name.</span></span>

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

### <span data-ttu-id="ae59c-120">-RemediationDescription</span><span class="sxs-lookup"><span data-stu-id="ae59c-120">-RemediationDescription</span></span>
<span data-ttu-id="ae59c-121">사용자가 보안 문제를 완화 하거나 해결 하는 다양 한 방법을 이해 하는 데 도움이 되는 자세한 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="ae59c-121">Detailed string that will help users to understand the different ways to mitigate or fix the security issue.</span></span>

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

### <span data-ttu-id="ae59c-122">-심각도</span><span class="sxs-lookup"><span data-stu-id="ae59c-122">-Severity</span></span>
<span data-ttu-id="ae59c-123">평가가 비정상 인 경우 보안 위험의 중요성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ae59c-123">Indicates the importance of the security risk if the assessment is unhealthy.</span></span>

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

### <span data-ttu-id="ae59c-124">-확인</span><span class="sxs-lookup"><span data-stu-id="ae59c-124">-Confirm</span></span>
<span data-ttu-id="ae59c-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae59c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae59c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae59c-126">-WhatIf</span></span>
<span data-ttu-id="ae59c-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ae59c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae59c-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae59c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae59c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae59c-129">CommonParameters</span></span>
<span data-ttu-id="ae59c-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae59c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae59c-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ae59c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae59c-132">입력</span><span class="sxs-lookup"><span data-stu-id="ae59c-132">INPUTS</span></span>

### <span data-ttu-id="ae59c-133">않아야</span><span class="sxs-lookup"><span data-stu-id="ae59c-133">None</span></span>

## <span data-ttu-id="ae59c-134">출력</span><span class="sxs-lookup"><span data-stu-id="ae59c-134">OUTPUTS</span></span>

### <span data-ttu-id="ae59c-135">AssessmentMetadata. PSSecurityAssessmentMetadata에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="ae59c-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="ae59c-136">상속자</span><span class="sxs-lookup"><span data-stu-id="ae59c-136">NOTES</span></span>

## <span data-ttu-id="ae59c-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae59c-137">RELATED LINKS</span></span>
