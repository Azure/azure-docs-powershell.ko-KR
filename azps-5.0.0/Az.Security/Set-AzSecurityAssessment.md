---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
ms.openlocfilehash: 9a227c742892d94417d42be7137f903e17b8b928
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218003"
---
# <span data-ttu-id="320bf-101">Set-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="320bf-101">Set-AzSecurityAssessment</span></span>

## <span data-ttu-id="320bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="320bf-102">SYNOPSIS</span></span>
<span data-ttu-id="320bf-103">리소스에 대 한 보안 평가 결과 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="320bf-103">Create or update a security assessment result on a resource</span></span>

## <span data-ttu-id="320bf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="320bf-104">SYNTAX</span></span>

### <span data-ttu-id="320bf-105">구독 Levelresource (기본값)</span><span class="sxs-lookup"><span data-stu-id="320bf-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAssessment -Name <String> [-StatusCode <String>] [-StatusCause <String>]
 [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="320bf-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="320bf-106">ResourceIdLevelResource</span></span>
```
Set-AzSecurityAssessment -Name <String> -AssessedResourceId <String> -StatusCode <String>
 [-StatusCause <String>] [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="320bf-107">설명은</span><span class="sxs-lookup"><span data-stu-id="320bf-107">DESCRIPTION</span></span>
<span data-ttu-id="320bf-108">리소스에 대 한 보안 평가 결과를 만들거나 업데이트 하 여 기존 결과의 상태를 변경 하거나 추가 데이터를 추가 하는 데 사용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="320bf-108">Create or update a security assessment result on a resource, can be used to change the status of an existing result or add additional data.</span></span>
<span data-ttu-id="320bf-109">"CustomerManaged" 평가 유형에만 사용할 수 있으며, 일치 하는 평가 메타 데이터를 만든 후에만 사용 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="320bf-109">can only be used for "CustomerManaged" assessment types and only after the matched assessment metadata is created.</span></span>

## <span data-ttu-id="320bf-110">예제의</span><span class="sxs-lookup"><span data-stu-id="320bf-110">EXAMPLES</span></span>

### <span data-ttu-id="320bf-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="320bf-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D -StatusCode "Unhealthy"
```

<span data-ttu-id="320bf-112">"4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" 유형의 평가에 대 한 "비정상"으로 구독 결과를 표시 합니다. 평가 형식에 대 한 자세한 내용은 assessmentMetadata 형식 아래에서 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="320bf-112">Marks the subscription result as "Unhealthy" for assessment of type "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" - more details about the assessment type will be found under the assessmentMetadata type</span></span>

## <span data-ttu-id="320bf-113">변수</span><span class="sxs-lookup"><span data-stu-id="320bf-113">PARAMETERS</span></span>

### <span data-ttu-id="320bf-114">-AdditionalData</span><span class="sxs-lookup"><span data-stu-id="320bf-114">-AdditionalData</span></span>
<span data-ttu-id="320bf-115">더 나은 조사 또는 상태 명확성을 위해 평가 결과에 첨부 된 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="320bf-115">Data that is attached to the assessment result for better investigations or status clarity.</span></span>

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

### <span data-ttu-id="320bf-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="320bf-116">-AssessedResourceId</span></span>
<span data-ttu-id="320bf-117">평가를 계산할 리소스의 전체 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="320bf-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="320bf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="320bf-118">-DefaultProfile</span></span>
<span data-ttu-id="320bf-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="320bf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="320bf-120">-이름</span><span class="sxs-lookup"><span data-stu-id="320bf-120">-Name</span></span>
<span data-ttu-id="320bf-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="320bf-121">Resource name.</span></span>

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

### <span data-ttu-id="320bf-122">-StatusCause</span><span class="sxs-lookup"><span data-stu-id="320bf-122">-StatusCause</span></span>
<span data-ttu-id="320bf-123">평가 결과의 원인을 Progremmatic 코드를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="320bf-123">Progremmatic code for the cause of the assessment's result.</span></span>

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

### <span data-ttu-id="320bf-124">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="320bf-124">-StatusCode</span></span>
<span data-ttu-id="320bf-125">평가 결과에 대 한 코드를 Progremmatic.</span><span class="sxs-lookup"><span data-stu-id="320bf-125">Progremmatic code for the result of the assessment.</span></span>
<span data-ttu-id="320bf-126">"정상", "비정상" 또는 "NotApplicable" 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="320bf-126">can be "Healthy", "Unhealthy" or "NotApplicable"</span></span>

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

### <span data-ttu-id="320bf-127">-StatusDescription</span><span class="sxs-lookup"><span data-stu-id="320bf-127">-StatusDescription</span></span>
<span data-ttu-id="320bf-128">평가 결과의 원인에 대 한 사람이 읽을 수 있는 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="320bf-128">Human readable description of the cause of the assessment's result.</span></span>

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

### <span data-ttu-id="320bf-129">-확인</span><span class="sxs-lookup"><span data-stu-id="320bf-129">-Confirm</span></span>
<span data-ttu-id="320bf-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="320bf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="320bf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="320bf-131">-WhatIf</span></span>
<span data-ttu-id="320bf-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="320bf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="320bf-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="320bf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="320bf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="320bf-134">CommonParameters</span></span>
<span data-ttu-id="320bf-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="320bf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="320bf-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="320bf-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="320bf-137">입력</span><span class="sxs-lookup"><span data-stu-id="320bf-137">INPUTS</span></span>

### <span data-ttu-id="320bf-138">않아야</span><span class="sxs-lookup"><span data-stu-id="320bf-138">None</span></span>

## <span data-ttu-id="320bf-139">출력</span><span class="sxs-lookup"><span data-stu-id="320bf-139">OUTPUTS</span></span>

### <span data-ttu-id="320bf-140">Microsoft. Azure. a. PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="320bf-140">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="320bf-141">상속자</span><span class="sxs-lookup"><span data-stu-id="320bf-141">NOTES</span></span>

## <span data-ttu-id="320bf-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="320bf-142">RELATED LINKS</span></span>
