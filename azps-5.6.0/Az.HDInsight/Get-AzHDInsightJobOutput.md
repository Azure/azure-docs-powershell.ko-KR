---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
ms.openlocfilehash: d36f49110cb3c3f4d51c9223e2a7ab150eb779ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992693"
---
# <span data-ttu-id="4e4b4-101">Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="4e4b4-101">Get-AzHDInsightJobOutput</span></span>

## <span data-ttu-id="4e4b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e4b4-102">SYNOPSIS</span></span>
<span data-ttu-id="4e4b4-103">지정된 클러스터와 연결된 저장소 계정에서 작업의 로그 출력을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4e4b4-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

## <span data-ttu-id="4e4b4-104">구문</span><span class="sxs-lookup"><span data-stu-id="4e4b4-104">SYNTAX</span></span>

```
Get-AzHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e4b4-105">설명</span><span class="sxs-lookup"><span data-stu-id="4e4b4-105">DESCRIPTION</span></span>
<span data-ttu-id="4e4b4-106">**Get-AzHDInsightJobOutput** cmdlet은 Azure HDInsight 클러스터와 연결된 Storage 계정에서 작업의 로그 출력을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4e4b4-106">The **Get-AzHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="4e4b4-107">예제</span><span class="sxs-lookup"><span data-stu-id="4e4b4-107">EXAMPLES</span></span>

### <span data-ttu-id="4e4b4-108">예제 1: 작업의 로그 출력 얻기</span><span class="sxs-lookup"><span data-stu-id="4e4b4-108">Example 1: Get the log output for a job</span></span>
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

<span data-ttu-id="4e4b4-109">이 명령은 your-hadoop-001이라는 클러스터에서 로그 출력을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4e4b4-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="4e4b4-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4e4b4-110">PARAMETERS</span></span>

### <span data-ttu-id="4e4b4-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4e4b4-111">-ClusterName</span></span>
<span data-ttu-id="4e4b4-112">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4e4b4-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="4e4b4-113">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="4e4b4-113">-DefaultContainer</span></span>
<span data-ttu-id="4e4b4-114">기본 컨테이너 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4e4b4-114">Specifies the default container name.</span></span>

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

### <span data-ttu-id="4e4b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e4b4-115">-DefaultProfile</span></span>
<span data-ttu-id="4e4b4-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4e4b4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e4b4-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4e4b4-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="4e4b4-118">기본 Storage 계정 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4e4b4-118">Specifies the default Storage account key.</span></span>

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

### <span data-ttu-id="4e4b4-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4e4b4-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="4e4b4-120">기본 Storage 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4e4b4-120">Specifies the default Storage account name.</span></span>

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

### <span data-ttu-id="4e4b4-121">-DisplayOutputType</span><span class="sxs-lookup"><span data-stu-id="4e4b4-121">-DisplayOutputType</span></span>
<span data-ttu-id="4e4b4-122">요청되는 작업 출력 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4e4b4-122">Specifies the job output type being requested.</span></span>
<span data-ttu-id="4e4b4-123">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="4e4b4-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4e4b4-124">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="4e4b4-124">StandardOutput</span></span>
- <span data-ttu-id="4e4b4-125">StandardError</span><span class="sxs-lookup"><span data-stu-id="4e4b4-125">StandardError</span></span>

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

### <span data-ttu-id="4e4b4-126">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="4e4b4-126">-HttpCredential</span></span>
<span data-ttu-id="4e4b4-127">클러스터에 대한 HTTP(클러스터 로그인) 자격 증명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4e4b4-127">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="4e4b4-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="4e4b4-128">-JobId</span></span>
<span data-ttu-id="4e4b4-129">출력을 인출할 작업의 작업 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4e4b4-129">Specifies the job ID of the job whose output will be fetched.</span></span>

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

### <span data-ttu-id="4e4b4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e4b4-130">-ResourceGroupName</span></span>
<span data-ttu-id="4e4b4-131">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4e4b4-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4e4b4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e4b4-132">CommonParameters</span></span>
<span data-ttu-id="4e4b4-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4e4b4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e4b4-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e4b4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e4b4-135">입력</span><span class="sxs-lookup"><span data-stu-id="4e4b4-135">INPUTS</span></span>

### <span data-ttu-id="4e4b4-136">없음</span><span class="sxs-lookup"><span data-stu-id="4e4b4-136">None</span></span>

## <span data-ttu-id="4e4b4-137">출력</span><span class="sxs-lookup"><span data-stu-id="4e4b4-137">OUTPUTS</span></span>

### <span data-ttu-id="4e4b4-138">System.String</span><span class="sxs-lookup"><span data-stu-id="4e4b4-138">System.String</span></span>

## <span data-ttu-id="4e4b4-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4e4b4-139">NOTES</span></span>

## <span data-ttu-id="4e4b4-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4e4b4-140">RELATED LINKS</span></span>

[<span data-ttu-id="4e4b4-141">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="4e4b4-141">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="4e4b4-142">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="4e4b4-142">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


