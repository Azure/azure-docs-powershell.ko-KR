---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: b13f09085b571d28f93a55bec5250d6bfa180306
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216728"
---
# <span data-ttu-id="1f647-101">Remove-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="1f647-101">Remove-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="1f647-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f647-102">SYNOPSIS</span></span>
<span data-ttu-id="1f647-103">구독에서 보안 평가 메타 데이터를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f647-103">Deletes a security assessment metadata from a subscription.</span></span>

## <span data-ttu-id="1f647-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1f647-104">SYNTAX</span></span>

### <span data-ttu-id="1f647-105">구독 Levelresource (기본값)</span><span class="sxs-lookup"><span data-stu-id="1f647-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessmentMetadata -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f647-106">리소스</span><span class="sxs-lookup"><span data-stu-id="1f647-106">ResourceId</span></span>
```
Remove-AzSecurityAssessmentMetadata -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f647-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="1f647-107">InputObject</span></span>
```
Remove-AzSecurityAssessmentMetadata -InputObject <PSSecurityAssessmentMetadata> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f647-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1f647-108">DESCRIPTION</span></span>
<span data-ttu-id="1f647-109">구독에서 보안 평가 메타 데이터를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f647-109">Deletes a security assessment metadata from a subscription.</span></span> <span data-ttu-id="1f647-110">이 작업을 수행 하면 평가 유형 및 구독에서 관련 된 모든 평가 결과가 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f647-110">This action will delete the assessment type and all the relevant assessment results from the subscription.</span></span>

## <span data-ttu-id="1f647-111">예제의</span><span class="sxs-lookup"><span data-stu-id="1f647-111">EXAMPLES</span></span>

### <span data-ttu-id="1f647-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="1f647-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessmentMetadata -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="1f647-113">구독에서 평가 유형을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f647-113">Deletes an assessment type from a subscription</span></span>

## <span data-ttu-id="1f647-114">변수</span><span class="sxs-lookup"><span data-stu-id="1f647-114">PARAMETERS</span></span>

### <span data-ttu-id="1f647-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f647-115">-DefaultProfile</span></span>
<span data-ttu-id="1f647-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f647-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f647-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f647-117">-InputObject</span></span>
<span data-ttu-id="1f647-118">입력 개체</span><span class="sxs-lookup"><span data-stu-id="1f647-118">Input Object.</span></span>

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

### <span data-ttu-id="1f647-119">-이름</span><span class="sxs-lookup"><span data-stu-id="1f647-119">-Name</span></span>
<span data-ttu-id="1f647-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f647-120">Resource name.</span></span>

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

### <span data-ttu-id="1f647-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f647-121">-PassThru</span></span>
<span data-ttu-id="1f647-122">작업이 성공적으로 수행 되었는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f647-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="1f647-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f647-123">-ResourceId</span></span>
<span data-ttu-id="1f647-124">명령을 호출 하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1f647-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="1f647-125">-확인</span><span class="sxs-lookup"><span data-stu-id="1f647-125">-Confirm</span></span>
<span data-ttu-id="1f647-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f647-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f647-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f647-127">-WhatIf</span></span>
<span data-ttu-id="1f647-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1f647-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f647-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f647-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f647-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f647-130">CommonParameters</span></span>
<span data-ttu-id="1f647-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f647-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f647-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1f647-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f647-133">입력</span><span class="sxs-lookup"><span data-stu-id="1f647-133">INPUTS</span></span>

### <span data-ttu-id="1f647-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1f647-134">System.String</span></span>

### <span data-ttu-id="1f647-135">AssessmentMetadata. PSSecurityAssessmentMetadata에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="1f647-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="1f647-136">출력</span><span class="sxs-lookup"><span data-stu-id="1f647-136">OUTPUTS</span></span>

### <span data-ttu-id="1f647-137">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1f647-137">System.Boolean</span></span>

## <span data-ttu-id="1f647-138">상속자</span><span class="sxs-lookup"><span data-stu-id="1f647-138">NOTES</span></span>

## <span data-ttu-id="1f647-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f647-139">RELATED LINKS</span></span>
