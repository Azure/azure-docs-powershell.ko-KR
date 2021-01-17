---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: c62dcefc2a4cfabc908c45454f3907c2da060f6c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329654"
---
# <span data-ttu-id="cb906-101">Remove-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="cb906-101">Remove-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="cb906-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb906-102">SYNOPSIS</span></span>
<span data-ttu-id="cb906-103">작업 영역의 서비스 연결 해제</span><span class="sxs-lookup"><span data-stu-id="cb906-103">Unlink service for workspace</span></span>

## <span data-ttu-id="cb906-104">구문</span><span class="sxs-lookup"><span data-stu-id="cb906-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cb906-105">설명</span><span class="sxs-lookup"><span data-stu-id="cb906-105">DESCRIPTION</span></span>
<span data-ttu-id="cb906-106">작업 영역의 서비스 연결 해제</span><span class="sxs-lookup"><span data-stu-id="cb906-106">Unlink service for workspace</span></span>

## <span data-ttu-id="cb906-107">예제</span><span class="sxs-lookup"><span data-stu-id="cb906-107">EXAMPLES</span></span>

### <span data-ttu-id="cb906-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="cb906-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

true
```

<span data-ttu-id="cb906-109">작업 영역의 연결된 서비스 연결 해제</span><span class="sxs-lookup"><span data-stu-id="cb906-109">Unlink linked service for workspace</span></span>

## <span data-ttu-id="cb906-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb906-110">PARAMETERS</span></span>

### <span data-ttu-id="cb906-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb906-111">-AsJob</span></span>
<span data-ttu-id="cb906-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="cb906-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cb906-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb906-113">-DefaultProfile</span></span>
<span data-ttu-id="cb906-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cb906-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb906-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="cb906-115">-LinkedServiceName</span></span>
<span data-ttu-id="cb906-116">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb906-116">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb906-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb906-117">-ResourceGroupName</span></span>
<span data-ttu-id="cb906-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb906-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb906-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cb906-119">-WorkspaceName</span></span>
<span data-ttu-id="cb906-120">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb906-120">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb906-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb906-121">-Confirm</span></span>
<span data-ttu-id="cb906-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb906-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb906-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb906-123">-WhatIf</span></span>
<span data-ttu-id="cb906-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="cb906-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb906-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb906-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb906-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb906-126">CommonParameters</span></span>
<span data-ttu-id="cb906-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cb906-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb906-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cb906-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb906-129">입력</span><span class="sxs-lookup"><span data-stu-id="cb906-129">INPUTS</span></span>

### <span data-ttu-id="cb906-130">System.String</span><span class="sxs-lookup"><span data-stu-id="cb906-130">System.String</span></span>

## <span data-ttu-id="cb906-131">출력</span><span class="sxs-lookup"><span data-stu-id="cb906-131">OUTPUTS</span></span>

### <span data-ttu-id="cb906-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cb906-132">System.Boolean</span></span>

## <span data-ttu-id="cb906-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cb906-133">NOTES</span></span>

## <span data-ttu-id="cb906-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb906-134">RELATED LINKS</span></span>
