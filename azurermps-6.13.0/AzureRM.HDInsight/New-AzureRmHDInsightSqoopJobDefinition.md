---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 709c87084cc871814e4760e0d2641c59b0e5a64e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530296"
---
# <span data-ttu-id="ae616-101">New-AzureRmHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ae616-101">New-AzureRmHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="ae616-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae616-102">SYNOPSIS</span></span>
<span data-ttu-id="ae616-103">Sqoop 작업 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ae616-103">Creates a Sqoop job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae616-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ae616-104">SYNTAX</span></span>

```
New-AzureRmHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae616-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ae616-105">DESCRIPTION</span></span>
<span data-ttu-id="ae616-106">**AzureRmHDInsightSqoopJobDefinition** Cmdlet은 Azure HDInsight 클러스터와 함께 사용할 sqoop 작업 개체를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae616-106">The **New-AzureRmHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="ae616-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ae616-107">EXAMPLES</span></span>

### <span data-ttu-id="ae616-108">예제 1: Sqoop 작업 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="ae616-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="ae616-109">이 명령은 Sqoop 작업 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ae616-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="ae616-110">변수</span><span class="sxs-lookup"><span data-stu-id="ae616-110">PARAMETERS</span></span>

### <span data-ttu-id="ae616-111">-명령</span><span class="sxs-lookup"><span data-stu-id="ae616-111">-Command</span></span>
<span data-ttu-id="ae616-112">Sqoop 명령을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae616-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="ae616-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae616-113">-DefaultProfile</span></span>
<span data-ttu-id="ae616-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ae616-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae616-115">-파일</span><span class="sxs-lookup"><span data-stu-id="ae616-115">-File</span></span>
<span data-ttu-id="ae616-116">실행할 쿼리를 포함 하는 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae616-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="ae616-117">이 파일은 클러스터와 연결 된 저장소 계정에서 사용할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae616-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="ae616-118">*쿼리* 매개 변수 대신이 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae616-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="ae616-119">-파일</span><span class="sxs-lookup"><span data-stu-id="ae616-119">-Files</span></span>
<span data-ttu-id="ae616-120">Hive 작업과 연결 된 파일의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae616-120">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="ae616-121">-기능 디렉터리</span><span class="sxs-lookup"><span data-stu-id="ae616-121">-LibDir</span></span>
<span data-ttu-id="ae616-122">Sqoop 작업의 라이브러리 디렉터리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae616-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="ae616-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="ae616-123">-StatusFolder</span></span>
<span data-ttu-id="ae616-124">작업에 대 한 표준 출력 및 오류 출력을 포함 하는 폴더의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae616-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="ae616-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae616-125">CommonParameters</span></span>
<span data-ttu-id="ae616-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae616-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae616-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae616-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae616-128">입력</span><span class="sxs-lookup"><span data-stu-id="ae616-128">INPUTS</span></span>

### <span data-ttu-id="ae616-129">않아야</span><span class="sxs-lookup"><span data-stu-id="ae616-129">None</span></span>

## <span data-ttu-id="ae616-130">출력</span><span class="sxs-lookup"><span data-stu-id="ae616-130">OUTPUTS</span></span>

### <span data-ttu-id="ae616-131">AzureHDInsightSqoopJobDefinition의. m m.</span><span class="sxs-lookup"><span data-stu-id="ae616-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="ae616-132">상속자</span><span class="sxs-lookup"><span data-stu-id="ae616-132">NOTES</span></span>

## <span data-ttu-id="ae616-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae616-133">RELATED LINKS</span></span>

[<span data-ttu-id="ae616-134">시작-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ae616-134">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


