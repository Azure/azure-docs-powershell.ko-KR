---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightHiveJobDefinition.md
ms.openlocfilehash: fd933d157748de424aa425179701897772d93569
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537211"
---
# <span data-ttu-id="d9979-101">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d9979-101">New-AzureRmHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="d9979-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9979-102">SYNOPSIS</span></span>
<span data-ttu-id="d9979-103">하이브 작업 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d9979-103">Creates a Hive job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9979-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d9979-104">SYNTAX</span></span>

```
New-AzureRmHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9979-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d9979-105">DESCRIPTION</span></span>
<span data-ttu-id="d9979-106">**AzureRmHDInsightHiveJobDefinition** Cmdlet은 Azure HDInsight 클러스터와 함께 사용 하기 위한 하이브 작업 개체를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9979-106">The **New-AzureRmHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="d9979-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d9979-107">EXAMPLES</span></span>

### <span data-ttu-id="d9979-108">예제 1: 하이브 작업 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="d9979-108">Example 1: Create a Hive job definition</span></span>
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

<span data-ttu-id="d9979-109">이 명령은 하이브 작업 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d9979-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="d9979-110">변수</span><span class="sxs-lookup"><span data-stu-id="d9979-110">PARAMETERS</span></span>

### <span data-ttu-id="d9979-111">-인수</span><span class="sxs-lookup"><span data-stu-id="d9979-111">-Arguments</span></span>
<span data-ttu-id="d9979-112">작업에 대 한 인수 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9979-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="d9979-113">인수는 각 작업에 명령줄 인수로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9979-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="d9979-114">-정의</span><span class="sxs-lookup"><span data-stu-id="d9979-114">-Defines</span></span>
<span data-ttu-id="d9979-115">작업이 실행 될 때 설정할 Hadoop 구성 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9979-115">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="d9979-116">-파일</span><span class="sxs-lookup"><span data-stu-id="d9979-116">-File</span></span>
<span data-ttu-id="d9979-117">실행할 쿼리를 포함 하는 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9979-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="d9979-118">이 파일은 클러스터와 연결 된 저장소 계정에서 사용할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9979-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="d9979-119">*쿼리* 매개 변수 대신이 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9979-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="d9979-120">-파일</span><span class="sxs-lookup"><span data-stu-id="d9979-120">-Files</span></span>
<span data-ttu-id="d9979-121">Hive 작업과 연결 된 파일의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9979-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="d9979-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="d9979-122">-JobName</span></span>
<span data-ttu-id="d9979-123">작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9979-123">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="d9979-124">-쿼리</span><span class="sxs-lookup"><span data-stu-id="d9979-124">-Query</span></span>
<span data-ttu-id="d9979-125">하이브 쿼리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9979-125">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="d9979-126">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="d9979-126">-RunAsFileJob</span></span>
<span data-ttu-id="d9979-127">이 cmdlet이 쿼리를 저장할 기본 Azure 저장소 계정에 파일을 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d9979-127">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="d9979-128">이 cmdlet은이 파일을 참조 하는 작업을 실행 하도록 스크립트로 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9979-128">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="d9979-129">이 기능을 사용 하 여 백분율 기호 (%) 등의 특수 문자를 처리할 수 있습니다. Templeton는 URL 매개 변수로 백분율 기호가 있는 쿼리를 해석 하기 때문에 Templeton를 통한 작업 제출에 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9979-129">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="d9979-130">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="d9979-130">-StatusFolder</span></span>
<span data-ttu-id="d9979-131">작업에 대 한 표준 출력 및 오류 출력을 포함 하는 폴더의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9979-131">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="d9979-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9979-132">-DefaultProfile</span></span>
<span data-ttu-id="d9979-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d9979-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9979-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9979-134">CommonParameters</span></span>
<span data-ttu-id="d9979-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9979-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9979-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9979-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9979-137">입력</span><span class="sxs-lookup"><span data-stu-id="d9979-137">INPUTS</span></span>

## <span data-ttu-id="d9979-138">출력</span><span class="sxs-lookup"><span data-stu-id="d9979-138">OUTPUTS</span></span>

### <span data-ttu-id="d9979-139">AzureHDInsightHiveJobDefinition의. m m.</span><span class="sxs-lookup"><span data-stu-id="d9979-139">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="d9979-140">상속자</span><span class="sxs-lookup"><span data-stu-id="d9979-140">NOTES</span></span>

## <span data-ttu-id="d9979-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d9979-141">RELATED LINKS</span></span>

[<span data-ttu-id="d9979-142">시작-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d9979-142">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


