---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
ms.openlocfilehash: 4d8a35498462cae6e218fc41365de89a897bb555
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689810"
---
# <span data-ttu-id="9dfe0-101">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="9dfe0-101">New-AzHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="9dfe0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dfe0-102">SYNOPSIS</span></span>
<span data-ttu-id="9dfe0-103">하이브 작업 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-103">Creates a Hive job object.</span></span>

## <span data-ttu-id="9dfe0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9dfe0-104">SYNTAX</span></span>

```
New-AzHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9dfe0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9dfe0-105">DESCRIPTION</span></span>
<span data-ttu-id="9dfe0-106">**AzHDInsightHiveJobDefinition** Cmdlet은 Azure HDInsight 클러스터와 함께 사용 하기 위한 하이브 작업 개체를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-106">The **New-AzHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="9dfe0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9dfe0-107">EXAMPLES</span></span>

### <span data-ttu-id="9dfe0-108">예제 1: 하이브 작업 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="9dfe0-108">Example 1: Create a Hive job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Hive job details
PS C:\>$statusFolder = "<status folder>"        
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="9dfe0-109">이 명령은 하이브 작업 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="9dfe0-110">변수</span><span class="sxs-lookup"><span data-stu-id="9dfe0-110">PARAMETERS</span></span>

### <span data-ttu-id="9dfe0-111">-인수</span><span class="sxs-lookup"><span data-stu-id="9dfe0-111">-Arguments</span></span>
<span data-ttu-id="9dfe0-112">작업에 대 한 인수 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="9dfe0-113">인수는 각 작업에 명령줄 인수로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="9dfe0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dfe0-114">-DefaultProfile</span></span>
<span data-ttu-id="9dfe0-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9dfe0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9dfe0-116">-정의</span><span class="sxs-lookup"><span data-stu-id="9dfe0-116">-Defines</span></span>
<span data-ttu-id="9dfe0-117">작업이 실행 될 때 설정할 Hadoop 구성 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="9dfe0-118">-파일</span><span class="sxs-lookup"><span data-stu-id="9dfe0-118">-File</span></span>
<span data-ttu-id="9dfe0-119">실행할 쿼리를 포함 하는 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="9dfe0-120">이 파일은 클러스터와 연결 된 저장소 계정에서 사용할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="9dfe0-121">*쿼리* 매개 변수 대신이 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-121">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="9dfe0-122">-파일</span><span class="sxs-lookup"><span data-stu-id="9dfe0-122">-Files</span></span>
<span data-ttu-id="9dfe0-123">Hive 작업과 연결 된 파일의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-123">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="9dfe0-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="9dfe0-124">-JobName</span></span>
<span data-ttu-id="9dfe0-125">작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="9dfe0-126">-쿼리</span><span class="sxs-lookup"><span data-stu-id="9dfe0-126">-Query</span></span>
<span data-ttu-id="9dfe0-127">하이브 쿼리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-127">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="9dfe0-128">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="9dfe0-128">-RunAsFileJob</span></span>
<span data-ttu-id="9dfe0-129">이 cmdlet이 쿼리를 저장할 기본 Azure 저장소 계정에 파일을 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="9dfe0-130">이 cmdlet은이 파일을 참조 하는 작업을 실행 하도록 스크립트로 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-130">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="9dfe0-131">이 기능을 사용 하 여 백분율 기호 (%) 등의 특수 문자를 처리할 수 있습니다. Templeton는 URL 매개 변수로 백분율 기호가 있는 쿼리를 해석 하기 때문에 Templeton를 통한 작업 제출에 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="9dfe0-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="9dfe0-132">-StatusFolder</span></span>
<span data-ttu-id="9dfe0-133">작업에 대 한 표준 출력 및 오류 출력을 포함 하는 폴더의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="9dfe0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dfe0-134">CommonParameters</span></span>
<span data-ttu-id="9dfe0-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dfe0-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dfe0-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dfe0-137">입력</span><span class="sxs-lookup"><span data-stu-id="9dfe0-137">INPUTS</span></span>

### <span data-ttu-id="9dfe0-138">않아야</span><span class="sxs-lookup"><span data-stu-id="9dfe0-138">None</span></span>

## <span data-ttu-id="9dfe0-139">출력</span><span class="sxs-lookup"><span data-stu-id="9dfe0-139">OUTPUTS</span></span>

### <span data-ttu-id="9dfe0-140">AzureHDInsightHiveJobDefinition의. m m.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="9dfe0-141">상속자</span><span class="sxs-lookup"><span data-stu-id="9dfe0-141">NOTES</span></span>

## <span data-ttu-id="9dfe0-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9dfe0-142">RELATED LINKS</span></span>

[<span data-ttu-id="9dfe0-143">시작-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9dfe0-143">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


