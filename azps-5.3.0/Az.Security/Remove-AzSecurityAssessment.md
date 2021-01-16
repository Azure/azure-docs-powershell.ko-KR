---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
ms.openlocfilehash: d24a2a5ef6017942815f1a652e1c769523815b7f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377728"
---
# <span data-ttu-id="d939f-101">Remove-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="d939f-101">Remove-AzSecurityAssessment</span></span>

## <span data-ttu-id="d939f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d939f-102">SYNOPSIS</span></span>
<span data-ttu-id="d939f-103">구독에서 보안 평가 결과를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="d939f-103">Deletes a security assessment result from a subscription.</span></span>

## <span data-ttu-id="d939f-104">구문</span><span class="sxs-lookup"><span data-stu-id="d939f-104">SYNTAX</span></span>

### <span data-ttu-id="d939f-105">SubscriptionLevelResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="d939f-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d939f-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="d939f-106">ResourceIdLevelResource</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-AssessedResourceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d939f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d939f-107">ResourceId</span></span>
```
Remove-AzSecurityAssessment -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d939f-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="d939f-108">InputObject</span></span>
```
Remove-AzSecurityAssessment -InputObject <PSSecurityAssessment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d939f-109">설명</span><span class="sxs-lookup"><span data-stu-id="d939f-109">DESCRIPTION</span></span>
<span data-ttu-id="d939f-110">구독에서 보안 평가 결과를 삭제합니다. 일반적으로 재구성이 삭제되거나 평가가 특정 리소스와 관련이 없는 경우 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d939f-110">Deletes a security assessment result from a subscription, usually used when a resoruce is deleted or when the assessment is not relevant for a specific resource anymore</span></span>

## <span data-ttu-id="d939f-111">예제</span><span class="sxs-lookup"><span data-stu-id="d939f-111">EXAMPLES</span></span>

### <span data-ttu-id="d939f-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="d939f-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="d939f-113">구독에서 평가 결과를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="d939f-113">Deletes an assessment result on a subscription</span></span>

## <span data-ttu-id="d939f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d939f-114">PARAMETERS</span></span>

### <span data-ttu-id="d939f-115">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="d939f-115">-AssessedResourceId</span></span>
<span data-ttu-id="d939f-116">평가가 계산된 리소스의 전체 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d939f-116">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d939f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d939f-117">-DefaultProfile</span></span>
<span data-ttu-id="d939f-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d939f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d939f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d939f-119">-InputObject</span></span>
<span data-ttu-id="d939f-120">입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d939f-120">Input Object.</span></span>

```yaml
Type: PSSecurityAssessment
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d939f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d939f-121">-Name</span></span>
<span data-ttu-id="d939f-122">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d939f-122">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d939f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d939f-123">-PassThru</span></span>
<span data-ttu-id="d939f-124">작업이 성공한지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d939f-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="d939f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d939f-125">-ResourceId</span></span>
<span data-ttu-id="d939f-126">명령을 호출하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d939f-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="d939f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d939f-127">-Confirm</span></span>
<span data-ttu-id="d939f-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d939f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d939f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d939f-129">-WhatIf</span></span>
<span data-ttu-id="d939f-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d939f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d939f-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d939f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d939f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d939f-132">CommonParameters</span></span>
<span data-ttu-id="d939f-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d939f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d939f-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d939f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d939f-135">입력</span><span class="sxs-lookup"><span data-stu-id="d939f-135">INPUTS</span></span>

### <span data-ttu-id="d939f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d939f-136">System.String</span></span>

### <span data-ttu-id="d939f-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="d939f-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="d939f-138">출력</span><span class="sxs-lookup"><span data-stu-id="d939f-138">OUTPUTS</span></span>

### <span data-ttu-id="d939f-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d939f-139">System.Boolean</span></span>

## <span data-ttu-id="d939f-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d939f-140">NOTES</span></span>

## <span data-ttu-id="d939f-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d939f-141">RELATED LINKS</span></span>
