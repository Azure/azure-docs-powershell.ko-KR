---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: FF41DDBA-6D4B-47A5-BCFF-3D0BB1D375C5
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2b6aaf5e8564b3eea675a57176b8f7118d2c7a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045960"
---
# <span data-ttu-id="f713b-101">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="f713b-101">Set-AzureHDInsightDefaultStorage</span></span>

## <span data-ttu-id="f713b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f713b-102">SYNOPSIS</span></span>
<span data-ttu-id="f713b-103">HDInsight 클러스터에 대 한 기본 저장소 계정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f713b-103">Sets the default storage account for an HDInsight cluster.</span></span>

## <span data-ttu-id="f713b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f713b-104">SYNTAX</span></span>

```
Set-AzureHDInsightDefaultStorage -Config <AzureHDInsightConfig> -StorageAccountKey <String>
 -StorageAccountName <String> -StorageContainerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f713b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f713b-105">DESCRIPTION</span></span>
<span data-ttu-id="f713b-106">이 버전의 Azure PowerShell HDInsight는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f713b-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="f713b-107">이러한 cmdlet은 2017 년 1 월 1 일에 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f713b-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="f713b-108">최신 버전의 Azure PowerShell HDInsight를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="f713b-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="f713b-109">새 HDInsight를 사용 하 여 클러스터를 만드는 방법에 대 한 자세한 내용은 [HDInsight에서 Azure PowerShell ()을 사용 하 여 Linux 기반 클러스터 만들기](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 를 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="f713b-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="f713b-110">Azure PowerShell 및 기타 접근 방법을 사용 하 여 작업을 제출 하는 방법에 대 한 자세한 내용은 [HDInsight에서 Hadoop 작업 제출](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ()을 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="f713b-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="f713b-111">Azure PowerShell HDInsight에 대 한 참조 정보는 [Azure Hdinsight cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ()을 참조 하세요 https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f713b-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="f713b-112">**AzureHDInsightDefaultStorage** Cmdlet은 HDInsight 클러스터 구성에 대 한 기본 저장소 계정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f713b-112">The **Set-AzureHDInsightDefaultStorage** cmdlet sets the default storage account for an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="f713b-113">예제의</span><span class="sxs-lookup"><span data-stu-id="f713b-113">EXAMPLES</span></span>

### <span data-ttu-id="f713b-114">예제 1: 기본 저장소 계정 설정</span><span class="sxs-lookup"><span data-stu-id="f713b-114">Example 1: Set the default storage account</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
    | Set-AzureHDInsightDefaultStorage -StorageAccountName "MyBlobStorage.blob.core.windows.net" -StorageAccountKey $Key1 -StorageContainerName "MyContainer"
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.widows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds
```

<span data-ttu-id="f713b-115">첫 번째 명령은 **AzureSubscription** cmdlet을 사용 하 여 현재 구독 ID를 가져오고 $SubId 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f713b-115">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="f713b-116">두 번째 및 세 번째 명령은 **가져오기-AzureStorageKey** cmdlet을 사용 하 여 MyBlobStorage 및 MySecondBlobStorage에 대 한 기본 저장소 키를 얻은 다음 키를 각각 $Key 1 및 $Key 2 개의 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f713b-116">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="f713b-117">네 번째, 다섯 번째 및 여섯 번째 명령은 현재 구독에 대 한 자격 증명을 **가져오고 자격 증명 cmdlet을** 사용 하 여 $Creds, $OozieCreds 및 $HiveCreds 변수에 자격 증명을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f713b-117">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription, and then stores the credentials in the $Creds, $OozieCreds, and $HiveCreds variables.</span></span>

<span data-ttu-id="f713b-118">마지막 명령은 다음 cmdlet을 사용 하 여 일련의 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f713b-118">The final command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="f713b-119">**AzureHDInsightClusterConfig-** HDInsight 클러스터 구성을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f713b-119">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="f713b-120">**Set-AzureHDInsightDefaultStorage-** 구성에 대 한 기본 저장소 계정을 MyBlobStorage.blob.core.windows.net으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f713b-120">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="f713b-121">**추가-AzureHDInsightStorage** MySecondBlobStorage.blob.core.windows.net 라는 두 번째 저장소 계정을 구성에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f713b-121">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="f713b-122">**Add-AzureHDInsightMetastore** 를 추가 하 여 Oozie의 Metastore 및 Hive에 대 한 metastore를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f713b-122">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="f713b-123">**AzureHDInsightCluster** 새 구성으로 HDInsight 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f713b-123">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="f713b-124">변수</span><span class="sxs-lookup"><span data-stu-id="f713b-124">PARAMETERS</span></span>

### <span data-ttu-id="f713b-125">-구성</span><span class="sxs-lookup"><span data-stu-id="f713b-125">-Config</span></span>
<span data-ttu-id="f713b-126">구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f713b-126">Specifies a configuration object.</span></span>
<span data-ttu-id="f713b-127">이 cmdlet은이 매개 변수에서 지정 하는 개체에 대 한 기본 저장소 계정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f713b-127">This cmdlet sets the default storage account for the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="f713b-128">-프로필</span><span class="sxs-lookup"><span data-stu-id="f713b-128">-Profile</span></span>
<span data-ttu-id="f713b-129">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f713b-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f713b-130">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f713b-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f713b-131">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f713b-131">-StorageAccountKey</span></span>
<span data-ttu-id="f713b-132">기본 저장소 계정에 액세스 하는 데 사용 되는 저장소 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f713b-132">Specifies the storage account key that is used to access the default storage account.</span></span>

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

### <span data-ttu-id="f713b-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f713b-133">-StorageAccountName</span></span>
<span data-ttu-id="f713b-134">기본 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f713b-134">Specifies the name of a default storage account.</span></span>

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

### <span data-ttu-id="f713b-135">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="f713b-135">-StorageContainerName</span></span>
<span data-ttu-id="f713b-136">클러스터에 대 한 기본 저장소 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f713b-136">Specifies the name of the default storage container for a cluster.</span></span>

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

### <span data-ttu-id="f713b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f713b-137">CommonParameters</span></span>
<span data-ttu-id="f713b-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f713b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f713b-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f713b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f713b-140">입력</span><span class="sxs-lookup"><span data-stu-id="f713b-140">INPUTS</span></span>

## <span data-ttu-id="f713b-141">출력</span><span class="sxs-lookup"><span data-stu-id="f713b-141">OUTPUTS</span></span>

## <span data-ttu-id="f713b-142">상속자</span><span class="sxs-lookup"><span data-stu-id="f713b-142">NOTES</span></span>

## <span data-ttu-id="f713b-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f713b-143">RELATED LINKS</span></span>

[<span data-ttu-id="f713b-144">추가-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="f713b-144">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="f713b-145">추가-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="f713b-145">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="f713b-146">새로운 AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f713b-146">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="f713b-147">새로운 AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="f713b-147">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)


