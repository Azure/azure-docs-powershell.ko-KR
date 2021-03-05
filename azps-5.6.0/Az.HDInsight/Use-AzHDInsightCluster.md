---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/use-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
ms.openlocfilehash: c9b95a1f16c90eb3c6e057707dbf63d431b9a1ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013552"
---
# <span data-ttu-id="e9a46-101">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e9a46-101">Use-AzHDInsightCluster</span></span>

## <span data-ttu-id="e9a46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9a46-102">SYNOPSIS</span></span>
<span data-ttu-id="e9a46-103">cmdlet과 함께 사용할 클러스터를 Invoke-RmAzureHDInsightHiveJob 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a46-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

## <span data-ttu-id="e9a46-104">구문</span><span class="sxs-lookup"><span data-stu-id="e9a46-104">SYNTAX</span></span>

```
Use-AzHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9a46-105">설명</span><span class="sxs-lookup"><span data-stu-id="e9a46-105">DESCRIPTION</span></span>
<span data-ttu-id="e9a46-106">**Use-AzHDInsightCluster** cmdlet은 Hive 작업을 제출하는 데 사용할 Invoke-AzHDInsightHiveJob azure HDInsight 클러스터를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a46-106">The **Use-AzHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="e9a46-107">예제</span><span class="sxs-lookup"><span data-stu-id="e9a46-107">EXAMPLES</span></span>

### <span data-ttu-id="e9a46-108">예제 1: Hive 쿼리 제출에 대한 클러스터 선택</span><span class="sxs-lookup"><span data-stu-id="e9a46-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="e9a46-109">이 명령은 Hive 쿼리 제출에 대한 클러스터를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a46-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="e9a46-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e9a46-110">PARAMETERS</span></span>

### <span data-ttu-id="e9a46-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e9a46-111">-ClusterName</span></span>
<span data-ttu-id="e9a46-112">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a46-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="e9a46-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9a46-113">-DefaultProfile</span></span>
<span data-ttu-id="e9a46-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e9a46-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9a46-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="e9a46-115">-HttpCredential</span></span>
<span data-ttu-id="e9a46-116">클러스터에 대한 HTTP(클러스터 로그인) 자격 증명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a46-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9a46-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9a46-117">-ResourceGroupName</span></span>
<span data-ttu-id="e9a46-118">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a46-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e9a46-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9a46-119">CommonParameters</span></span>
<span data-ttu-id="e9a46-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a46-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9a46-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9a46-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9a46-122">입력</span><span class="sxs-lookup"><span data-stu-id="e9a46-122">INPUTS</span></span>

### <span data-ttu-id="e9a46-123">없음</span><span class="sxs-lookup"><span data-stu-id="e9a46-123">None</span></span>

## <span data-ttu-id="e9a46-124">출력</span><span class="sxs-lookup"><span data-stu-id="e9a46-124">OUTPUTS</span></span>

### <span data-ttu-id="e9a46-125">System.String</span><span class="sxs-lookup"><span data-stu-id="e9a46-125">System.String</span></span>

## <span data-ttu-id="e9a46-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e9a46-126">NOTES</span></span>

## <span data-ttu-id="e9a46-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9a46-127">RELATED LINKS</span></span>

[<span data-ttu-id="e9a46-128">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e9a46-128">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="e9a46-129">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e9a46-129">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)


