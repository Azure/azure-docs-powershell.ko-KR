---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
ms.openlocfilehash: 2f63ba552931f70b745816a1d1b892977b6626e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537755"
---
# <span data-ttu-id="7129b-101">Get-AzureRmHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="7129b-101">Get-AzureRmHDInsightJobOutput</span></span>

## <span data-ttu-id="7129b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7129b-102">SYNOPSIS</span></span>
<span data-ttu-id="7129b-103">지정한 클러스터와 연결 된 저장소 계정의 작업에 대 한 로그 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7129b-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7129b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7129b-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7129b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7129b-105">DESCRIPTION</span></span>
<span data-ttu-id="7129b-106">**AzureRmHDInsightJobOutput** Cmdlet은 Azure HDInsight 클러스터와 연결 된 저장소 계정의 작업에 대 한 로그 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7129b-106">The **Get-AzureRmHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="7129b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7129b-107">EXAMPLES</span></span>

### <span data-ttu-id="7129b-108">예제 1: 작업의 로그 출력 가져오기</span><span class="sxs-lookup"><span data-stu-id="7129b-108">Example 1: Get the log output for a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "<status folder>"
PS C:\> $query = "<query here>"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzureRmHDInsightJobOutput `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="7129b-109">이 명령은-hadoop-001 이라는 클러스터의 로그 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7129b-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="7129b-110">변수</span><span class="sxs-lookup"><span data-stu-id="7129b-110">PARAMETERS</span></span>

### <span data-ttu-id="7129b-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7129b-111">-ClusterName</span></span>
<span data-ttu-id="7129b-112">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7129b-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="7129b-113">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="7129b-113">-DefaultContainer</span></span>
<span data-ttu-id="7129b-114">기본 컨테이너 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7129b-114">Specifies the default container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7129b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7129b-115">-DefaultProfile</span></span>
<span data-ttu-id="7129b-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7129b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7129b-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7129b-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="7129b-118">기본 저장소 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7129b-118">Specifies the default Storage account key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7129b-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7129b-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="7129b-120">기본 저장소 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7129b-120">Specifies the default Storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7129b-121">-DisplayOutputType</span><span class="sxs-lookup"><span data-stu-id="7129b-121">-DisplayOutputType</span></span>
<span data-ttu-id="7129b-122">요청 되는 작업 출력 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7129b-122">Specifies the job output type being requested.</span></span>
<span data-ttu-id="7129b-123">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7129b-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7129b-124">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="7129b-124">StandardOutput</span></span>
- <span data-ttu-id="7129b-125">StandardError</span><span class="sxs-lookup"><span data-stu-id="7129b-125">StandardError</span></span>

```yaml
Type: JobDisplayOutputType
Parameter Sets: (All)
Aliases: 
Accepted values: StandardOutput, StandardError

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7129b-126">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="7129b-126">-HttpCredential</span></span>
<span data-ttu-id="7129b-127">클러스터에 대 한 HTTP (클러스터 로그인) 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7129b-127">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7129b-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="7129b-128">-JobId</span></span>
<span data-ttu-id="7129b-129">출력을 반입할 작업의 작업 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7129b-129">Specifies the job ID of the job whose output will be fetched.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7129b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7129b-130">-ResourceGroupName</span></span>
<span data-ttu-id="7129b-131">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7129b-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7129b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7129b-132">CommonParameters</span></span>
<span data-ttu-id="7129b-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7129b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7129b-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7129b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7129b-135">입력</span><span class="sxs-lookup"><span data-stu-id="7129b-135">INPUTS</span></span>

### <span data-ttu-id="7129b-136">않아야</span><span class="sxs-lookup"><span data-stu-id="7129b-136">None</span></span>
<span data-ttu-id="7129b-137">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7129b-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7129b-138">출력</span><span class="sxs-lookup"><span data-stu-id="7129b-138">OUTPUTS</span></span>

### <span data-ttu-id="7129b-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7129b-139">System.String</span></span>

## <span data-ttu-id="7129b-140">상속자</span><span class="sxs-lookup"><span data-stu-id="7129b-140">NOTES</span></span>

## <span data-ttu-id="7129b-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7129b-141">RELATED LINKS</span></span>

[<span data-ttu-id="7129b-142">새로운 AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="7129b-142">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="7129b-143">시작-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="7129b-143">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


