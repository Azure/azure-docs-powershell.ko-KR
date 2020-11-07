---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: c4a3f33094e5337306e44e2b310cd7cce32e8887
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879758"
---
# <span data-ttu-id="d2918-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d2918-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="d2918-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2918-102">SYNOPSIS</span></span>
<span data-ttu-id="d2918-103">현재 구독에서 지정 된 HDInsight 클러스터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2918-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="d2918-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d2918-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2918-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d2918-105">DESCRIPTION</span></span>
<span data-ttu-id="d2918-106">**AzHDInsightCluster** cmdlet은 지정 된 HDInsight 서비스 클러스터를 구독에서 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2918-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="d2918-107">또한이 작업은 클러스터의 Hadoop 분산 파일 시스템 (HDFS)에 저장 된 모든 데이터를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2918-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="d2918-108">연결 된 Azure 저장소 계정에 저장 된 데이터는 삭제 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d2918-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="d2918-109">외부 metastores에 저장 된 데이터는 삭제 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d2918-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="d2918-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d2918-110">EXAMPLES</span></span>

### <span data-ttu-id="d2918-111">예제 1: Azure HDInsight 클러스터 삭제</span><span class="sxs-lookup"><span data-stu-id="d2918-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="d2918-112">이 명령은-hadoop-001 이라는 클러스터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2918-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="d2918-113">변수</span><span class="sxs-lookup"><span data-stu-id="d2918-113">PARAMETERS</span></span>

### <span data-ttu-id="d2918-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d2918-114">-ClusterName</span></span>
<span data-ttu-id="d2918-115">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2918-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="d2918-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2918-116">-DefaultProfile</span></span>
<span data-ttu-id="d2918-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d2918-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2918-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2918-118">-ResourceGroupName</span></span>
<span data-ttu-id="d2918-119">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2918-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d2918-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2918-120">-PassThru</span></span>
<span data-ttu-id="d2918-121">PassThru가 있는 경우 결과를 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2918-121">If PassThru is present, output the result</span></span>

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

### <span data-ttu-id="d2918-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2918-122">CommonParameters</span></span>
<span data-ttu-id="d2918-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2918-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2918-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d2918-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2918-125">입력</span><span class="sxs-lookup"><span data-stu-id="d2918-125">INPUTS</span></span>

### <span data-ttu-id="d2918-126">않아야</span><span class="sxs-lookup"><span data-stu-id="d2918-126">None</span></span>
## <span data-ttu-id="d2918-127">출력</span><span class="sxs-lookup"><span data-stu-id="d2918-127">OUTPUTS</span></span>

### <span data-ttu-id="d2918-128">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d2918-128">System.Boolean</span></span>
## <span data-ttu-id="d2918-129">상속자</span><span class="sxs-lookup"><span data-stu-id="d2918-129">NOTES</span></span>

## <span data-ttu-id="d2918-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2918-130">RELATED LINKS</span></span>

[<span data-ttu-id="d2918-131">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d2918-131">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="d2918-132">-AzHDInsightCluster 사용</span><span class="sxs-lookup"><span data-stu-id="d2918-132">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


