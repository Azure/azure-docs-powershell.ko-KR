---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
ms.openlocfilehash: 242161a7a02cf3767ecd87dfc6e91a7ffba97eb3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322986"
---
# <span data-ttu-id="990e9-101">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="990e9-101">New-AzHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="990e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="990e9-102">SYNOPSIS</span></span>
<span data-ttu-id="990e9-103">Hive 작업 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="990e9-103">Creates a Hive job object.</span></span>

## <span data-ttu-id="990e9-104">구문</span><span class="sxs-lookup"><span data-stu-id="990e9-104">SYNTAX</span></span>

```
New-AzHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="990e9-105">설명</span><span class="sxs-lookup"><span data-stu-id="990e9-105">DESCRIPTION</span></span>
<span data-ttu-id="990e9-106">**New-AzHDInsightHiveJobDefinition** cmdlet은 Azure HDInsight 클러스터와 함께 사용할 Hive 작업 개체를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="990e9-106">The **New-AzHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="990e9-107">예제</span><span class="sxs-lookup"><span data-stu-id="990e9-107">EXAMPLES</span></span>

### <span data-ttu-id="990e9-108">예제 1: Hive 작업 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="990e9-108">Example 1: Create a Hive job definition</span></span>
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

<span data-ttu-id="990e9-109">이 명령은 Hive 작업 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="990e9-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="990e9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="990e9-110">PARAMETERS</span></span>

### <span data-ttu-id="990e9-111">-Arguments</span><span class="sxs-lookup"><span data-stu-id="990e9-111">-Arguments</span></span>
<span data-ttu-id="990e9-112">작업의 인수 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="990e9-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="990e9-113">인수는 각 태스크에 명령줄 인수로 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="990e9-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="990e9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="990e9-114">-DefaultProfile</span></span>
<span data-ttu-id="990e9-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="990e9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="990e9-116">-Defines</span><span class="sxs-lookup"><span data-stu-id="990e9-116">-Defines</span></span>
<span data-ttu-id="990e9-117">작업이 실행되는 경우 설정할 Hadoop 구성 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="990e9-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="990e9-118">-File</span><span class="sxs-lookup"><span data-stu-id="990e9-118">-File</span></span>
<span data-ttu-id="990e9-119">실행할 쿼리가 포함된 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="990e9-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="990e9-120">이 파일은 클러스터와 연결된 저장소 계정에서 사용할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="990e9-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="990e9-121">쿼리 매개 변수 대신 이 매개 변수를 사용할 *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="990e9-121">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="990e9-122">-Files</span><span class="sxs-lookup"><span data-stu-id="990e9-122">-Files</span></span>
<span data-ttu-id="990e9-123">Hive 작업과 연결된 파일 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="990e9-123">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="990e9-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="990e9-124">-JobName</span></span>
<span data-ttu-id="990e9-125">작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="990e9-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="990e9-126">-Query</span><span class="sxs-lookup"><span data-stu-id="990e9-126">-Query</span></span>
<span data-ttu-id="990e9-127">Hive 쿼리를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="990e9-127">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="990e9-128">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="990e9-128">-RunAsFileJob</span></span>
<span data-ttu-id="990e9-129">이 cmdlet이 쿼리를 저장할 기본 Azure 저장소 계정에 파일을 만들었다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="990e9-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="990e9-130">이 cmdlet은 이 파일을 실행할 스크립트로 참조하는 작업을 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="990e9-130">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="990e9-131">이 기능을 사용하여 백분율 기호(%)와 같은 특수 문자를 처리할 수 있습니다. Templeton은 백분율 기호가 있는 쿼리를 URL 매개 변수로 해석하기 때문에 Templeton을 통한 작업 제출에 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="990e9-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="990e9-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="990e9-132">-StatusFolder</span></span>
<span data-ttu-id="990e9-133">작업의 표준 출력 및 오류 출력이 포함된 폴더의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="990e9-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="990e9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="990e9-134">CommonParameters</span></span>
<span data-ttu-id="990e9-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="990e9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="990e9-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="990e9-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="990e9-137">입력</span><span class="sxs-lookup"><span data-stu-id="990e9-137">INPUTS</span></span>

### <span data-ttu-id="990e9-138">없음</span><span class="sxs-lookup"><span data-stu-id="990e9-138">None</span></span>

## <span data-ttu-id="990e9-139">출력</span><span class="sxs-lookup"><span data-stu-id="990e9-139">OUTPUTS</span></span>

### <span data-ttu-id="990e9-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="990e9-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="990e9-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="990e9-141">NOTES</span></span>

## <span data-ttu-id="990e9-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="990e9-142">RELATED LINKS</span></span>

[<span data-ttu-id="990e9-143">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="990e9-143">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


