---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
ms.openlocfilehash: 01f9a2a9bae03606773c146f44f7e737fb9b613f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711552"
---
# <span data-ttu-id="f15a2-101">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f15a2-101">Use-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="f15a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f15a2-102">SYNOPSIS</span></span>
<span data-ttu-id="f15a2-103">Invoke-RmAzureHDInsightHiveJob cmdlet에 사용할 클러스터를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f15a2-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f15a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f15a2-104">SYNTAX</span></span>

```
Use-AzureRmHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f15a2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f15a2-105">DESCRIPTION</span></span>
<span data-ttu-id="f15a2-106">**AzureRmHDInsightCluster** Cmdlet은 Hive 작업을 제출 하는 데 사용할 Invoke-AzureRmHDInsightHiveJob cmdlet에 대 한 Azure HDInsight 클러스터를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f15a2-106">The **Use-AzureRmHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzureRmHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="f15a2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f15a2-107">EXAMPLES</span></span>

### <span data-ttu-id="f15a2-108">예제 1: 하이브 쿼리 제출을 위한 클러스터 선택</span><span class="sxs-lookup"><span data-stu-id="f15a2-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzureRmHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="f15a2-109">이 명령은 하이브 쿼리 제출에 대 한 클러스터를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f15a2-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="f15a2-110">변수</span><span class="sxs-lookup"><span data-stu-id="f15a2-110">PARAMETERS</span></span>

### <span data-ttu-id="f15a2-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f15a2-111">-ClusterName</span></span>
<span data-ttu-id="f15a2-112">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f15a2-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="f15a2-113">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="f15a2-113">-HttpCredential</span></span>
<span data-ttu-id="f15a2-114">클러스터에 대 한 HTTP (클러스터 로그인) 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f15a2-114">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="f15a2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f15a2-115">-ResourceGroupName</span></span>
<span data-ttu-id="f15a2-116">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f15a2-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f15a2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f15a2-117">-DefaultProfile</span></span>
<span data-ttu-id="f15a2-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f15a2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f15a2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f15a2-119">CommonParameters</span></span>
<span data-ttu-id="f15a2-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f15a2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f15a2-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f15a2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f15a2-122">입력</span><span class="sxs-lookup"><span data-stu-id="f15a2-122">INPUTS</span></span>

## <span data-ttu-id="f15a2-123">출력</span><span class="sxs-lookup"><span data-stu-id="f15a2-123">OUTPUTS</span></span>

### <span data-ttu-id="f15a2-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f15a2-124">System.String</span></span>

## <span data-ttu-id="f15a2-125">상속자</span><span class="sxs-lookup"><span data-stu-id="f15a2-125">NOTES</span></span>

## <span data-ttu-id="f15a2-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f15a2-126">RELATED LINKS</span></span>

[<span data-ttu-id="f15a2-127">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f15a2-127">Get-AzureRmHDInsightCluster</span></span>](./Get-AzureRmHDInsightCluster.md)

[<span data-ttu-id="f15a2-128">제거-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f15a2-128">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)


