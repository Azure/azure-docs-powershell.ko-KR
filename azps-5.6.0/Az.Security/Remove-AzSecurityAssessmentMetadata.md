---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: daa0d87eab24743863e6cbbcdd1c010e974c113c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974336"
---
# <span data-ttu-id="1a2e3-101">Remove-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="1a2e3-101">Remove-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="1a2e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a2e3-102">SYNOPSIS</span></span>
<span data-ttu-id="1a2e3-103">구독에서 보안 평가 메타데이터를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1a2e3-103">Deletes a security assessment metadata from a subscription.</span></span>

## <span data-ttu-id="1a2e3-104">구문</span><span class="sxs-lookup"><span data-stu-id="1a2e3-104">SYNTAX</span></span>

### <span data-ttu-id="1a2e3-105">SubscriptionLevelResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="1a2e3-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessmentMetadata -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a2e3-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a2e3-106">ResourceId</span></span>
```
Remove-AzSecurityAssessmentMetadata -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a2e3-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="1a2e3-107">InputObject</span></span>
```
Remove-AzSecurityAssessmentMetadata -InputObject <PSSecurityAssessmentMetadata> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a2e3-108">설명</span><span class="sxs-lookup"><span data-stu-id="1a2e3-108">DESCRIPTION</span></span>
<span data-ttu-id="1a2e3-109">구독에서 보안 평가 메타데이터를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1a2e3-109">Deletes a security assessment metadata from a subscription.</span></span> <span data-ttu-id="1a2e3-110">이 작업은 평가 유형 및 구독의 모든 관련 평가 결과를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1a2e3-110">This action will delete the assessment type and all the relevant assessment results from the subscription.</span></span>

## <span data-ttu-id="1a2e3-111">예제</span><span class="sxs-lookup"><span data-stu-id="1a2e3-111">EXAMPLES</span></span>

### <span data-ttu-id="1a2e3-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="1a2e3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessmentMetadata -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="1a2e3-113">구독에서 평가 유형을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1a2e3-113">Deletes an assessment type from a subscription</span></span>

## <span data-ttu-id="1a2e3-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1a2e3-114">PARAMETERS</span></span>

### <span data-ttu-id="1a2e3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a2e3-115">-DefaultProfile</span></span>
<span data-ttu-id="1a2e3-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1a2e3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a2e3-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a2e3-117">-InputObject</span></span>
<span data-ttu-id="1a2e3-118">입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1a2e3-118">Input Object.</span></span>

```yaml
Type: PSSecurityAssessmentMetadata
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a2e3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1a2e3-119">-Name</span></span>
<span data-ttu-id="1a2e3-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a2e3-120">Resource name.</span></span>

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

### <span data-ttu-id="1a2e3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a2e3-121">-PassThru</span></span>
<span data-ttu-id="1a2e3-122">작업이 성공한지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1a2e3-122">Return whether the operation was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a2e3-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a2e3-123">-ResourceId</span></span>
<span data-ttu-id="1a2e3-124">명령을 호출할 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1a2e3-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="1a2e3-125">-확인</span><span class="sxs-lookup"><span data-stu-id="1a2e3-125">-Confirm</span></span>
<span data-ttu-id="1a2e3-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a2e3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a2e3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a2e3-127">-WhatIf</span></span>
<span data-ttu-id="1a2e3-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1a2e3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a2e3-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1a2e3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a2e3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a2e3-130">CommonParameters</span></span>
<span data-ttu-id="1a2e3-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1a2e3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a2e3-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a2e3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a2e3-133">입력</span><span class="sxs-lookup"><span data-stu-id="1a2e3-133">INPUTS</span></span>

### <span data-ttu-id="1a2e3-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1a2e3-134">System.String</span></span>

### <span data-ttu-id="1a2e3-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="1a2e3-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="1a2e3-136">출력</span><span class="sxs-lookup"><span data-stu-id="1a2e3-136">OUTPUTS</span></span>

### <span data-ttu-id="1a2e3-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1a2e3-137">System.Boolean</span></span>

## <span data-ttu-id="1a2e3-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1a2e3-138">NOTES</span></span>

## <span data-ttu-id="1a2e3-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a2e3-139">RELATED LINKS</span></span>
