---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/invoke-azhdinsighthivejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
ms.openlocfilehash: 737ccdbd742b3c4cc12518262423e846678cf599
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492945"
---
# <span data-ttu-id="7cd8e-101">Invoke-AzHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="7cd8e-101">Invoke-AzHDInsightHiveJob</span></span>

## <span data-ttu-id="7cd8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cd8e-102">SYNOPSIS</span></span>
<span data-ttu-id="7cd8e-103">HDInsight 클러스터에 Hive 쿼리를 제출하고 쿼리 결과를 한 번의 작업으로 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd8e-103">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

## <span data-ttu-id="7cd8e-104">구문</span><span class="sxs-lookup"><span data-stu-id="7cd8e-104">SYNTAX</span></span>

```
Invoke-AzHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cd8e-105">설명</span><span class="sxs-lookup"><span data-stu-id="7cd8e-105">DESCRIPTION</span></span>
<span data-ttu-id="7cd8e-106">**Invoke-AzHDInsightHiveJob** cmdlet은 Azure HDInsight 클러스터에 Hive 쿼리를 제출하고 쿼리 결과를 한 번의 작업으로 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd8e-106">The **Invoke-AzHDInsightHiveJob** cmdlet submits a Hive query to an Azure HDInsight cluster and retrieves query results in one operation.</span></span>
<span data-ttu-id="7cd8e-107">**Invoke-AzHDInsightHiveJob을** 호출하기 전에 Use-AzHDInsightCluster cmdlet을 사용하여 쿼리에 사용할 클러스터를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd8e-107">Use the Use-AzHDInsightCluster cmdlet before calling **Invoke-AzHDInsightHiveJob** to specify which cluster will be used for the query.</span></span>

## <span data-ttu-id="7cd8e-108">예제</span><span class="sxs-lookup"><span data-stu-id="7cd8e-108">EXAMPLES</span></span>

### <span data-ttu-id="7cd8e-109">예제 1: Azure HDInsight 클러스터에 Hive 쿼리 제출</span><span class="sxs-lookup"><span data-stu-id="7cd8e-109">Example 1: Submit a Hive query to an Azure HDInsight cluster</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> Use-AzHDInsightCluster `
            -ClusterCredential $clusterCreds `
            -ClusterName $clusterName

PS C:\> Invoke-AzHDInsightHiveJob -StatusFolder $statusFolder `
            -Query $query `
            -DefaultContainer $storageContainer `
            -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
            -DefaultStorageAccountKey $storageAccountKey
```

<span data-ttu-id="7cd8e-110">이 명령은 show TABLES 쿼리를 your-hadoop-001이라는 클러스터에 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd8e-110">This command submits the query SHOW TABLES to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="7cd8e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7cd8e-111">PARAMETERS</span></span>

### <span data-ttu-id="7cd8e-112">-Arguments</span><span class="sxs-lookup"><span data-stu-id="7cd8e-112">-Arguments</span></span>
<span data-ttu-id="7cd8e-113">작업의 인수 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd8e-113">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="7cd8e-114">인수는 각 태스크에 명령줄 인수로 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="7cd8e-114">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd8e-115">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="7cd8e-115">-DefaultContainer</span></span>
<span data-ttu-id="7cd8e-116">HDInsight 클러스터에서 사용하는 기본 Azure Storage 계정의 기본 컨테이너 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd8e-116">Specifies the name of the default container in the default Azure Storage account that an HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="7cd8e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cd8e-117">-DefaultProfile</span></span>
<span data-ttu-id="7cd8e-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7cd8e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7cd8e-119">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7cd8e-119">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="7cd8e-120">HDInsight 클러스터에서 사용하는 기본 저장소 계정에 대한 계정 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd8e-120">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="7cd8e-121">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7cd8e-121">-DefaultStorageAccountName</span></span>
<span data-ttu-id="7cd8e-122">HDInsight 클러스터에서 사용하는 기본 저장소 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd8e-122">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="7cd8e-123">-Defines</span><span class="sxs-lookup"><span data-stu-id="7cd8e-123">-Defines</span></span>
<span data-ttu-id="7cd8e-124">작업이 실행되는 경우 설정할 Hadoop 구성 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd8e-124">Specifies Hadoop configuration values to set when a job runs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd8e-125">-File</span><span class="sxs-lookup"><span data-stu-id="7cd8e-125">-File</span></span>
<span data-ttu-id="7cd8e-126">실행할 쿼리가 포함된 Azure Storage의 파일에 대한 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd8e-126">Specifies the path to a file in Azure Storage that contains the query to run.</span></span>
<span data-ttu-id="7cd8e-127">쿼리 매개 변수 대신 이 매개 변수를 사용할 *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7cd8e-127">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="7cd8e-128">-Files</span><span class="sxs-lookup"><span data-stu-id="7cd8e-128">-Files</span></span>
<span data-ttu-id="7cd8e-129">Hive 작업에서 필요한 파일 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd8e-129">Specifies a collection of files that are required for a Hive job.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd8e-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="7cd8e-130">-JobName</span></span>
<span data-ttu-id="7cd8e-131">Hive 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd8e-131">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="7cd8e-132">이 매개 변수를 지정하지 않으면 이 cmdlet은 기본값인 "Hive: \<first 100 characters of Query\> "를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd8e-132">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

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

### <span data-ttu-id="7cd8e-133">-Query</span><span class="sxs-lookup"><span data-stu-id="7cd8e-133">-Query</span></span>
<span data-ttu-id="7cd8e-134">Hive 쿼리를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd8e-134">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="7cd8e-135">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="7cd8e-135">-RunAsFileJob</span></span>
<span data-ttu-id="7cd8e-136">이 cmdlet이 쿼리를 저장할 기본 Azure 저장소 계정에 파일을 만들었다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7cd8e-136">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="7cd8e-137">이 cmdlet은 이 파일을 실행할 스크립트로 참조하는 작업을 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd8e-137">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="7cd8e-138">이 기능을 사용하여 백분율 기호(%)와 같은 특수 문자를 처리할 수 있습니다. Templeton은 백분율 기호가 있는 쿼리를 URL 매개 변수로 해석하기 때문에 Templeton을 통한 작업 제출에 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd8e-138">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd8e-139">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="7cd8e-139">-StatusFolder</span></span>
<span data-ttu-id="7cd8e-140">작업의 표준 출력 및 오류 출력이 포함된 폴더의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd8e-140">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="7cd8e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cd8e-141">CommonParameters</span></span>
<span data-ttu-id="7cd8e-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd8e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cd8e-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7cd8e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cd8e-144">입력</span><span class="sxs-lookup"><span data-stu-id="7cd8e-144">INPUTS</span></span>

### <span data-ttu-id="7cd8e-145">없음</span><span class="sxs-lookup"><span data-stu-id="7cd8e-145">None</span></span>

## <span data-ttu-id="7cd8e-146">출력</span><span class="sxs-lookup"><span data-stu-id="7cd8e-146">OUTPUTS</span></span>

### <span data-ttu-id="7cd8e-147">System.String</span><span class="sxs-lookup"><span data-stu-id="7cd8e-147">System.String</span></span>

## <span data-ttu-id="7cd8e-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7cd8e-148">NOTES</span></span>

## <span data-ttu-id="7cd8e-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7cd8e-149">RELATED LINKS</span></span>

[<span data-ttu-id="7cd8e-150">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="7cd8e-150">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


