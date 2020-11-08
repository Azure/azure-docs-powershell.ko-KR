---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 600D35F8-1E3C-4724-9F5E-75CF754F424F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0809415ea5dfff687c69089e1aeda60c9f3b00ee
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045720"
---
# <span data-ttu-id="46683-101">Add-AzureHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="46683-101">Add-AzureHDInsightScriptAction</span></span>

## <span data-ttu-id="46683-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46683-102">SYNOPSIS</span></span>
<span data-ttu-id="46683-103">HDInsight 스크립트 작업을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="46683-103">Adds an HDInsight script action.</span></span>

## <span data-ttu-id="46683-104">구문과</span><span class="sxs-lookup"><span data-stu-id="46683-104">SYNTAX</span></span>

```
Add-AzureHDInsightScriptAction -Config <AzureHDInsightConfig> -Name <String>
 -ClusterRoleCollection <ClusterNodeType[]> -Uri <Uri> [-Parameters <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="46683-105">설명은</span><span class="sxs-lookup"><span data-stu-id="46683-105">DESCRIPTION</span></span>
<span data-ttu-id="46683-106">이 버전의 Azure PowerShell HDInsight는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46683-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="46683-107">이러한 cmdlet은 2017 년 1 월 1 일에 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="46683-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="46683-108">최신 버전의 Azure PowerShell HDInsight를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="46683-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="46683-109">새 HDInsight를 사용 하 여 클러스터를 만드는 방법에 대 한 자세한 내용은 [HDInsight에서 Azure PowerShell ()을 사용 하 여 Linux 기반 클러스터 만들기](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 를 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="46683-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="46683-110">Azure PowerShell 및 기타 접근 방법을 사용 하 여 작업을 제출 하는 방법에 대 한 자세한 내용은 [HDInsight에서 Hadoop 작업 제출](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ()을 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="46683-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="46683-111">Azure PowerShell HDInsight에 대 한 참조 정보는 [Azure Hdinsight cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ()을 참조 하세요 https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="46683-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="46683-112">**AzureHDInsightScriptAction** cmdlet은 추가 소프트웨어를 설치 하거나 Windows PowerShell 스크립트를 사용 하 여 Hadoop 클러스터에서 실행 되는 응용 프로그램의 구성을 변경 하는 데 사용 되는 Azure HDInsight 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="46683-112">The **Add-AzureHDInsightScriptAction** cmdlet provides Azure HDInsight functionality that is used to install additional software or to change the configuration of applications that run on a Hadoop cluster by using Windows PowerShell scripts.</span></span>

<span data-ttu-id="46683-113">HDInsight 클러스터를 배포할 때 클러스터 노드에서 스크립트 작업을 실행 하 고 클러스터 전체 HDInsight 구성의 노드 이후 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="46683-113">A script action runs on the cluster nodes when HDInsight clusters are deployed, and they run after nodes in the cluster complete HDInsight configuration.</span></span>
<span data-ttu-id="46683-114">스크립트 동작은 시스템 관리자 계정 권한으로 실행 되며 클러스터 노드에 대 한 전체 액세스 권한을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="46683-114">The script action runs under system administrator account privileges and provides full access rights to the cluster nodes.</span></span>
<span data-ttu-id="46683-115">각 클러스터에 대해 지정 된 순서로 실행할 스크립트 작업 목록을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46683-115">You can provide each cluster with a list of script actions to run in a specified sequence.</span></span>

## <span data-ttu-id="46683-116">예제의</span><span class="sxs-lookup"><span data-stu-id="46683-116">EXAMPLES</span></span>

### <span data-ttu-id="46683-117">예제 1: 클러스터에 스크립트 동작 추가</span><span class="sxs-lookup"><span data-stu-id="46683-117">Example 1: Add a script action to a cluster</span></span>
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction" -Uri http://test.com/test.ps1 -Parameters "test" -ClusterRoleCollection HeadNode,DataNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

<span data-ttu-id="46683-118">첫 번째 명령은 **새 AzureHDInsightClusterConfig** cmdlet을 사용 하 여 HDInsight 클러스터 구성을 만든 다음이를 $Config 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="46683-118">The first command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>

<span data-ttu-id="46683-119">두 번째 명령은 **AzureHDInsightScriptAction** cmdlet을 사용 하 여 $Config TestScriptAction 이라는 스크립트 작업을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="46683-119">The second command uses the **Add-AzureHDInsightScriptAction** cmdlet to add the script action named TestScriptAction to $Config.</span></span>

<span data-ttu-id="46683-120">마지막 명령은 **AzureHDInsightCluster** cmdlet을 사용 하 여 $Config에 저장 된 스크립트 작업을 실행 하는 새 HDInsight 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="46683-120">The final command uses the **New-AzureHDInsightCluster** cmdlet to create a new HDInsight cluster that runs the script action stored in $Config.</span></span>

### <span data-ttu-id="46683-121">예제 2: 클러스터에 여러 스크립트 동작 추가</span><span class="sxs-lookup"><span data-stu-id="46683-121">Example 2: Add multiple script actions to a cluster</span></span>
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction1" -Uri http://test.com/test1.ps1 -Parameters "Test1" -ClusterRoleCollection HeadNode,DataNode | Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction2" -Uri http://test.com/test2.ps1 -ClusterRoleCollection HeadNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

<span data-ttu-id="46683-122">첫 번째 명령은 **새 AzureHDInsightClusterConfig** cmdlet을 사용 하 여 HDInsight 클러스터 구성을 만든 다음이를 $Config 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="46683-122">The first command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>

<span data-ttu-id="46683-123">두 번째 명령은 **AzureHDInsightScriptAction** cmdlet을 사용 하 여 $Config에 지정 된 스크립트 작업을 추가한 다음 파이프라인 연산자를 사용 하 여 $Config를 **추가-AzureHDInsightScriptAction** 에 전달 하 여 두 번째 스크립트 작업을 $Config에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="46683-123">The second command uses the **Add-AzureHDInsightScriptAction** cmdlet to add the specified script action to $Config, and then uses the pipeline operator to pass $Config to **Add-AzureHDInsightScriptAction** a second time to add a second script action to $Config.</span></span>

<span data-ttu-id="46683-124">마지막 명령은 **새 AzureHDInsightCluster** cmdlet을 사용 하 여 $Config에서 스크립트 작업을 실행 하는 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="46683-124">The final command uses the **New-AzureHDInsightCluster** cmdlet to create a cluster that runs the script actions in $Config.</span></span>

## <span data-ttu-id="46683-125">변수</span><span class="sxs-lookup"><span data-stu-id="46683-125">PARAMETERS</span></span>

### <span data-ttu-id="46683-126">-ClusterRoleCollection</span><span class="sxs-lookup"><span data-stu-id="46683-126">-ClusterRoleCollection</span></span>
<span data-ttu-id="46683-127">스크립트를 실행할 노드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46683-127">Specifies the nodes for which to run a script.</span></span>
<span data-ttu-id="46683-128">이 매개 변수에 허용 되는 값은 DataNode입니다.</span><span class="sxs-lookup"><span data-stu-id="46683-128">The acceptable values for this parameter are: HeadNode or DataNode.</span></span>

<span data-ttu-id="46683-129">값을 하나 또는 둘 다 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46683-129">You can specify one value or both values.</span></span>

```yaml
Type: ClusterNodeType[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46683-130">-구성</span><span class="sxs-lookup"><span data-stu-id="46683-130">-Config</span></span>
<span data-ttu-id="46683-131">구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46683-131">Specifies a configuration object.</span></span>
<span data-ttu-id="46683-132">이 cmdlet은이 매개 변수에서 지정 하는 개체에 스크립트 작업 정보를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="46683-132">This cmdlet adds script action information to the object that this parameter specifies.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46683-133">-이름</span><span class="sxs-lookup"><span data-stu-id="46683-133">-Name</span></span>
<span data-ttu-id="46683-134">스크립트 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46683-134">Specifies the name of a script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46683-135">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="46683-135">-Parameters</span></span>
<span data-ttu-id="46683-136">스크립트 작업에 필요한 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46683-136">Specifies the parameters that are required by a script action.</span></span>

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

### <span data-ttu-id="46683-137">-프로필</span><span class="sxs-lookup"><span data-stu-id="46683-137">-Profile</span></span>
<span data-ttu-id="46683-138">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46683-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="46683-139">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="46683-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46683-140">-Uri</span><span class="sxs-lookup"><span data-stu-id="46683-140">-Uri</span></span>
<span data-ttu-id="46683-141">실행할 스크립트의 URI 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46683-141">Specifies the URI location of a script to run.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46683-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46683-142">CommonParameters</span></span>
<span data-ttu-id="46683-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="46683-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46683-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46683-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46683-145">입력</span><span class="sxs-lookup"><span data-stu-id="46683-145">INPUTS</span></span>

## <span data-ttu-id="46683-146">출력</span><span class="sxs-lookup"><span data-stu-id="46683-146">OUTPUTS</span></span>

## <span data-ttu-id="46683-147">상속자</span><span class="sxs-lookup"><span data-stu-id="46683-147">NOTES</span></span>

## <span data-ttu-id="46683-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46683-148">RELATED LINKS</span></span>

[<span data-ttu-id="46683-149">새로운 AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="46683-149">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="46683-150">새로운 AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="46683-150">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)


