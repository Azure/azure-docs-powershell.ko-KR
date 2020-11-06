---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Invoke-AzureRmHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Invoke-AzureRmHDInsightHiveJob.md
ms.openlocfilehash: 127e949bfaa9d54644f7f690cfefbf095d477374
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537216"
---
# <span data-ttu-id="8c08c-101">Invoke-AzureRmHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="8c08c-101">Invoke-AzureRmHDInsightHiveJob</span></span>

## <span data-ttu-id="8c08c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c08c-102">SYNOPSIS</span></span>
<span data-ttu-id="8c08c-103">HDInsight 클러스터에 하이브 쿼리를 제출 하 고 한 번의 작업으로 쿼리 결과를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c08c-103">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c08c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8c08c-104">SYNTAX</span></span>

```
Invoke-AzureRmHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c08c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8c08c-105">DESCRIPTION</span></span>
<span data-ttu-id="8c08c-106">**AzureRmHDInsightHiveJob** Cmdlet은 하이브 쿼리를 Azure HDInsight 클러스터에 제출 하 고 한 번의 작업으로 쿼리 결과를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c08c-106">The **Invoke-AzureRmHDInsightHiveJob** cmdlet submits a Hive query to an Azure HDInsight cluster and retrieves query results in one operation.</span></span>
<span data-ttu-id="8c08c-107">**AzureRmHDInsightHiveJob** 를 호출 하기 전에 Use-AzureRmHDInsightCluster cmdlet을 사용 하 여 쿼리에 사용할 클러스터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c08c-107">Use the Use-AzureRmHDInsightCluster cmdlet before calling **Invoke-AzureRmHDInsightHiveJob** to specify which cluster will be used for the query.</span></span>

## <span data-ttu-id="8c08c-108">예제의</span><span class="sxs-lookup"><span data-stu-id="8c08c-108">EXAMPLES</span></span>

### <span data-ttu-id="8c08c-109">예제 1: 하이브 쿼리를 Azure HDInsight 클러스터에 제출</span><span class="sxs-lookup"><span data-stu-id="8c08c-109">Example 1: Submit a Hive query to an Azure HDInsight cluster</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> Use-AzureRmHDInsightCluster `
            -ClusterCredential $clusterCreds `
            -ClusterName $clusterName

PS C:\> Invoke-AzureRmHDInsightHiveJob -StatusFolder $statusFolder `
            -Query $query `
            -DefaultContainer $storageAccountContainer `
            -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
            -DefaultStorageAccountKey $storageAccountKey
```

<span data-ttu-id="8c08c-110">이 명령은-hadoop-001 이라는 클러스터에 대 한 쿼리 표시 테이블을 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c08c-110">This command submits the query SHOW TABLES to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="8c08c-111">변수</span><span class="sxs-lookup"><span data-stu-id="8c08c-111">PARAMETERS</span></span>

### <span data-ttu-id="8c08c-112">-인수</span><span class="sxs-lookup"><span data-stu-id="8c08c-112">-Arguments</span></span>
<span data-ttu-id="8c08c-113">작업에 대 한 인수 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c08c-113">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="8c08c-114">인수는 각 작업에 명령줄 인수로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8c08c-114">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="8c08c-115">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="8c08c-115">-DefaultContainer</span></span>
<span data-ttu-id="8c08c-116">HDInsight 클러스터에서 사용 하는 기본 Azure 저장소 계정에서 기본 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c08c-116">Specifies the name of the default container in the default Azure Storage account that an HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="8c08c-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="8c08c-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="8c08c-118">HDInsight 클러스터에서 사용 하는 기본 저장소 계정에 대 한 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c08c-118">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="8c08c-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8c08c-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="8c08c-120">HDInsight 클러스터에서 사용 하는 기본 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c08c-120">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="8c08c-121">-정의</span><span class="sxs-lookup"><span data-stu-id="8c08c-121">-Defines</span></span>
<span data-ttu-id="8c08c-122">작업을 실행할 때 설정할 Hadoop 구성 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c08c-122">Specifies Hadoop configuration values to set when a job runs.</span></span>

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

### <span data-ttu-id="8c08c-123">-파일</span><span class="sxs-lookup"><span data-stu-id="8c08c-123">-File</span></span>
<span data-ttu-id="8c08c-124">실행할 쿼리를 포함 하는 Azure Storage의 파일에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c08c-124">Specifies the path to a file in Azure Storage that contains the query to run.</span></span>
<span data-ttu-id="8c08c-125">*쿼리* 매개 변수 대신이 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c08c-125">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="8c08c-126">-파일</span><span class="sxs-lookup"><span data-stu-id="8c08c-126">-Files</span></span>
<span data-ttu-id="8c08c-127">하이브 작업에 필요한 파일의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c08c-127">Specifies a collection of files that are required for a Hive job.</span></span>

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

### <span data-ttu-id="8c08c-128">-JobName</span><span class="sxs-lookup"><span data-stu-id="8c08c-128">-JobName</span></span>
<span data-ttu-id="8c08c-129">하이브 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c08c-129">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="8c08c-130">이 매개 변수를 지정 하지 않으면이 cmdlet은 기본값 "Hive:"를 사용 합니다. \<first 100 characters of Query\></span><span class="sxs-lookup"><span data-stu-id="8c08c-130">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

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

### <span data-ttu-id="8c08c-131">-쿼리</span><span class="sxs-lookup"><span data-stu-id="8c08c-131">-Query</span></span>
<span data-ttu-id="8c08c-132">하이브 쿼리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c08c-132">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="8c08c-133">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="8c08c-133">-RunAsFileJob</span></span>
<span data-ttu-id="8c08c-134">이 cmdlet이 쿼리를 저장할 기본 Azure 저장소 계정에 파일을 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8c08c-134">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="8c08c-135">이 cmdlet은이 파일을 참조 하는 작업을 실행 하도록 스크립트로 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c08c-135">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="8c08c-136">이 기능을 사용 하 여 백분율 기호 (%) 등의 특수 문자를 처리할 수 있습니다. Templeton는 URL 매개 변수로 백분율 기호가 있는 쿼리를 해석 하기 때문에 Templeton를 통한 작업 제출에 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c08c-136">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="8c08c-137">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="8c08c-137">-StatusFolder</span></span>
<span data-ttu-id="8c08c-138">작업에 대 한 표준 출력 및 오류 출력을 포함 하는 폴더의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c08c-138">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="8c08c-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c08c-139">-DefaultProfile</span></span>
<span data-ttu-id="8c08c-140">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8c08c-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c08c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c08c-141">CommonParameters</span></span>
<span data-ttu-id="8c08c-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c08c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c08c-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c08c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c08c-144">입력</span><span class="sxs-lookup"><span data-stu-id="8c08c-144">INPUTS</span></span>

## <span data-ttu-id="8c08c-145">출력</span><span class="sxs-lookup"><span data-stu-id="8c08c-145">OUTPUTS</span></span>

### <span data-ttu-id="8c08c-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8c08c-146">System.String</span></span>

## <span data-ttu-id="8c08c-147">상속자</span><span class="sxs-lookup"><span data-stu-id="8c08c-147">NOTES</span></span>

## <span data-ttu-id="8c08c-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8c08c-148">RELATED LINKS</span></span>

[<span data-ttu-id="8c08c-149">-AzureRmHDInsightCluster 사용</span><span class="sxs-lookup"><span data-stu-id="8c08c-149">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


