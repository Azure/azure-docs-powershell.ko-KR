---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/wait-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
ms.openlocfilehash: 4c1d991d3236c8e631b2b5c7f0026e91af2f8cf2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185849"
---
# <span data-ttu-id="e1f9e-101">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e1f9e-101">Wait-AzHDInsightJob</span></span>

## <span data-ttu-id="e1f9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1f9e-102">SYNOPSIS</span></span>
<span data-ttu-id="e1f9e-103">지정된 작업의 완료 또는 실패를 기다릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-103">Waits for the completion or failure of a specified job.</span></span>

## <span data-ttu-id="e1f9e-104">구문</span><span class="sxs-lookup"><span data-stu-id="e1f9e-104">SYNTAX</span></span>

```
Wait-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1f9e-105">설명</span><span class="sxs-lookup"><span data-stu-id="e1f9e-105">DESCRIPTION</span></span>
<span data-ttu-id="e1f9e-106">**Wait-AzHDInsightJob** cmdlet은 Azure HDInsight 작업의 완료 또는 실패를 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-106">The **Wait-AzHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="e1f9e-107">예제</span><span class="sxs-lookup"><span data-stu-id="e1f9e-107">EXAMPLES</span></span>

### <span data-ttu-id="e1f9e-108">예제 1: 작업 완료 또는 실패 대기</span><span class="sxs-lookup"><span data-stu-id="e1f9e-108">Example 1: Wait for the completion or failure of a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Wait-AzHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="e1f9e-109">이 명령은 작업의 완료 또는 실패를 기다릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="e1f9e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1f9e-110">PARAMETERS</span></span>

### <span data-ttu-id="e1f9e-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e1f9e-111">-ClusterName</span></span>
<span data-ttu-id="e1f9e-112">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="e1f9e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1f9e-113">-DefaultProfile</span></span>
<span data-ttu-id="e1f9e-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e1f9e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1f9e-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="e1f9e-115">-HttpCredential</span></span>
<span data-ttu-id="e1f9e-116">클러스터에 대한 클러스터 로그인(HTTP) 자격 증명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f9e-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="e1f9e-117">-JobId</span></span>
<span data-ttu-id="e1f9e-118">작업의 작업 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-118">Specifies the job ID of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f9e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1f9e-119">-ResourceGroupName</span></span>
<span data-ttu-id="e1f9e-120">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e1f9e-121">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="e1f9e-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="e1f9e-122">작업 완료를 기다리는 총 시간(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-122">The total time to wait for job completion, in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f9e-123">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="e1f9e-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="e1f9e-124">작업 상태 검사 사이의 대기 시간(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-124">The time to wait between job status checks, in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f9e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1f9e-125">CommonParameters</span></span>
<span data-ttu-id="e1f9e-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1f9e-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1f9e-128">입력</span><span class="sxs-lookup"><span data-stu-id="e1f9e-128">INPUTS</span></span>

### <span data-ttu-id="e1f9e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e1f9e-129">System.String</span></span>

## <span data-ttu-id="e1f9e-130">출력</span><span class="sxs-lookup"><span data-stu-id="e1f9e-130">OUTPUTS</span></span>

### <span data-ttu-id="e1f9e-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e1f9e-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="e1f9e-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e1f9e-132">NOTES</span></span>

## <span data-ttu-id="e1f9e-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e1f9e-133">RELATED LINKS</span></span>

[<span data-ttu-id="e1f9e-134">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e1f9e-134">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="e1f9e-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e1f9e-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="e1f9e-136">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e1f9e-136">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)


