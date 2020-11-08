---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
ms.openlocfilehash: d24a2a5ef6017942815f1a652e1c769523815b7f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213970"
---
# <span data-ttu-id="fd0b1-101">Remove-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="fd0b1-101">Remove-AzSecurityAssessment</span></span>

## <span data-ttu-id="fd0b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd0b1-102">SYNOPSIS</span></span>
<span data-ttu-id="fd0b1-103">구독에서 보안 평가 결과를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd0b1-103">Deletes a security assessment result from a subscription.</span></span>

## <span data-ttu-id="fd0b1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fd0b1-104">SYNTAX</span></span>

### <span data-ttu-id="fd0b1-105">구독 Levelresource (기본값)</span><span class="sxs-lookup"><span data-stu-id="fd0b1-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd0b1-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="fd0b1-106">ResourceIdLevelResource</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-AssessedResourceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd0b1-107">리소스</span><span class="sxs-lookup"><span data-stu-id="fd0b1-107">ResourceId</span></span>
```
Remove-AzSecurityAssessment -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd0b1-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="fd0b1-108">InputObject</span></span>
```
Remove-AzSecurityAssessment -InputObject <PSSecurityAssessment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd0b1-109">설명은</span><span class="sxs-lookup"><span data-stu-id="fd0b1-109">DESCRIPTION</span></span>
<span data-ttu-id="fd0b1-110">Resoruce 삭제 되거나 특정 리소스와 평가가 관련이 없을 때 일반적으로 사용 되는 구독에서 보안 평가 결과를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd0b1-110">Deletes a security assessment result from a subscription, usually used when a resoruce is deleted or when the assessment is not relevant for a specific resource anymore</span></span>

## <span data-ttu-id="fd0b1-111">예제의</span><span class="sxs-lookup"><span data-stu-id="fd0b1-111">EXAMPLES</span></span>

### <span data-ttu-id="fd0b1-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="fd0b1-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="fd0b1-113">구독에 대 한 평가 결과를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd0b1-113">Deletes an assessment result on a subscription</span></span>

## <span data-ttu-id="fd0b1-114">변수</span><span class="sxs-lookup"><span data-stu-id="fd0b1-114">PARAMETERS</span></span>

### <span data-ttu-id="fd0b1-115">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="fd0b1-115">-AssessedResourceId</span></span>
<span data-ttu-id="fd0b1-116">평가를 계산할 리소스의 전체 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fd0b1-116">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="fd0b1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd0b1-117">-DefaultProfile</span></span>
<span data-ttu-id="fd0b1-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd0b1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd0b1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd0b1-119">-InputObject</span></span>
<span data-ttu-id="fd0b1-120">입력 개체</span><span class="sxs-lookup"><span data-stu-id="fd0b1-120">Input Object.</span></span>

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

### <span data-ttu-id="fd0b1-121">-이름</span><span class="sxs-lookup"><span data-stu-id="fd0b1-121">-Name</span></span>
<span data-ttu-id="fd0b1-122">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd0b1-122">Resource name.</span></span>

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

### <span data-ttu-id="fd0b1-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd0b1-123">-PassThru</span></span>
<span data-ttu-id="fd0b1-124">작업이 성공적으로 수행 되었는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd0b1-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="fd0b1-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd0b1-125">-ResourceId</span></span>
<span data-ttu-id="fd0b1-126">명령을 호출 하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fd0b1-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="fd0b1-127">-확인</span><span class="sxs-lookup"><span data-stu-id="fd0b1-127">-Confirm</span></span>
<span data-ttu-id="fd0b1-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd0b1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd0b1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd0b1-129">-WhatIf</span></span>
<span data-ttu-id="fd0b1-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fd0b1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd0b1-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd0b1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd0b1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd0b1-132">CommonParameters</span></span>
<span data-ttu-id="fd0b1-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd0b1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd0b1-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fd0b1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd0b1-135">입력</span><span class="sxs-lookup"><span data-stu-id="fd0b1-135">INPUTS</span></span>

### <span data-ttu-id="fd0b1-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fd0b1-136">System.String</span></span>

### <span data-ttu-id="fd0b1-137">Microsoft. Azure. a. PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="fd0b1-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="fd0b1-138">출력</span><span class="sxs-lookup"><span data-stu-id="fd0b1-138">OUTPUTS</span></span>

### <span data-ttu-id="fd0b1-139">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="fd0b1-139">System.Boolean</span></span>

## <span data-ttu-id="fd0b1-140">상속자</span><span class="sxs-lookup"><span data-stu-id="fd0b1-140">NOTES</span></span>

## <span data-ttu-id="fd0b1-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd0b1-141">RELATED LINKS</span></span>
