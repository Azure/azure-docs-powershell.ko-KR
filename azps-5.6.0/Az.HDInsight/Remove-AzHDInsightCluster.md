---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: 5baf67bfec2c4e18e718241dbb973bb8b2050bbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965899"
---
# <span data-ttu-id="a5d30-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a5d30-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="a5d30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5d30-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d30-103">현재 구독에서 지정된 HDInsight 클러스터를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d30-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="a5d30-104">구문</span><span class="sxs-lookup"><span data-stu-id="a5d30-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5d30-105">설명</span><span class="sxs-lookup"><span data-stu-id="a5d30-105">DESCRIPTION</span></span>
<span data-ttu-id="a5d30-106">**Remove-AzHDInsightCluster** cmdlet은 구독에서 지정된 HDInsight 서비스 클러스터를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d30-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="a5d30-107">또한 이 작업은 클러스터의 HDFS(Hadoop 분산 파일 시스템)에 저장된 모든 데이터를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d30-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="a5d30-108">연결된 Azure Storage 계정에 저장된 데이터는 삭제되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5d30-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="a5d30-109">외부 메타스토어에 저장된 데이터는 삭제되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5d30-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="a5d30-110">예제</span><span class="sxs-lookup"><span data-stu-id="a5d30-110">EXAMPLES</span></span>

### <span data-ttu-id="a5d30-111">예제 1: Azure HDInsight 클러스터 삭제</span><span class="sxs-lookup"><span data-stu-id="a5d30-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="a5d30-112">이 명령은 your-hadoop-001이라는 클러스터를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d30-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="a5d30-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a5d30-113">PARAMETERS</span></span>

### <span data-ttu-id="a5d30-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a5d30-114">-ClusterName</span></span>
<span data-ttu-id="a5d30-115">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d30-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="a5d30-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5d30-116">-DefaultProfile</span></span>
<span data-ttu-id="a5d30-117">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a5d30-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5d30-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5d30-118">-PassThru</span></span>
<span data-ttu-id="a5d30-119">PassThru가 있는 경우 결과를 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d30-119">If PassThru is present, output the result</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d30-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5d30-120">-ResourceGroupName</span></span>
<span data-ttu-id="a5d30-121">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d30-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a5d30-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d30-122">CommonParameters</span></span>
<span data-ttu-id="a5d30-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d30-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d30-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5d30-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d30-125">입력</span><span class="sxs-lookup"><span data-stu-id="a5d30-125">INPUTS</span></span>

### <span data-ttu-id="a5d30-126">없음</span><span class="sxs-lookup"><span data-stu-id="a5d30-126">None</span></span>
## <span data-ttu-id="a5d30-127">출력</span><span class="sxs-lookup"><span data-stu-id="a5d30-127">OUTPUTS</span></span>

### <span data-ttu-id="a5d30-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a5d30-128">System.Boolean</span></span>
## <span data-ttu-id="a5d30-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a5d30-129">NOTES</span></span>

## <span data-ttu-id="a5d30-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5d30-130">RELATED LINKS</span></span>

[<span data-ttu-id="a5d30-131">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a5d30-131">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="a5d30-132">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a5d30-132">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


