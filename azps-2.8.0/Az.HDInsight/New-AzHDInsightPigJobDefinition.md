---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightpigjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
ms.openlocfilehash: 3f40857c0388983a12217477db96cbbdbb94e815
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689808"
---
# <span data-ttu-id="57ba3-101">New-AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="57ba3-101">New-AzHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="57ba3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57ba3-102">SYNOPSIS</span></span>
<span data-ttu-id="57ba3-103">문 돼지 job 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="57ba3-103">Creates a Pig job object.</span></span>

## <span data-ttu-id="57ba3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="57ba3-104">SYNTAX</span></span>

```
New-AzHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57ba3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="57ba3-105">DESCRIPTION</span></span>
<span data-ttu-id="57ba3-106">**AzHDInsightPigJobDefinition** Cmdlet은 Azure HDInsight 클러스터와 함께 사용할 문 돼지 job 개체를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="57ba3-106">The **New-AzHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="57ba3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="57ba3-107">EXAMPLES</span></span>

### <span data-ttu-id="57ba3-108">예제 1: 문 돼지 작업 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="57ba3-108">Example 1: Create a Pig job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Pig job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightPigJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="57ba3-109">이 명령은 문 돼지 작업 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="57ba3-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="57ba3-110">변수</span><span class="sxs-lookup"><span data-stu-id="57ba3-110">PARAMETERS</span></span>

### <span data-ttu-id="57ba3-111">-인수</span><span class="sxs-lookup"><span data-stu-id="57ba3-111">-Arguments</span></span>
<span data-ttu-id="57ba3-112">작업에 대 한 인수 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57ba3-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="57ba3-113">인수는 각 작업에 명령줄 인수로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="57ba3-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="57ba3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57ba3-114">-DefaultProfile</span></span>
<span data-ttu-id="57ba3-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="57ba3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57ba3-116">-파일</span><span class="sxs-lookup"><span data-stu-id="57ba3-116">-File</span></span>
<span data-ttu-id="57ba3-117">실행할 쿼리를 포함 하는 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57ba3-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="57ba3-118">이 파일은 클러스터와 연결 된 저장소 계정에서 사용할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="57ba3-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="57ba3-119">*쿼리* 매개 변수 대신이 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57ba3-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="57ba3-120">-파일</span><span class="sxs-lookup"><span data-stu-id="57ba3-120">-Files</span></span>
<span data-ttu-id="57ba3-121">Hive 작업과 연결 된 파일의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57ba3-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="57ba3-122">-쿼리</span><span class="sxs-lookup"><span data-stu-id="57ba3-122">-Query</span></span>
<span data-ttu-id="57ba3-123">문 돼지 쿼리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57ba3-123">Specifies the Pig query.</span></span>

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

### <span data-ttu-id="57ba3-124">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="57ba3-124">-StatusFolder</span></span>
<span data-ttu-id="57ba3-125">작업에 대 한 표준 출력 및 오류 출력을 포함 하는 폴더의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57ba3-125">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="57ba3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57ba3-126">CommonParameters</span></span>
<span data-ttu-id="57ba3-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57ba3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57ba3-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57ba3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57ba3-129">입력</span><span class="sxs-lookup"><span data-stu-id="57ba3-129">INPUTS</span></span>

### <span data-ttu-id="57ba3-130">않아야</span><span class="sxs-lookup"><span data-stu-id="57ba3-130">None</span></span>

## <span data-ttu-id="57ba3-131">출력</span><span class="sxs-lookup"><span data-stu-id="57ba3-131">OUTPUTS</span></span>

### <span data-ttu-id="57ba3-132">AzureHDInsightPigJobDefinition의. m m.</span><span class="sxs-lookup"><span data-stu-id="57ba3-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="57ba3-133">상속자</span><span class="sxs-lookup"><span data-stu-id="57ba3-133">NOTES</span></span>

## <span data-ttu-id="57ba3-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57ba3-134">RELATED LINKS</span></span>

[<span data-ttu-id="57ba3-135">시작-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="57ba3-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


