---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
ms.openlocfilehash: 9a227c742892d94417d42be7137f903e17b8b928
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490243"
---
# <span data-ttu-id="aa5ec-101">Set-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="aa5ec-101">Set-AzSecurityAssessment</span></span>

## <span data-ttu-id="aa5ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa5ec-102">SYNOPSIS</span></span>
<span data-ttu-id="aa5ec-103">리소스에 대한 보안 평가 결과 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="aa5ec-103">Create or update a security assessment result on a resource</span></span>

## <span data-ttu-id="aa5ec-104">구문</span><span class="sxs-lookup"><span data-stu-id="aa5ec-104">SYNTAX</span></span>

### <span data-ttu-id="aa5ec-105">SubscriptionLevelResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="aa5ec-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAssessment -Name <String> [-StatusCode <String>] [-StatusCause <String>]
 [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa5ec-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="aa5ec-106">ResourceIdLevelResource</span></span>
```
Set-AzSecurityAssessment -Name <String> -AssessedResourceId <String> -StatusCode <String>
 [-StatusCause <String>] [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa5ec-107">설명</span><span class="sxs-lookup"><span data-stu-id="aa5ec-107">DESCRIPTION</span></span>
<span data-ttu-id="aa5ec-108">리소스에 대한 보안 평가 결과를 만들거나 업데이트하거나 기존 결과의 상태를 변경하거나 추가 데이터를 추가하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa5ec-108">Create or update a security assessment result on a resource, can be used to change the status of an existing result or add additional data.</span></span>
<span data-ttu-id="aa5ec-109">"고객 관리" 평가 유형에만 사용할 수 있으며 일치하는 평가 메타데이터를 만든 후에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa5ec-109">can only be used for "CustomerManaged" assessment types and only after the matched assessment metadata is created.</span></span>

## <span data-ttu-id="aa5ec-110">예제</span><span class="sxs-lookup"><span data-stu-id="aa5ec-110">EXAMPLES</span></span>

### <span data-ttu-id="aa5ec-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="aa5ec-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D -StatusCode "Unhealthy"
```

<span data-ttu-id="aa5ec-112">"4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" 형식의 평가에 대한 구독 결과를 "Unhealthy"로 표시 - 평가 유형에 대한 자세한 내용은 assessmentMetadata 형식에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa5ec-112">Marks the subscription result as "Unhealthy" for assessment of type "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" - more details about the assessment type will be found under the assessmentMetadata type</span></span>

## <span data-ttu-id="aa5ec-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa5ec-113">PARAMETERS</span></span>

### <span data-ttu-id="aa5ec-114">-AdditionalData</span><span class="sxs-lookup"><span data-stu-id="aa5ec-114">-AdditionalData</span></span>
<span data-ttu-id="aa5ec-115">더 나은 조사 또는 상태 명확성을 위해 평가 결과에 연결된 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="aa5ec-115">Data that is attached to the assessment result for better investigations or status clarity.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa5ec-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="aa5ec-116">-AssessedResourceId</span></span>
<span data-ttu-id="aa5ec-117">평가가 계산된 리소스의 전체 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="aa5ec-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="aa5ec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa5ec-118">-DefaultProfile</span></span>
<span data-ttu-id="aa5ec-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aa5ec-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa5ec-120">-Name</span><span class="sxs-lookup"><span data-stu-id="aa5ec-120">-Name</span></span>
<span data-ttu-id="aa5ec-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa5ec-121">Resource name.</span></span>

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

### <span data-ttu-id="aa5ec-122">-StatusCause</span><span class="sxs-lookup"><span data-stu-id="aa5ec-122">-StatusCause</span></span>
<span data-ttu-id="aa5ec-123">평가 결과의 원인에 대한 전형적 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="aa5ec-123">Progremmatic code for the cause of the assessment's result.</span></span>

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

### <span data-ttu-id="aa5ec-124">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="aa5ec-124">-StatusCode</span></span>
<span data-ttu-id="aa5ec-125">평가 결과에 대한 예시 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="aa5ec-125">Progremmatic code for the result of the assessment.</span></span>
<span data-ttu-id="aa5ec-126">"정상", "정상" 또는 "NotApplicable"일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa5ec-126">can be "Healthy", "Unhealthy" or "NotApplicable"</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: False
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

### <span data-ttu-id="aa5ec-127">-StatusDescription</span><span class="sxs-lookup"><span data-stu-id="aa5ec-127">-StatusDescription</span></span>
<span data-ttu-id="aa5ec-128">평가 결과의 원인에 대한 사람이 읽을 수 있는 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="aa5ec-128">Human readable description of the cause of the assessment's result.</span></span>

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

### <span data-ttu-id="aa5ec-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa5ec-129">-Confirm</span></span>
<span data-ttu-id="aa5ec-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="aa5ec-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa5ec-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa5ec-131">-WhatIf</span></span>
<span data-ttu-id="aa5ec-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="aa5ec-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa5ec-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa5ec-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa5ec-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa5ec-134">CommonParameters</span></span>
<span data-ttu-id="aa5ec-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aa5ec-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa5ec-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aa5ec-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa5ec-137">입력</span><span class="sxs-lookup"><span data-stu-id="aa5ec-137">INPUTS</span></span>

### <span data-ttu-id="aa5ec-138">없음</span><span class="sxs-lookup"><span data-stu-id="aa5ec-138">None</span></span>

## <span data-ttu-id="aa5ec-139">출력</span><span class="sxs-lookup"><span data-stu-id="aa5ec-139">OUTPUTS</span></span>

### <span data-ttu-id="aa5ec-140">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="aa5ec-140">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="aa5ec-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aa5ec-141">NOTES</span></span>

## <span data-ttu-id="aa5ec-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa5ec-142">RELATED LINKS</span></span>
