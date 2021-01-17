---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
ms.openlocfilehash: 7dae5bd29877097b7d0df60feff8bf44977e61f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489591"
---
# <span data-ttu-id="f4f38-101">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="f4f38-101">Set-AzHDInsightClusterSize</span></span>

## <span data-ttu-id="f4f38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4f38-102">SYNOPSIS</span></span>
<span data-ttu-id="f4f38-103">지정된 클러스터의 Worker 노드 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f38-103">Sets the number of Worker nodes in a specified cluster.</span></span>

## <span data-ttu-id="f4f38-104">구문</span><span class="sxs-lookup"><span data-stu-id="f4f38-104">SYNTAX</span></span>

```
Set-AzHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4f38-105">설명</span><span class="sxs-lookup"><span data-stu-id="f4f38-105">DESCRIPTION</span></span>
<span data-ttu-id="f4f38-106">**Set-AzHDInsightClusterSize** cmdlet은 지정된 Azure HDInsight 클러스터의 Worker 노드 수를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f38-106">The **Set-AzHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="f4f38-107">예제</span><span class="sxs-lookup"><span data-stu-id="f4f38-107">EXAMPLES</span></span>

### <span data-ttu-id="f4f38-108">예제 1: 지정된 클러스터의 크기 설정</span><span class="sxs-lookup"><span data-stu-id="f4f38-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="f4f38-109">이 명령은 your-hadoop-001이라는 클러스터의 크기를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f38-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="f4f38-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4f38-110">PARAMETERS</span></span>

### <span data-ttu-id="f4f38-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f4f38-111">-ClusterName</span></span>
<span data-ttu-id="f4f38-112">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f38-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="f4f38-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4f38-113">-DefaultProfile</span></span>
<span data-ttu-id="f4f38-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f4f38-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4f38-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4f38-115">-ResourceGroupName</span></span>
<span data-ttu-id="f4f38-116">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f38-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f4f38-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="f4f38-117">-TargetInstanceCount</span></span>
<span data-ttu-id="f4f38-118">클러스터에서 원하는 수의 Worker 노드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f38-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

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

### <span data-ttu-id="f4f38-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4f38-119">CommonParameters</span></span>
<span data-ttu-id="f4f38-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f38-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4f38-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f4f38-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4f38-122">입력</span><span class="sxs-lookup"><span data-stu-id="f4f38-122">INPUTS</span></span>

### <span data-ttu-id="f4f38-123">없음</span><span class="sxs-lookup"><span data-stu-id="f4f38-123">None</span></span>

## <span data-ttu-id="f4f38-124">출력</span><span class="sxs-lookup"><span data-stu-id="f4f38-124">OUTPUTS</span></span>

### <span data-ttu-id="f4f38-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span><span class="sxs-lookup"><span data-stu-id="f4f38-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="f4f38-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f4f38-126">NOTES</span></span>

## <span data-ttu-id="f4f38-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f4f38-127">RELATED LINKS</span></span>
