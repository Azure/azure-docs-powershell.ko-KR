---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 8a78fc36e13360babc43b512dccee80550b3fbf9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989851"
---
# <span data-ttu-id="e0a0d-101">Remove-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="e0a0d-101">Remove-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="e0a0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0a0d-102">SYNOPSIS</span></span>
<span data-ttu-id="e0a0d-103">작업 영역의 서비스 연결 해제</span><span class="sxs-lookup"><span data-stu-id="e0a0d-103">Unlink service for workspace</span></span>

## <span data-ttu-id="e0a0d-104">구문</span><span class="sxs-lookup"><span data-stu-id="e0a0d-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0a0d-105">설명</span><span class="sxs-lookup"><span data-stu-id="e0a0d-105">DESCRIPTION</span></span>
<span data-ttu-id="e0a0d-106">작업 영역의 서비스 연결 해제</span><span class="sxs-lookup"><span data-stu-id="e0a0d-106">Unlink service for workspace</span></span>

## <span data-ttu-id="e0a0d-107">예제</span><span class="sxs-lookup"><span data-stu-id="e0a0d-107">EXAMPLES</span></span>

### <span data-ttu-id="e0a0d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e0a0d-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

true
```

<span data-ttu-id="e0a0d-109">작업 영역의 연결된 서비스 연결 해제</span><span class="sxs-lookup"><span data-stu-id="e0a0d-109">Unlink linked service for workspace</span></span>

## <span data-ttu-id="e0a0d-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e0a0d-110">PARAMETERS</span></span>

### <span data-ttu-id="e0a0d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0a0d-111">-AsJob</span></span>
<span data-ttu-id="e0a0d-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e0a0d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e0a0d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0a0d-113">-DefaultProfile</span></span>
<span data-ttu-id="e0a0d-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e0a0d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0a0d-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="e0a0d-115">-LinkedServiceName</span></span>
<span data-ttu-id="e0a0d-116">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e0a0d-116">The Workspace name.</span></span>

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

### <span data-ttu-id="e0a0d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0a0d-117">-ResourceGroupName</span></span>
<span data-ttu-id="e0a0d-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e0a0d-118">The resource group name.</span></span>

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

### <span data-ttu-id="e0a0d-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e0a0d-119">-WorkspaceName</span></span>
<span data-ttu-id="e0a0d-120">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e0a0d-120">The Workspace name.</span></span>

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

### <span data-ttu-id="e0a0d-121">-확인</span><span class="sxs-lookup"><span data-stu-id="e0a0d-121">-Confirm</span></span>
<span data-ttu-id="e0a0d-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0a0d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0a0d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0a0d-123">-WhatIf</span></span>
<span data-ttu-id="e0a0d-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e0a0d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0a0d-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e0a0d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0a0d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0a0d-126">CommonParameters</span></span>
<span data-ttu-id="e0a0d-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e0a0d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0a0d-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0a0d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0a0d-129">입력</span><span class="sxs-lookup"><span data-stu-id="e0a0d-129">INPUTS</span></span>

### <span data-ttu-id="e0a0d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e0a0d-130">System.String</span></span>

## <span data-ttu-id="e0a0d-131">출력</span><span class="sxs-lookup"><span data-stu-id="e0a0d-131">OUTPUTS</span></span>

### <span data-ttu-id="e0a0d-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e0a0d-132">System.Boolean</span></span>

## <span data-ttu-id="e0a0d-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e0a0d-133">NOTES</span></span>

## <span data-ttu-id="e0a0d-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0a0d-134">RELATED LINKS</span></span>
