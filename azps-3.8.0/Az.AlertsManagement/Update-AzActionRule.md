---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 2af687a79255d5e5ab4b49135bf8a8f7b8f819f1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034654"
---
# <span data-ttu-id="34de9-101">Update-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="34de9-101">Update-AzActionRule</span></span>

## <span data-ttu-id="34de9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34de9-102">SYNOPSIS</span></span>
<span data-ttu-id="34de9-103">작업 규칙 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="34de9-103">Updates action rule properties.</span></span>

## <span data-ttu-id="34de9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="34de9-104">SYNTAX</span></span>

### <span data-ttu-id="34de9-105">ByNameSimplifiedPatch (기본값)</span><span class="sxs-lookup"><span data-stu-id="34de9-105">ByNameSimplifiedPatch (Default)</span></span>
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34de9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="34de9-106">ByResourceId</span></span>
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34de9-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="34de9-107">ByInputObject</span></span>
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34de9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="34de9-108">DESCRIPTION</span></span>
<span data-ttu-id="34de9-109">**업데이트-AzActionRule** cmdlet은 작업 규칙 속성-상태 및 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="34de9-109">**Update-AzActionRule** cmdlet updates action rule properties - status and tags.</span></span>

## <span data-ttu-id="34de9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="34de9-110">EXAMPLES</span></span>

### <span data-ttu-id="34de9-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="34de9-111">Example 1</span></span>
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

<span data-ttu-id="34de9-112">이 cmdlet은 작업 규칙을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34de9-112">This cmdlet disables the action rule.</span></span> 

## <span data-ttu-id="34de9-113">변수</span><span class="sxs-lookup"><span data-stu-id="34de9-113">PARAMETERS</span></span>

### <span data-ttu-id="34de9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34de9-114">-DefaultProfile</span></span>
<span data-ttu-id="34de9-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="34de9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34de9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34de9-116">-InputObject</span></span>
<span data-ttu-id="34de9-117">작업 규칙 리소스</span><span class="sxs-lookup"><span data-stu-id="34de9-117">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34de9-118">-이름</span><span class="sxs-lookup"><span data-stu-id="34de9-118">-Name</span></span>
<span data-ttu-id="34de9-119">작업 규칙 이름</span><span class="sxs-lookup"><span data-stu-id="34de9-119">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34de9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34de9-120">-ResourceGroupName</span></span>
<span data-ttu-id="34de9-121">작업 규칙 이름</span><span class="sxs-lookup"><span data-stu-id="34de9-121">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34de9-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34de9-122">-ResourceId</span></span>
<span data-ttu-id="34de9-123">작업 규칙의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="34de9-123">The resource id of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34de9-124">-상태</span><span class="sxs-lookup"><span data-stu-id="34de9-124">-Status</span></span>
<span data-ttu-id="34de9-125">작업 규칙 상태</span><span class="sxs-lookup"><span data-stu-id="34de9-125">Action rule status</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34de9-126">태그</span><span class="sxs-lookup"><span data-stu-id="34de9-126">-Tag</span></span>
<span data-ttu-id="34de9-127">작업 규칙 태그</span><span class="sxs-lookup"><span data-stu-id="34de9-127">Action rule tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34de9-128">-확인</span><span class="sxs-lookup"><span data-stu-id="34de9-128">-Confirm</span></span>
<span data-ttu-id="34de9-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="34de9-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34de9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34de9-130">-WhatIf</span></span>
<span data-ttu-id="34de9-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="34de9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34de9-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34de9-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34de9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34de9-133">CommonParameters</span></span>
<span data-ttu-id="34de9-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="34de9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34de9-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="34de9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34de9-136">입력</span><span class="sxs-lookup"><span data-stu-id="34de9-136">INPUTS</span></span>

### <span data-ttu-id="34de9-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="34de9-137">System.String</span></span>

### <span data-ttu-id="34de9-138">AlertsManagement 모델. a PSActionRule</span><span class="sxs-lookup"><span data-stu-id="34de9-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="34de9-139">출력</span><span class="sxs-lookup"><span data-stu-id="34de9-139">OUTPUTS</span></span>

### <span data-ttu-id="34de9-140">AlertsManagement 모델. a PSActionRule</span><span class="sxs-lookup"><span data-stu-id="34de9-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="34de9-141">상속자</span><span class="sxs-lookup"><span data-stu-id="34de9-141">NOTES</span></span>

## <span data-ttu-id="34de9-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34de9-142">RELATED LINKS</span></span>
