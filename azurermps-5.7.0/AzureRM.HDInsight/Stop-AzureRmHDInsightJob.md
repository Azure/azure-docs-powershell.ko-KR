---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/stop-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
ms.openlocfilehash: 82587d855b41a8112bac900f0efe6c4b30941eb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711434"
---
# <span data-ttu-id="448b3-101">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="448b3-101">Stop-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="448b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="448b3-102">SYNOPSIS</span></span>
<span data-ttu-id="448b3-103">클러스터에서 실행 중인 지정 된 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="448b3-103">Stops a specified running job on a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="448b3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="448b3-104">SYNTAX</span></span>

```
Stop-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="448b3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="448b3-105">DESCRIPTION</span></span>
<span data-ttu-id="448b3-106">**AzureRmHDInsightJob** Cmdlet은 Azure HDInsight 클러스터에서 지정 된 실행 중인 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="448b3-106">The **Stop-AzureRmHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="448b3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="448b3-107">EXAMPLES</span></span>

### <span data-ttu-id="448b3-108">예제 1: 지정 된 클러스터에서 작업 중지</span><span class="sxs-lookup"><span data-stu-id="448b3-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="448b3-109">이 명령은-hadoop-001 이라는 클러스터에서 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="448b3-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="448b3-110">변수</span><span class="sxs-lookup"><span data-stu-id="448b3-110">PARAMETERS</span></span>

### <span data-ttu-id="448b3-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="448b3-111">-ClusterName</span></span>
<span data-ttu-id="448b3-112">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="448b3-112">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="448b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="448b3-113">-DefaultProfile</span></span>
<span data-ttu-id="448b3-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="448b3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="448b3-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="448b3-115">-HttpCredential</span></span>
<span data-ttu-id="448b3-116">클러스터에 대 한 HTTP (클러스터 로그인) 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="448b3-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="448b3-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="448b3-117">-JobId</span></span>
<span data-ttu-id="448b3-118">작업의 작업 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="448b3-118">Specifies the job ID of the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="448b3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="448b3-119">-ResourceGroupName</span></span>
<span data-ttu-id="448b3-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="448b3-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="448b3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="448b3-121">CommonParameters</span></span>
<span data-ttu-id="448b3-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="448b3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="448b3-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="448b3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="448b3-124">입력</span><span class="sxs-lookup"><span data-stu-id="448b3-124">INPUTS</span></span>

### <span data-ttu-id="448b3-125">이름</span><span class="sxs-lookup"><span data-stu-id="448b3-125">String</span></span>
<span data-ttu-id="448b3-126">' JobId ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="448b3-126">Parameter 'JobId' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="448b3-127">출력</span><span class="sxs-lookup"><span data-stu-id="448b3-127">OUTPUTS</span></span>

### <span data-ttu-id="448b3-128">AzureHDInsightJob의. m m.</span><span class="sxs-lookup"><span data-stu-id="448b3-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="448b3-129">상속자</span><span class="sxs-lookup"><span data-stu-id="448b3-129">NOTES</span></span>

## <span data-ttu-id="448b3-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="448b3-130">RELATED LINKS</span></span>

[<span data-ttu-id="448b3-131">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="448b3-131">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="448b3-132">시작-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="448b3-132">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="448b3-133">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="448b3-133">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


