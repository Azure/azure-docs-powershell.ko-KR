---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/use-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
ms.openlocfilehash: c8a58963e66c8260a0001c144230cabf3a80b295
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711433"
---
# <span data-ttu-id="0fa1f-101">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="0fa1f-101">Use-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="0fa1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fa1f-102">SYNOPSIS</span></span>
<span data-ttu-id="0fa1f-103">Invoke-RmAzureHDInsightHiveJob cmdlet에 사용할 클러스터를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fa1f-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fa1f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0fa1f-104">SYNTAX</span></span>

```
Use-AzureRmHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fa1f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0fa1f-105">DESCRIPTION</span></span>
<span data-ttu-id="0fa1f-106">**AzureRmHDInsightCluster** Cmdlet은 Hive 작업을 제출 하는 데 사용할 Invoke-AzureRmHDInsightHiveJob cmdlet에 대 한 Azure HDInsight 클러스터를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fa1f-106">The **Use-AzureRmHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzureRmHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="0fa1f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0fa1f-107">EXAMPLES</span></span>

### <span data-ttu-id="0fa1f-108">예제 1: 하이브 쿼리 제출을 위한 클러스터 선택</span><span class="sxs-lookup"><span data-stu-id="0fa1f-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzureRmHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="0fa1f-109">이 명령은 하이브 쿼리 제출에 대 한 클러스터를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fa1f-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="0fa1f-110">변수</span><span class="sxs-lookup"><span data-stu-id="0fa1f-110">PARAMETERS</span></span>

### <span data-ttu-id="0fa1f-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0fa1f-111">-ClusterName</span></span>
<span data-ttu-id="0fa1f-112">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fa1f-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="0fa1f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fa1f-113">-DefaultProfile</span></span>
<span data-ttu-id="0fa1f-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0fa1f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fa1f-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="0fa1f-115">-HttpCredential</span></span>
<span data-ttu-id="0fa1f-116">클러스터에 대 한 HTTP (클러스터 로그인) 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fa1f-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fa1f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fa1f-117">-ResourceGroupName</span></span>
<span data-ttu-id="0fa1f-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fa1f-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0fa1f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fa1f-119">CommonParameters</span></span>
<span data-ttu-id="0fa1f-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fa1f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fa1f-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fa1f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fa1f-122">입력</span><span class="sxs-lookup"><span data-stu-id="0fa1f-122">INPUTS</span></span>

### <span data-ttu-id="0fa1f-123">않아야</span><span class="sxs-lookup"><span data-stu-id="0fa1f-123">None</span></span>
<span data-ttu-id="0fa1f-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0fa1f-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0fa1f-125">출력</span><span class="sxs-lookup"><span data-stu-id="0fa1f-125">OUTPUTS</span></span>

### <span data-ttu-id="0fa1f-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0fa1f-126">System.String</span></span>

## <span data-ttu-id="0fa1f-127">상속자</span><span class="sxs-lookup"><span data-stu-id="0fa1f-127">NOTES</span></span>

## <span data-ttu-id="0fa1f-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0fa1f-128">RELATED LINKS</span></span>

[<span data-ttu-id="0fa1f-129">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="0fa1f-129">Get-AzureRmHDInsightCluster</span></span>](./Get-AzureRmHDInsightCluster.md)

[<span data-ttu-id="0fa1f-130">제거-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="0fa1f-130">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)


