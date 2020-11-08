---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/use-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
ms.openlocfilehash: 15d93d6dbdc7b231d47d5372864883f915e66ae9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217828"
---
# <span data-ttu-id="48e43-101">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="48e43-101">Use-AzHDInsightCluster</span></span>

## <span data-ttu-id="48e43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48e43-102">SYNOPSIS</span></span>
<span data-ttu-id="48e43-103">Invoke-RmAzureHDInsightHiveJob cmdlet에 사용할 클러스터를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="48e43-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

## <span data-ttu-id="48e43-104">구문과</span><span class="sxs-lookup"><span data-stu-id="48e43-104">SYNTAX</span></span>

```
Use-AzHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48e43-105">설명은</span><span class="sxs-lookup"><span data-stu-id="48e43-105">DESCRIPTION</span></span>
<span data-ttu-id="48e43-106">**AzHDInsightCluster** Cmdlet은 Hive 작업을 제출 하는 데 사용할 Invoke-AzHDInsightHiveJob cmdlet에 대 한 Azure HDInsight 클러스터를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="48e43-106">The **Use-AzHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="48e43-107">예제의</span><span class="sxs-lookup"><span data-stu-id="48e43-107">EXAMPLES</span></span>

### <span data-ttu-id="48e43-108">예제 1: 하이브 쿼리 제출을 위한 클러스터 선택</span><span class="sxs-lookup"><span data-stu-id="48e43-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="48e43-109">이 명령은 하이브 쿼리 제출에 대 한 클러스터를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="48e43-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="48e43-110">변수</span><span class="sxs-lookup"><span data-stu-id="48e43-110">PARAMETERS</span></span>

### <span data-ttu-id="48e43-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="48e43-111">-ClusterName</span></span>
<span data-ttu-id="48e43-112">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="48e43-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="48e43-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48e43-113">-DefaultProfile</span></span>
<span data-ttu-id="48e43-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="48e43-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48e43-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="48e43-115">-HttpCredential</span></span>
<span data-ttu-id="48e43-116">클러스터에 대 한 HTTP (클러스터 로그인) 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="48e43-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="48e43-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48e43-117">-ResourceGroupName</span></span>
<span data-ttu-id="48e43-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="48e43-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="48e43-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48e43-119">CommonParameters</span></span>
<span data-ttu-id="48e43-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="48e43-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48e43-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48e43-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48e43-122">입력</span><span class="sxs-lookup"><span data-stu-id="48e43-122">INPUTS</span></span>

### <span data-ttu-id="48e43-123">않아야</span><span class="sxs-lookup"><span data-stu-id="48e43-123">None</span></span>

## <span data-ttu-id="48e43-124">출력</span><span class="sxs-lookup"><span data-stu-id="48e43-124">OUTPUTS</span></span>

### <span data-ttu-id="48e43-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="48e43-125">System.String</span></span>

## <span data-ttu-id="48e43-126">상속자</span><span class="sxs-lookup"><span data-stu-id="48e43-126">NOTES</span></span>

## <span data-ttu-id="48e43-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="48e43-127">RELATED LINKS</span></span>

[<span data-ttu-id="48e43-128">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="48e43-128">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="48e43-129">제거-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="48e43-129">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)


