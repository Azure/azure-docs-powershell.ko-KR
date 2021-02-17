---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
ms.openlocfilehash: 4bcc62d3b5bd52382c5d02eb3761c51af27c1ca3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202336"
---
# <span data-ttu-id="3a329-101">Remove-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="3a329-101">Remove-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="3a329-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a329-102">SYNOPSIS</span></span>
<span data-ttu-id="3a329-103">클러스터 삭제</span><span class="sxs-lookup"><span data-stu-id="3a329-103">Delete cluster</span></span>

## <span data-ttu-id="3a329-104">구문</span><span class="sxs-lookup"><span data-stu-id="3a329-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a329-105">설명</span><span class="sxs-lookup"><span data-stu-id="3a329-105">DESCRIPTION</span></span>
<span data-ttu-id="3a329-106">클러스터 삭제, 프로비전 상태가 "성공"인 클러스터에만 적용</span><span class="sxs-lookup"><span data-stu-id="3a329-106">Delete cluster, only apply to clusters with provisioning state "Succeeded"</span></span>

## <span data-ttu-id="3a329-107">예제</span><span class="sxs-lookup"><span data-stu-id="3a329-107">EXAMPLES</span></span>

### <span data-ttu-id="3a329-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3a329-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

true
```

<span data-ttu-id="3a329-109">클러스터 삭제</span><span class="sxs-lookup"><span data-stu-id="3a329-109">Delete cluster</span></span>

## <span data-ttu-id="3a329-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a329-110">PARAMETERS</span></span>

### <span data-ttu-id="3a329-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a329-111">-AsJob</span></span>
<span data-ttu-id="3a329-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3a329-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a329-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3a329-113">-ClusterName</span></span>
<span data-ttu-id="3a329-114">클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3a329-114">The cluster name.</span></span>

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

### <span data-ttu-id="3a329-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a329-115">-DefaultProfile</span></span>
<span data-ttu-id="3a329-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3a329-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a329-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a329-117">-ResourceGroupName</span></span>
<span data-ttu-id="3a329-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3a329-118">The resource group name.</span></span>

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

### <span data-ttu-id="3a329-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a329-119">-Confirm</span></span>
<span data-ttu-id="3a329-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a329-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a329-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a329-121">-WhatIf</span></span>
<span data-ttu-id="3a329-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3a329-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a329-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a329-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a329-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a329-124">CommonParameters</span></span>
<span data-ttu-id="3a329-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3a329-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a329-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3a329-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a329-127">입력</span><span class="sxs-lookup"><span data-stu-id="3a329-127">INPUTS</span></span>

### <span data-ttu-id="3a329-128">System.String</span><span class="sxs-lookup"><span data-stu-id="3a329-128">System.String</span></span>

## <span data-ttu-id="3a329-129">출력</span><span class="sxs-lookup"><span data-stu-id="3a329-129">OUTPUTS</span></span>

### <span data-ttu-id="3a329-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3a329-130">System.Boolean</span></span>

## <span data-ttu-id="3a329-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3a329-131">NOTES</span></span>

## <span data-ttu-id="3a329-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a329-132">RELATED LINKS</span></span>
