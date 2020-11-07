---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
ms.openlocfilehash: 6e19594cfcd79c6be82373af6245ea2154296b48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711894"
---
# <span data-ttu-id="8ae91-101">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8ae91-101">Wait-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="8ae91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ae91-102">SYNOPSIS</span></span>
<span data-ttu-id="8ae91-103">지정 된 작업의 완료 또는 실패를 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="8ae91-103">Waits for the completion or failure of a specified job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ae91-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8ae91-104">SYNTAX</span></span>

```
Wait-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ae91-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8ae91-105">DESCRIPTION</span></span>
<span data-ttu-id="8ae91-106">**AzureRmHDInsightJob** Cmdlet은 Azure HDInsight 작업의 완료 또는 실패를 세계가 귀하 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ae91-106">The **Wait-AzureRmHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="8ae91-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8ae91-107">EXAMPLES</span></span>

### <span data-ttu-id="8ae91-108">예제 1: 작업 완료 또는 실패를 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="8ae91-108">Example 1: Wait for the completion or failure of a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Wait-AzureRmHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="8ae91-109">이 명령은 작업의 완료 또는 실패를 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="8ae91-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="8ae91-110">변수</span><span class="sxs-lookup"><span data-stu-id="8ae91-110">PARAMETERS</span></span>

### <span data-ttu-id="8ae91-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8ae91-111">-ClusterName</span></span>
<span data-ttu-id="8ae91-112">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ae91-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="8ae91-113">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="8ae91-113">-HttpCredential</span></span>
<span data-ttu-id="8ae91-114">클러스터에 대 한 HTTP (클러스터 로그인) 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ae91-114">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="8ae91-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="8ae91-115">-JobId</span></span>
<span data-ttu-id="8ae91-116">작업의 작업 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ae91-116">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="8ae91-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ae91-117">-ResourceGroupName</span></span>
<span data-ttu-id="8ae91-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ae91-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8ae91-119">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="8ae91-119">-TimeoutInSeconds</span></span>
<span data-ttu-id="8ae91-120">작업 완료를 기다리는 총 시간 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="8ae91-120">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="8ae91-121">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="8ae91-121">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="8ae91-122">작업 상태 검사 사이에 대기 하는 시간 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="8ae91-122">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="8ae91-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ae91-123">-DefaultProfile</span></span>
<span data-ttu-id="8ae91-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8ae91-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ae91-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ae91-125">CommonParameters</span></span>
<span data-ttu-id="8ae91-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ae91-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ae91-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ae91-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ae91-128">입력</span><span class="sxs-lookup"><span data-stu-id="8ae91-128">INPUTS</span></span>

### <span data-ttu-id="8ae91-129">이름</span><span class="sxs-lookup"><span data-stu-id="8ae91-129">String</span></span>
<span data-ttu-id="8ae91-130">' JobId ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ae91-130">Parameter 'JobId' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="8ae91-131">출력</span><span class="sxs-lookup"><span data-stu-id="8ae91-131">OUTPUTS</span></span>

### <span data-ttu-id="8ae91-132">AzureHDInsightJob의. m m.</span><span class="sxs-lookup"><span data-stu-id="8ae91-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="8ae91-133">상속자</span><span class="sxs-lookup"><span data-stu-id="8ae91-133">NOTES</span></span>

## <span data-ttu-id="8ae91-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ae91-134">RELATED LINKS</span></span>

[<span data-ttu-id="8ae91-135">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8ae91-135">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="8ae91-136">시작-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8ae91-136">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="8ae91-137">중지-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8ae91-137">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)


