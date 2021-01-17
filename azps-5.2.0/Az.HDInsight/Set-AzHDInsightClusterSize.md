---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
ms.openlocfilehash: 8f34e9233da61bb2381c99c33922fa4332b588fd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328313"
---
# <span data-ttu-id="c620f-101">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="c620f-101">Set-AzHDInsightClusterSize</span></span>

## <span data-ttu-id="c620f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c620f-102">SYNOPSIS</span></span>
<span data-ttu-id="c620f-103">지정된 클러스터의 Worker 노드 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c620f-103">Sets the number of Worker nodes in a specified cluster.</span></span>

## <span data-ttu-id="c620f-104">구문</span><span class="sxs-lookup"><span data-stu-id="c620f-104">SYNTAX</span></span>

```
Set-AzHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c620f-105">설명</span><span class="sxs-lookup"><span data-stu-id="c620f-105">DESCRIPTION</span></span>
<span data-ttu-id="c620f-106">**Set-AzHDInsightClusterSize** cmdlet은 지정된 Azure HDInsight 클러스터의 Worker 노드 수를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c620f-106">The **Set-AzHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="c620f-107">예제</span><span class="sxs-lookup"><span data-stu-id="c620f-107">EXAMPLES</span></span>

### <span data-ttu-id="c620f-108">예제 1: 지정된 클러스터의 크기 설정</span><span class="sxs-lookup"><span data-stu-id="c620f-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="c620f-109">이 명령은 your-hadoop-001이라는 클러스터의 크기를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c620f-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="c620f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c620f-110">PARAMETERS</span></span>

### <span data-ttu-id="c620f-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c620f-111">-ClusterName</span></span>
<span data-ttu-id="c620f-112">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c620f-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c620f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c620f-113">-DefaultProfile</span></span>
<span data-ttu-id="c620f-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c620f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c620f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c620f-115">-ResourceGroupName</span></span>
<span data-ttu-id="c620f-116">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c620f-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c620f-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="c620f-117">-TargetInstanceCount</span></span>
<span data-ttu-id="c620f-118">클러스터에서 원하는 수의 Worker 노드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c620f-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c620f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c620f-119">CommonParameters</span></span>
<span data-ttu-id="c620f-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c620f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c620f-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c620f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c620f-122">입력</span><span class="sxs-lookup"><span data-stu-id="c620f-122">INPUTS</span></span>

### <span data-ttu-id="c620f-123">없음</span><span class="sxs-lookup"><span data-stu-id="c620f-123">None</span></span>

## <span data-ttu-id="c620f-124">출력</span><span class="sxs-lookup"><span data-stu-id="c620f-124">OUTPUTS</span></span>

### <span data-ttu-id="c620f-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span><span class="sxs-lookup"><span data-stu-id="c620f-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="c620f-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c620f-126">NOTES</span></span>

## <span data-ttu-id="c620f-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c620f-127">RELATED LINKS</span></span>
