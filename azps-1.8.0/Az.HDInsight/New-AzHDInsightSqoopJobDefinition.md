---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
ms.openlocfilehash: d5841a7c612bccb760a8d755fc9a1c1364cc52a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868246"
---
# <span data-ttu-id="b4493-101">New-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b4493-101">New-AzHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="b4493-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4493-102">SYNOPSIS</span></span>
<span data-ttu-id="b4493-103">Sqoop 작업 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b4493-103">Creates a Sqoop job object.</span></span>

## <span data-ttu-id="b4493-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b4493-104">SYNTAX</span></span>

```
New-AzHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4493-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b4493-105">DESCRIPTION</span></span>
<span data-ttu-id="b4493-106">**AzHDInsightSqoopJobDefinition** Cmdlet은 Azure HDInsight 클러스터와 함께 사용할 sqoop 작업 개체를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4493-106">The **New-AzHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b4493-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b4493-107">EXAMPLES</span></span>

### <span data-ttu-id="b4493-108">예제 1: Sqoop 작업 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="b4493-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="b4493-109">이 명령은 Sqoop 작업 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b4493-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="b4493-110">변수</span><span class="sxs-lookup"><span data-stu-id="b4493-110">PARAMETERS</span></span>

### <span data-ttu-id="b4493-111">-명령</span><span class="sxs-lookup"><span data-stu-id="b4493-111">-Command</span></span>
<span data-ttu-id="b4493-112">Sqoop 명령을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4493-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="b4493-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4493-113">-DefaultProfile</span></span>
<span data-ttu-id="b4493-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b4493-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4493-115">-파일</span><span class="sxs-lookup"><span data-stu-id="b4493-115">-File</span></span>
<span data-ttu-id="b4493-116">실행할 쿼리를 포함 하는 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4493-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="b4493-117">이 파일은 클러스터와 연결 된 저장소 계정에서 사용할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4493-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="b4493-118">*쿼리* 매개 변수 대신이 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4493-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="b4493-119">-파일</span><span class="sxs-lookup"><span data-stu-id="b4493-119">-Files</span></span>
<span data-ttu-id="b4493-120">Hive 작업과 연결 된 파일의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4493-120">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="b4493-121">-기능 디렉터리</span><span class="sxs-lookup"><span data-stu-id="b4493-121">-LibDir</span></span>
<span data-ttu-id="b4493-122">Sqoop 작업의 라이브러리 디렉터리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4493-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="b4493-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="b4493-123">-StatusFolder</span></span>
<span data-ttu-id="b4493-124">작업에 대 한 표준 출력 및 오류 출력을 포함 하는 폴더의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4493-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="b4493-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4493-125">CommonParameters</span></span>
<span data-ttu-id="b4493-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4493-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4493-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4493-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4493-128">입력</span><span class="sxs-lookup"><span data-stu-id="b4493-128">INPUTS</span></span>

### <span data-ttu-id="b4493-129">않아야</span><span class="sxs-lookup"><span data-stu-id="b4493-129">None</span></span>

## <span data-ttu-id="b4493-130">출력</span><span class="sxs-lookup"><span data-stu-id="b4493-130">OUTPUTS</span></span>

### <span data-ttu-id="b4493-131">AzureHDInsightSqoopJobDefinition의. m m.</span><span class="sxs-lookup"><span data-stu-id="b4493-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="b4493-132">상속자</span><span class="sxs-lookup"><span data-stu-id="b4493-132">NOTES</span></span>

## <span data-ttu-id="b4493-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4493-133">RELATED LINKS</span></span>

[<span data-ttu-id="b4493-134">시작-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b4493-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


