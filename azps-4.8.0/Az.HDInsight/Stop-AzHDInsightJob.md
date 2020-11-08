---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/stop-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
ms.openlocfilehash: d5e38cf3edb89801b630735dee1ce0dbd1d62d41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211987"
---
# <span data-ttu-id="d2710-101">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d2710-101">Stop-AzHDInsightJob</span></span>

## <span data-ttu-id="d2710-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2710-102">SYNOPSIS</span></span>
<span data-ttu-id="d2710-103">클러스터에서 실행 중인 지정 된 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2710-103">Stops a specified running job on a cluster.</span></span>

## <span data-ttu-id="d2710-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d2710-104">SYNTAX</span></span>

```
Stop-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2710-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d2710-105">DESCRIPTION</span></span>
<span data-ttu-id="d2710-106">**AzHDInsightJob** Cmdlet은 Azure HDInsight 클러스터에서 지정 된 실행 중인 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2710-106">The **Stop-AzHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="d2710-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d2710-107">EXAMPLES</span></span>

### <span data-ttu-id="d2710-108">예제 1: 지정 된 클러스터에서 작업 중지</span><span class="sxs-lookup"><span data-stu-id="d2710-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="d2710-109">이 명령은-hadoop-001 이라는 클러스터에서 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2710-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="d2710-110">변수</span><span class="sxs-lookup"><span data-stu-id="d2710-110">PARAMETERS</span></span>

### <span data-ttu-id="d2710-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d2710-111">-ClusterName</span></span>
<span data-ttu-id="d2710-112">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2710-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2710-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2710-113">-DefaultProfile</span></span>
<span data-ttu-id="d2710-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d2710-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2710-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="d2710-115">-HttpCredential</span></span>
<span data-ttu-id="d2710-116">클러스터에 대 한 HTTP (클러스터 로그인) 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2710-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2710-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="d2710-117">-JobId</span></span>
<span data-ttu-id="d2710-118">작업의 작업 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2710-118">Specifies the job ID of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2710-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2710-119">-ResourceGroupName</span></span>
<span data-ttu-id="d2710-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2710-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d2710-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2710-121">CommonParameters</span></span>
<span data-ttu-id="d2710-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2710-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2710-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2710-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2710-124">입력</span><span class="sxs-lookup"><span data-stu-id="d2710-124">INPUTS</span></span>

### <span data-ttu-id="d2710-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d2710-125">System.String</span></span>

## <span data-ttu-id="d2710-126">출력</span><span class="sxs-lookup"><span data-stu-id="d2710-126">OUTPUTS</span></span>

### <span data-ttu-id="d2710-127">AzureHDInsightJob의. m m.</span><span class="sxs-lookup"><span data-stu-id="d2710-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="d2710-128">상속자</span><span class="sxs-lookup"><span data-stu-id="d2710-128">NOTES</span></span>

## <span data-ttu-id="d2710-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2710-129">RELATED LINKS</span></span>

[<span data-ttu-id="d2710-130">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d2710-130">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="d2710-131">시작-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d2710-131">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="d2710-132">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d2710-132">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


