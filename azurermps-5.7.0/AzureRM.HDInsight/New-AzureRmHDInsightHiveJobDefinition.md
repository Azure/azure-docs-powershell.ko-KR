---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightHiveJobDefinition.md
ms.openlocfilehash: 3e4748a8bc5e5c04868fb7c2d4179c07ea63c905
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528132"
---
# <span data-ttu-id="2b263-101">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="2b263-101">New-AzureRmHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="2b263-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b263-102">SYNOPSIS</span></span>
<span data-ttu-id="2b263-103">하이브 작업 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2b263-103">Creates a Hive job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b263-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2b263-104">SYNTAX</span></span>

```
New-AzureRmHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b263-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2b263-105">DESCRIPTION</span></span>
<span data-ttu-id="2b263-106">**AzureRmHDInsightHiveJobDefinition** Cmdlet은 Azure HDInsight 클러스터와 함께 사용 하기 위한 하이브 작업 개체를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b263-106">The **New-AzureRmHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="2b263-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2b263-107">EXAMPLES</span></span>

### <span data-ttu-id="2b263-108">예제 1: 하이브 작업 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="2b263-108">Example 1: Create a Hive job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Hive job details
PS C:\>$statusFolder = "<status folder>"        
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="2b263-109">이 명령은 하이브 작업 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2b263-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="2b263-110">변수</span><span class="sxs-lookup"><span data-stu-id="2b263-110">PARAMETERS</span></span>

### <span data-ttu-id="2b263-111">-인수</span><span class="sxs-lookup"><span data-stu-id="2b263-111">-Arguments</span></span>
<span data-ttu-id="2b263-112">작업에 대 한 인수 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b263-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="2b263-113">인수는 각 작업에 명령줄 인수로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b263-113">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b263-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b263-114">-DefaultProfile</span></span>
<span data-ttu-id="2b263-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2b263-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b263-116">-정의</span><span class="sxs-lookup"><span data-stu-id="2b263-116">-Defines</span></span>
<span data-ttu-id="2b263-117">작업이 실행 될 때 설정할 Hadoop 구성 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b263-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b263-118">-파일</span><span class="sxs-lookup"><span data-stu-id="2b263-118">-File</span></span>
<span data-ttu-id="2b263-119">실행할 쿼리를 포함 하는 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b263-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="2b263-120">이 파일은 클러스터와 연결 된 저장소 계정에서 사용할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b263-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="2b263-121">*쿼리* 매개 변수 대신이 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b263-121">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="2b263-122">-파일</span><span class="sxs-lookup"><span data-stu-id="2b263-122">-Files</span></span>
<span data-ttu-id="2b263-123">Hive 작업과 연결 된 파일의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b263-123">Specifies a collection of files that are associated with a Hive job.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b263-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="2b263-124">-JobName</span></span>
<span data-ttu-id="2b263-125">작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b263-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="2b263-126">-쿼리</span><span class="sxs-lookup"><span data-stu-id="2b263-126">-Query</span></span>
<span data-ttu-id="2b263-127">하이브 쿼리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b263-127">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="2b263-128">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="2b263-128">-RunAsFileJob</span></span>
<span data-ttu-id="2b263-129">이 cmdlet이 쿼리를 저장할 기본 Azure 저장소 계정에 파일을 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2b263-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="2b263-130">이 cmdlet은이 파일을 참조 하는 작업을 실행 하도록 스크립트로 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b263-130">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="2b263-131">이 기능을 사용 하 여 백분율 기호 (%) 등의 특수 문자를 처리할 수 있습니다. Templeton는 URL 매개 변수로 백분율 기호가 있는 쿼리를 해석 하기 때문에 Templeton를 통한 작업 제출에 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b263-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b263-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="2b263-132">-StatusFolder</span></span>
<span data-ttu-id="2b263-133">작업에 대 한 표준 출력 및 오류 출력을 포함 하는 폴더의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b263-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="2b263-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b263-134">CommonParameters</span></span>
<span data-ttu-id="2b263-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b263-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b263-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b263-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b263-137">입력</span><span class="sxs-lookup"><span data-stu-id="2b263-137">INPUTS</span></span>

### <span data-ttu-id="2b263-138">않아야</span><span class="sxs-lookup"><span data-stu-id="2b263-138">None</span></span>
<span data-ttu-id="2b263-139">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2b263-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2b263-140">출력</span><span class="sxs-lookup"><span data-stu-id="2b263-140">OUTPUTS</span></span>

### <span data-ttu-id="2b263-141">AzureHDInsightHiveJobDefinition의. m m.</span><span class="sxs-lookup"><span data-stu-id="2b263-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="2b263-142">상속자</span><span class="sxs-lookup"><span data-stu-id="2b263-142">NOTES</span></span>

## <span data-ttu-id="2b263-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b263-143">RELATED LINKS</span></span>

[<span data-ttu-id="2b263-144">시작-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2b263-144">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


