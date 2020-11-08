---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 1B6AC121-1AA0-4D28-B1EA-C96147FDD168
online version: ''
schema: 2.0.0
ms.openlocfilehash: 02435c28ca17666a3b19389fde039353f3d779a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045716"
---
# <span data-ttu-id="bb4e1-101">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="bb4e1-101">Add-AzureHDInsightStorage</span></span>

## <span data-ttu-id="bb4e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb4e1-102">SYNOPSIS</span></span>
<span data-ttu-id="bb4e1-103">HDInsight 구성에 blob 저장소 계정 항목을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb4e1-103">Adds a blob storage account entry to an HDInsight configuration.</span></span>

## <span data-ttu-id="bb4e1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bb4e1-104">SYNTAX</span></span>

```
Add-AzureHDInsightStorage -Config <AzureHDInsightConfig> -StorageAccountKey <String>
 -StorageAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bb4e1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bb4e1-105">DESCRIPTION</span></span>
<span data-ttu-id="bb4e1-106">이 버전의 Azure PowerShell HDInsight는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bb4e1-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="bb4e1-107">이러한 cmdlet은 2017 년 1 월 1 일에 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bb4e1-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="bb4e1-108">최신 버전의 Azure PowerShell HDInsight를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="bb4e1-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="bb4e1-109">새 HDInsight를 사용 하 여 클러스터를 만드는 방법에 대 한 자세한 내용은 [HDInsight에서 Azure PowerShell ()을 사용 하 여 Linux 기반 클러스터 만들기](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 를 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="bb4e1-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="bb4e1-110">Azure PowerShell 및 기타 접근 방법을 사용 하 여 작업을 제출 하는 방법에 대 한 자세한 내용은 [HDInsight에서 Hadoop 작업 제출](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ()을 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="bb4e1-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="bb4e1-111">Azure PowerShell HDInsight에 대 한 참조 정보는 [Azure Hdinsight cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ()을 참조 하세요 https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="bb4e1-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="bb4e1-112">**Add-AzureHDInsightStorage** Cmdlet은 Azure HDInsight 구성에 blob 저장소 계정 항목을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb4e1-112">The **Add-AzureHDInsightStorage** cmdlet adds a blob storage account entry to an Azure HDInsight configuration.</span></span>

## <span data-ttu-id="bb4e1-113">예제의</span><span class="sxs-lookup"><span data-stu-id="bb4e1-113">EXAMPLES</span></span>

### <span data-ttu-id="bb4e1-114">예제 1: 저장소 계정 추가</span><span class="sxs-lookup"><span data-stu-id="bb4e1-114">Example 1: Add a storage account</span></span>
```
PS C:\>$StoreConfig = Add-AzureHDInsightStorage -Config $Config -StorageAccountName "MyStorage" -StorageAccountKey "Key"
```

<span data-ttu-id="bb4e1-115">이 명령은 MyStorage 라는 저장소 계정을 $Config에 저장 된 구성 개체에 추가한 다음 구성을 $StoreConfig 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb4e1-115">This command adds a storage account named MyStorage to the configuration object stored in $Config, and then stores the configuration in the $StoreConfig variable.</span></span>

### <span data-ttu-id="bb4e1-116">예제 2: 여러 저장소 계정 구성</span><span class="sxs-lookup"><span data-stu-id="bb4e1-116">Example 2: Configure multiple storage accounts</span></span>
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
    | Add-AzureHDInsightMetastore -SqlAzureServerName "Sqlserver01.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "Sqlserver01.database.windows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubID -Credential $Creds
```

<span data-ttu-id="bb4e1-117">첫 번째 명령은 **AzureSubscription** cmdlet을 사용 하 여 현재 구독 ID를 가져오고 $SubId 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb4e1-117">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="bb4e1-118">두 번째 및 세 번째 명령은 **가져오기-AzureStorageKey** cmdlet을 사용 하 여 MyBlobStorage 및 MySecondBlobStorage에 대 한 기본 저장소 키를 얻은 다음 키를 각각 $Key 1 및 $Key 2 개의 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb4e1-118">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="bb4e1-119">네 번째, 다섯 번째 및 여섯 번째 명령은 현재 구독과 Oozie 및 Hive에 대 한 자격 증명을 얻은 다음 변수에 자격 증명을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb4e1-119">The fourth, fifth, and sixth commands get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="bb4e1-120">마지막 명령은 다음 cmdlet을 사용 하 여 일련의 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb4e1-120">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="bb4e1-121">**새로운 기능-** HDInsight 클러스터 구성을 만들기 AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="bb4e1-121">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration</span></span>
- <span data-ttu-id="bb4e1-122">**Set-AzureHDInsightDefaultStorage-** configuration에 대 한 기본 저장소 계정을 MyBlobStorage.blob.core.windows.net로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb4e1-122">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net</span></span>
- <span data-ttu-id="bb4e1-123">**추가-AzureHDInsightStorage** 구성에 MySecondBlobStorage.blob.core.windows.net 이라는 두 번째 저장소 계정을 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="bb4e1-123">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration</span></span>
- <span data-ttu-id="bb4e1-124">**추가-AzureHDInsightStorage** Oozie의 Metastore 및 Hive에 대 한 metastore를 구성에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb4e1-124">**Add-AzureHDInsightStorage** to add a metastore for Oozie and a metastore for Hive to the configuration</span></span>
- <span data-ttu-id="bb4e1-125">**New-** 새로운 구성으로 HDInsight 클러스터 만들기 AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="bb4e1-125">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration</span></span>

## <span data-ttu-id="bb4e1-126">변수</span><span class="sxs-lookup"><span data-stu-id="bb4e1-126">PARAMETERS</span></span>

### <span data-ttu-id="bb4e1-127">-구성</span><span class="sxs-lookup"><span data-stu-id="bb4e1-127">-Config</span></span>
<span data-ttu-id="bb4e1-128">구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb4e1-128">Specifies a configuration object.</span></span>
<span data-ttu-id="bb4e1-129">이 cmdlet은이 매개 변수에서 지정 하는 개체에 저장소 계정 정보를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb4e1-129">This cmdlet adds storage account information to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="bb4e1-130">-프로필</span><span class="sxs-lookup"><span data-stu-id="bb4e1-130">-Profile</span></span>
<span data-ttu-id="bb4e1-131">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb4e1-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bb4e1-132">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="bb4e1-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bb4e1-133">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="bb4e1-133">-StorageAccountKey</span></span>
<span data-ttu-id="bb4e1-134">저장소 계정에 액세스 하는 데 사용 되는 저장소 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb4e1-134">Specifies the storage account key that is used to access a storage account.</span></span>

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

### <span data-ttu-id="bb4e1-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bb4e1-135">-StorageAccountName</span></span>
<span data-ttu-id="bb4e1-136">추가할 Azure 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb4e1-136">Specifies the name of the Azure storage account to add.</span></span>

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

### <span data-ttu-id="bb4e1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb4e1-137">CommonParameters</span></span>
<span data-ttu-id="bb4e1-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb4e1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb4e1-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb4e1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb4e1-140">입력</span><span class="sxs-lookup"><span data-stu-id="bb4e1-140">INPUTS</span></span>

## <span data-ttu-id="bb4e1-141">출력</span><span class="sxs-lookup"><span data-stu-id="bb4e1-141">OUTPUTS</span></span>

## <span data-ttu-id="bb4e1-142">상속자</span><span class="sxs-lookup"><span data-stu-id="bb4e1-142">NOTES</span></span>

## <span data-ttu-id="bb4e1-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb4e1-143">RELATED LINKS</span></span>

[<span data-ttu-id="bb4e1-144">새로운 AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="bb4e1-144">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="bb4e1-145">새로운 AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="bb4e1-145">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="bb4e1-146">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="bb4e1-146">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)


