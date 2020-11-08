---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/wait-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
ms.openlocfilehash: 6b87b7f6e3482aad974c5f7d334724f5d2f99e7c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217824"
---
# <span data-ttu-id="efead-101">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="efead-101">Wait-AzHDInsightJob</span></span>

## <span data-ttu-id="efead-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efead-102">SYNOPSIS</span></span>
<span data-ttu-id="efead-103">지정 된 작업의 완료 또는 실패를 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="efead-103">Waits for the completion or failure of a specified job.</span></span>

## <span data-ttu-id="efead-104">구문과</span><span class="sxs-lookup"><span data-stu-id="efead-104">SYNTAX</span></span>

```
Wait-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efead-105">설명은</span><span class="sxs-lookup"><span data-stu-id="efead-105">DESCRIPTION</span></span>
<span data-ttu-id="efead-106">**AzHDInsightJob** Cmdlet은 Azure HDInsight 작업의 완료 또는 실패를 세계가 귀하 합니다.</span><span class="sxs-lookup"><span data-stu-id="efead-106">The **Wait-AzHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="efead-107">예제의</span><span class="sxs-lookup"><span data-stu-id="efead-107">EXAMPLES</span></span>

### <span data-ttu-id="efead-108">예제 1: 작업 완료 또는 실패를 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="efead-108">Example 1: Wait for the completion or failure of a job</span></span>
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

<span data-ttu-id="efead-109">이 명령은 작업의 완료 또는 실패를 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="efead-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="efead-110">변수</span><span class="sxs-lookup"><span data-stu-id="efead-110">PARAMETERS</span></span>

### <span data-ttu-id="efead-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="efead-111">-ClusterName</span></span>
<span data-ttu-id="efead-112">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="efead-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="efead-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efead-113">-DefaultProfile</span></span>
<span data-ttu-id="efead-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="efead-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="efead-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="efead-115">-HttpCredential</span></span>
<span data-ttu-id="efead-116">클러스터에 대 한 HTTP (클러스터 로그인) 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="efead-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="efead-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="efead-117">-JobId</span></span>
<span data-ttu-id="efead-118">작업의 작업 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="efead-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="efead-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efead-119">-ResourceGroupName</span></span>
<span data-ttu-id="efead-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="efead-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="efead-121">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="efead-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="efead-122">작업 완료를 기다리는 총 시간 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="efead-122">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="efead-123">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="efead-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="efead-124">작업 상태 검사 사이에 대기 하는 시간 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="efead-124">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="efead-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efead-125">CommonParameters</span></span>
<span data-ttu-id="efead-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="efead-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efead-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efead-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efead-128">입력</span><span class="sxs-lookup"><span data-stu-id="efead-128">INPUTS</span></span>

### <span data-ttu-id="efead-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="efead-129">System.String</span></span>

## <span data-ttu-id="efead-130">출력</span><span class="sxs-lookup"><span data-stu-id="efead-130">OUTPUTS</span></span>

### <span data-ttu-id="efead-131">AzureHDInsightJob의. m m.</span><span class="sxs-lookup"><span data-stu-id="efead-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="efead-132">상속자</span><span class="sxs-lookup"><span data-stu-id="efead-132">NOTES</span></span>

## <span data-ttu-id="efead-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="efead-133">RELATED LINKS</span></span>

[<span data-ttu-id="efead-134">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="efead-134">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="efead-135">시작-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="efead-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="efead-136">중지-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="efead-136">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)


