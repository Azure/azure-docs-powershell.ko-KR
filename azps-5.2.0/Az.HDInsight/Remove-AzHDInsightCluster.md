---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: c4a3f33094e5337306e44e2b310cd7cce32e8887
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328362"
---
# <span data-ttu-id="fce46-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="fce46-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="fce46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fce46-102">SYNOPSIS</span></span>
<span data-ttu-id="fce46-103">현재 구독에서 지정된 HDInsight 클러스터를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fce46-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="fce46-104">구문</span><span class="sxs-lookup"><span data-stu-id="fce46-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fce46-105">설명</span><span class="sxs-lookup"><span data-stu-id="fce46-105">DESCRIPTION</span></span>
<span data-ttu-id="fce46-106">**Remove-AzHDInsightCluster** cmdlet은 구독에서 지정된 HDInsight 서비스 클러스터를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fce46-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="fce46-107">또한 이 작업은 클러스터의 HDFS(Hadoop 분산 파일 시스템)에 저장된 모든 데이터를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="fce46-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="fce46-108">연결된 Azure Storage 계정에 저장된 데이터는 삭제되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fce46-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="fce46-109">외부 메타스토어에 저장된 데이터는 삭제되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fce46-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="fce46-110">예제</span><span class="sxs-lookup"><span data-stu-id="fce46-110">EXAMPLES</span></span>

### <span data-ttu-id="fce46-111">예제 1: Azure HDInsight 클러스터 삭제</span><span class="sxs-lookup"><span data-stu-id="fce46-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="fce46-112">이 명령은 your-hadoop-001이라는 클러스터를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fce46-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="fce46-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fce46-113">PARAMETERS</span></span>

### <span data-ttu-id="fce46-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="fce46-114">-ClusterName</span></span>
<span data-ttu-id="fce46-115">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fce46-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="fce46-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fce46-116">-DefaultProfile</span></span>
<span data-ttu-id="fce46-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fce46-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fce46-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fce46-118">-ResourceGroupName</span></span>
<span data-ttu-id="fce46-119">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fce46-119">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fce46-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fce46-120">-PassThru</span></span>
<span data-ttu-id="fce46-121">PassThru가 있는 경우 결과를 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="fce46-121">If PassThru is present, output the result</span></span>

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

### <span data-ttu-id="fce46-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fce46-122">CommonParameters</span></span>
<span data-ttu-id="fce46-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fce46-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fce46-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fce46-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fce46-125">입력</span><span class="sxs-lookup"><span data-stu-id="fce46-125">INPUTS</span></span>

### <span data-ttu-id="fce46-126">없음</span><span class="sxs-lookup"><span data-stu-id="fce46-126">None</span></span>
## <span data-ttu-id="fce46-127">출력</span><span class="sxs-lookup"><span data-stu-id="fce46-127">OUTPUTS</span></span>

### <span data-ttu-id="fce46-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fce46-128">System.Boolean</span></span>
## <span data-ttu-id="fce46-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fce46-129">NOTES</span></span>

## <span data-ttu-id="fce46-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fce46-130">RELATED LINKS</span></span>

[<span data-ttu-id="fce46-131">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="fce46-131">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="fce46-132">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="fce46-132">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


