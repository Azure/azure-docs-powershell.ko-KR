---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
ms.openlocfilehash: 3d4ffa7a3172921b8aba7d73fc2c468c0e3117f3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868286"
---
# <span data-ttu-id="4330c-101">Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="4330c-101">Get-AzHDInsightJobOutput</span></span>

## <span data-ttu-id="4330c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4330c-102">SYNOPSIS</span></span>
<span data-ttu-id="4330c-103">지정한 클러스터와 연결 된 저장소 계정의 작업에 대 한 로그 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4330c-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

## <span data-ttu-id="4330c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4330c-104">SYNTAX</span></span>

```
Get-AzHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4330c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4330c-105">DESCRIPTION</span></span>
<span data-ttu-id="4330c-106">**AzHDInsightJobOutput** Cmdlet은 Azure HDInsight 클러스터와 연결 된 저장소 계정의 작업에 대 한 로그 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4330c-106">The **Get-AzHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="4330c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4330c-107">EXAMPLES</span></span>

### <span data-ttu-id="4330c-108">예제 1: 작업의 로그 출력 가져오기</span><span class="sxs-lookup"><span data-stu-id="4330c-108">Example 1: Get the log output for a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "<status folder>"
PS C:\> $query = "<query here>"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzHDInsightJobOutput `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="4330c-109">이 명령은-hadoop-001 이라는 클러스터의 로그 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4330c-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="4330c-110">변수</span><span class="sxs-lookup"><span data-stu-id="4330c-110">PARAMETERS</span></span>

### <span data-ttu-id="4330c-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4330c-111">-ClusterName</span></span>
<span data-ttu-id="4330c-112">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4330c-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="4330c-113">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="4330c-113">-DefaultContainer</span></span>
<span data-ttu-id="4330c-114">기본 컨테이너 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4330c-114">Specifies the default container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4330c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4330c-115">-DefaultProfile</span></span>
<span data-ttu-id="4330c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4330c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4330c-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4330c-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="4330c-118">기본 저장소 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4330c-118">Specifies the default Storage account key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4330c-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4330c-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="4330c-120">기본 저장소 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4330c-120">Specifies the default Storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4330c-121">-DisplayOutputType</span><span class="sxs-lookup"><span data-stu-id="4330c-121">-DisplayOutputType</span></span>
<span data-ttu-id="4330c-122">요청 되는 작업 출력 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4330c-122">Specifies the job output type being requested.</span></span>
<span data-ttu-id="4330c-123">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4330c-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4330c-124">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="4330c-124">StandardOutput</span></span>
- <span data-ttu-id="4330c-125">StandardError</span><span class="sxs-lookup"><span data-stu-id="4330c-125">StandardError</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Job.JobDisplayOutputType
Parameter Sets: (All)
Aliases:
Accepted values: StandardOutput, StandardError

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4330c-126">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="4330c-126">-HttpCredential</span></span>
<span data-ttu-id="4330c-127">클러스터에 대 한 HTTP (클러스터 로그인) 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4330c-127">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4330c-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="4330c-128">-JobId</span></span>
<span data-ttu-id="4330c-129">출력을 반입할 작업의 작업 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4330c-129">Specifies the job ID of the job whose output will be fetched.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4330c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4330c-130">-ResourceGroupName</span></span>
<span data-ttu-id="4330c-131">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4330c-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4330c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4330c-132">CommonParameters</span></span>
<span data-ttu-id="4330c-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4330c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4330c-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4330c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4330c-135">입력</span><span class="sxs-lookup"><span data-stu-id="4330c-135">INPUTS</span></span>

### <span data-ttu-id="4330c-136">않아야</span><span class="sxs-lookup"><span data-stu-id="4330c-136">None</span></span>

## <span data-ttu-id="4330c-137">출력</span><span class="sxs-lookup"><span data-stu-id="4330c-137">OUTPUTS</span></span>

### <span data-ttu-id="4330c-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4330c-138">System.String</span></span>

## <span data-ttu-id="4330c-139">상속자</span><span class="sxs-lookup"><span data-stu-id="4330c-139">NOTES</span></span>

## <span data-ttu-id="4330c-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4330c-140">RELATED LINKS</span></span>

[<span data-ttu-id="4330c-141">새로운 AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="4330c-141">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="4330c-142">시작-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="4330c-142">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


