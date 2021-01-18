---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: b13f09085b571d28f93a55bec5250d6bfa180306
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494980"
---
# <span data-ttu-id="3be7b-101">Remove-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="3be7b-101">Remove-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="3be7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3be7b-102">SYNOPSIS</span></span>
<span data-ttu-id="3be7b-103">구독에서 보안 평가 메타데이터를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="3be7b-103">Deletes a security assessment metadata from a subscription.</span></span>

## <span data-ttu-id="3be7b-104">구문</span><span class="sxs-lookup"><span data-stu-id="3be7b-104">SYNTAX</span></span>

### <span data-ttu-id="3be7b-105">SubscriptionLevelResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="3be7b-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessmentMetadata -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3be7b-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3be7b-106">ResourceId</span></span>
```
Remove-AzSecurityAssessmentMetadata -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3be7b-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="3be7b-107">InputObject</span></span>
```
Remove-AzSecurityAssessmentMetadata -InputObject <PSSecurityAssessmentMetadata> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3be7b-108">설명</span><span class="sxs-lookup"><span data-stu-id="3be7b-108">DESCRIPTION</span></span>
<span data-ttu-id="3be7b-109">구독에서 보안 평가 메타데이터를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="3be7b-109">Deletes a security assessment metadata from a subscription.</span></span> <span data-ttu-id="3be7b-110">이 작업은 구독에서 평가 유형 및 모든 관련 평가 결과를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="3be7b-110">This action will delete the assessment type and all the relevant assessment results from the subscription.</span></span>

## <span data-ttu-id="3be7b-111">예제</span><span class="sxs-lookup"><span data-stu-id="3be7b-111">EXAMPLES</span></span>

### <span data-ttu-id="3be7b-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="3be7b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessmentMetadata -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="3be7b-113">구독에서 평가 유형을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="3be7b-113">Deletes an assessment type from a subscription</span></span>

## <span data-ttu-id="3be7b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3be7b-114">PARAMETERS</span></span>

### <span data-ttu-id="3be7b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3be7b-115">-DefaultProfile</span></span>
<span data-ttu-id="3be7b-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3be7b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3be7b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3be7b-117">-InputObject</span></span>
<span data-ttu-id="3be7b-118">입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3be7b-118">Input Object.</span></span>

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

### <span data-ttu-id="3be7b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3be7b-119">-Name</span></span>
<span data-ttu-id="3be7b-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3be7b-120">Resource name.</span></span>

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

### <span data-ttu-id="3be7b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3be7b-121">-PassThru</span></span>
<span data-ttu-id="3be7b-122">작업이 성공한지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3be7b-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="3be7b-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3be7b-123">-ResourceId</span></span>
<span data-ttu-id="3be7b-124">명령을 호출하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3be7b-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="3be7b-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3be7b-125">-Confirm</span></span>
<span data-ttu-id="3be7b-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3be7b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3be7b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3be7b-127">-WhatIf</span></span>
<span data-ttu-id="3be7b-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3be7b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3be7b-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3be7b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3be7b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3be7b-130">CommonParameters</span></span>
<span data-ttu-id="3be7b-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3be7b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3be7b-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3be7b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3be7b-133">입력</span><span class="sxs-lookup"><span data-stu-id="3be7b-133">INPUTS</span></span>

### <span data-ttu-id="3be7b-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3be7b-134">System.String</span></span>

### <span data-ttu-id="3be7b-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="3be7b-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="3be7b-136">출력</span><span class="sxs-lookup"><span data-stu-id="3be7b-136">OUTPUTS</span></span>

### <span data-ttu-id="3be7b-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3be7b-137">System.Boolean</span></span>

## <span data-ttu-id="3be7b-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3be7b-138">NOTES</span></span>

## <span data-ttu-id="3be7b-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3be7b-139">RELATED LINKS</span></span>
