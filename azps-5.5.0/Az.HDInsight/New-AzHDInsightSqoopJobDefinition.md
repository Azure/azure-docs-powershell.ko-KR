---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 69bb20b8a6610d2701a6c2256317b081dc11ad3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200220"
---
# <span data-ttu-id="1e588-101">New-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="1e588-101">New-AzHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="1e588-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e588-102">SYNOPSIS</span></span>
<span data-ttu-id="1e588-103">Sqoop 작업 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1e588-103">Creates a Sqoop job object.</span></span>

## <span data-ttu-id="1e588-104">구문</span><span class="sxs-lookup"><span data-stu-id="1e588-104">SYNTAX</span></span>

```
New-AzHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e588-105">설명</span><span class="sxs-lookup"><span data-stu-id="1e588-105">DESCRIPTION</span></span>
<span data-ttu-id="1e588-106">**New-AzHDInsightSqoopJobDefinition** cmdlet은 Azure HDInsight 클러스터와 함께 사용할 Sqoop 작업 개체를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="1e588-106">The **New-AzHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="1e588-107">예제</span><span class="sxs-lookup"><span data-stu-id="1e588-107">EXAMPLES</span></span>

### <span data-ttu-id="1e588-108">예제 1: Sqoop 작업 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="1e588-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="1e588-109">이 명령은 Sqoop 작업 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1e588-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="1e588-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e588-110">PARAMETERS</span></span>

### <span data-ttu-id="1e588-111">-Command</span><span class="sxs-lookup"><span data-stu-id="1e588-111">-Command</span></span>
<span data-ttu-id="1e588-112">Sqoop 명령을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1e588-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="1e588-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e588-113">-DefaultProfile</span></span>
<span data-ttu-id="1e588-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1e588-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e588-115">-File</span><span class="sxs-lookup"><span data-stu-id="1e588-115">-File</span></span>
<span data-ttu-id="1e588-116">실행할 쿼리가 포함된 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1e588-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="1e588-117">클러스터와 연결된 Storage 계정에서 파일을 사용할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e588-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="1e588-118">쿼리 매개 변수 대신 이 매개 변수를 사용할 *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e588-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="1e588-119">-Files</span><span class="sxs-lookup"><span data-stu-id="1e588-119">-Files</span></span>
<span data-ttu-id="1e588-120">Hive 작업과 연결된 파일 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1e588-120">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="1e588-121">-LibDir</span><span class="sxs-lookup"><span data-stu-id="1e588-121">-LibDir</span></span>
<span data-ttu-id="1e588-122">Sqoop 작업의 라이브러리 디렉터리를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1e588-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="1e588-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="1e588-123">-StatusFolder</span></span>
<span data-ttu-id="1e588-124">작업의 표준 출력 및 오류 출력이 포함된 폴더의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1e588-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="1e588-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e588-125">CommonParameters</span></span>
<span data-ttu-id="1e588-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1e588-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e588-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1e588-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e588-128">입력</span><span class="sxs-lookup"><span data-stu-id="1e588-128">INPUTS</span></span>

### <span data-ttu-id="1e588-129">없음</span><span class="sxs-lookup"><span data-stu-id="1e588-129">None</span></span>

## <span data-ttu-id="1e588-130">출력</span><span class="sxs-lookup"><span data-stu-id="1e588-130">OUTPUTS</span></span>

### <span data-ttu-id="1e588-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="1e588-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="1e588-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1e588-132">NOTES</span></span>

## <span data-ttu-id="1e588-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e588-133">RELATED LINKS</span></span>

[<span data-ttu-id="1e588-134">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="1e588-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


