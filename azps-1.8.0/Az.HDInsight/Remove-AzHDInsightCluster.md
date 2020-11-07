---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: e52d838f0aa7ce901b8099710b38f570d4285a4c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868222"
---
# <span data-ttu-id="68a8c-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="68a8c-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="68a8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68a8c-102">SYNOPSIS</span></span>
<span data-ttu-id="68a8c-103">현재 구독에서 지정 된 HDInsight 클러스터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a8c-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="68a8c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="68a8c-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68a8c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="68a8c-105">DESCRIPTION</span></span>
<span data-ttu-id="68a8c-106">**AzHDInsightCluster** cmdlet은 지정 된 HDInsight 서비스 클러스터를 구독에서 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a8c-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="68a8c-107">또한이 작업은 클러스터의 Hadoop 분산 파일 시스템 (HDFS)에 저장 된 모든 데이터를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a8c-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="68a8c-108">연결 된 Azure 저장소 계정에 저장 된 데이터는 삭제 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68a8c-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="68a8c-109">외부 metastores에 저장 된 데이터는 삭제 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68a8c-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="68a8c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="68a8c-110">EXAMPLES</span></span>

### <span data-ttu-id="68a8c-111">예제 1: Azure HDInsight 클러스터 삭제</span><span class="sxs-lookup"><span data-stu-id="68a8c-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="68a8c-112">이 명령은-hadoop-001 이라는 클러스터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a8c-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="68a8c-113">변수</span><span class="sxs-lookup"><span data-stu-id="68a8c-113">PARAMETERS</span></span>

### <span data-ttu-id="68a8c-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="68a8c-114">-ClusterName</span></span>
<span data-ttu-id="68a8c-115">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a8c-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="68a8c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68a8c-116">-DefaultProfile</span></span>
<span data-ttu-id="68a8c-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="68a8c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68a8c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68a8c-118">-ResourceGroupName</span></span>
<span data-ttu-id="68a8c-119">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a8c-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="68a8c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68a8c-120">CommonParameters</span></span>
<span data-ttu-id="68a8c-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a8c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68a8c-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68a8c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68a8c-123">입력</span><span class="sxs-lookup"><span data-stu-id="68a8c-123">INPUTS</span></span>

### <span data-ttu-id="68a8c-124">않아야</span><span class="sxs-lookup"><span data-stu-id="68a8c-124">None</span></span>

## <span data-ttu-id="68a8c-125">출력</span><span class="sxs-lookup"><span data-stu-id="68a8c-125">OUTPUTS</span></span>

### <span data-ttu-id="68a8c-126">Microsoft. Azure. 관리. ClusterGetResponse</span><span class="sxs-lookup"><span data-stu-id="68a8c-126">Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse</span></span>

## <span data-ttu-id="68a8c-127">상속자</span><span class="sxs-lookup"><span data-stu-id="68a8c-127">NOTES</span></span>

## <span data-ttu-id="68a8c-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68a8c-128">RELATED LINKS</span></span>

[<span data-ttu-id="68a8c-129">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="68a8c-129">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="68a8c-130">-AzHDInsightCluster 사용</span><span class="sxs-lookup"><span data-stu-id="68a8c-130">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


