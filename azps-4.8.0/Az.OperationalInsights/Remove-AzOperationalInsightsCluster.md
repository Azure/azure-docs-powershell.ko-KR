---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
ms.openlocfilehash: 4bcc62d3b5bd52382c5d02eb3761c51af27c1ca3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214029"
---
# <span data-ttu-id="1e9c7-101">Remove-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="1e9c7-101">Remove-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="1e9c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e9c7-102">SYNOPSIS</span></span>
<span data-ttu-id="1e9c7-103">클러스터 삭제</span><span class="sxs-lookup"><span data-stu-id="1e9c7-103">Delete cluster</span></span>

## <span data-ttu-id="1e9c7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1e9c7-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e9c7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1e9c7-105">DESCRIPTION</span></span>
<span data-ttu-id="1e9c7-106">클러스터 삭제, 프로 비전 상태가 "성공" 인 클러스터에만 적용</span><span class="sxs-lookup"><span data-stu-id="1e9c7-106">Delete cluster, only apply to clusters with provisioning state "Succeeded"</span></span>

## <span data-ttu-id="1e9c7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1e9c7-107">EXAMPLES</span></span>

### <span data-ttu-id="1e9c7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1e9c7-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

true
```

<span data-ttu-id="1e9c7-109">클러스터 삭제</span><span class="sxs-lookup"><span data-stu-id="1e9c7-109">Delete cluster</span></span>

## <span data-ttu-id="1e9c7-110">변수</span><span class="sxs-lookup"><span data-stu-id="1e9c7-110">PARAMETERS</span></span>

### <span data-ttu-id="1e9c7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e9c7-111">-AsJob</span></span>
<span data-ttu-id="1e9c7-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1e9c7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e9c7-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1e9c7-113">-ClusterName</span></span>
<span data-ttu-id="1e9c7-114">클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1e9c7-114">The cluster name.</span></span>

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

### <span data-ttu-id="1e9c7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e9c7-115">-DefaultProfile</span></span>
<span data-ttu-id="1e9c7-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1e9c7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e9c7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e9c7-117">-ResourceGroupName</span></span>
<span data-ttu-id="1e9c7-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1e9c7-118">The resource group name.</span></span>

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

### <span data-ttu-id="1e9c7-119">-확인</span><span class="sxs-lookup"><span data-stu-id="1e9c7-119">-Confirm</span></span>
<span data-ttu-id="1e9c7-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e9c7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e9c7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e9c7-121">-WhatIf</span></span>
<span data-ttu-id="1e9c7-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1e9c7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e9c7-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e9c7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e9c7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e9c7-124">CommonParameters</span></span>
<span data-ttu-id="1e9c7-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e9c7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e9c7-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1e9c7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e9c7-127">입력</span><span class="sxs-lookup"><span data-stu-id="1e9c7-127">INPUTS</span></span>

### <span data-ttu-id="1e9c7-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1e9c7-128">System.String</span></span>

## <span data-ttu-id="1e9c7-129">출력</span><span class="sxs-lookup"><span data-stu-id="1e9c7-129">OUTPUTS</span></span>

### <span data-ttu-id="1e9c7-130">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1e9c7-130">System.Boolean</span></span>

## <span data-ttu-id="1e9c7-131">상속자</span><span class="sxs-lookup"><span data-stu-id="1e9c7-131">NOTES</span></span>

## <span data-ttu-id="1e9c7-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e9c7-132">RELATED LINKS</span></span>
