---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: EB196CF5-3E2C-4F38-A983-3365A379672A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 637fc6f65c7168db9ba7e45cea7268208b334c99
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045723"
---
# <span data-ttu-id="4b9a1-101">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="4b9a1-101">Add-AzureHDInsightMetastore</span></span>

## <span data-ttu-id="4b9a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b9a1-102">SYNOPSIS</span></span>
<span data-ttu-id="4b9a1-103">HDInsight 클러스터 구성에 SQL Server 데이터베이스 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-103">Adds a SQL Server database account to an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="4b9a1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4b9a1-104">SYNTAX</span></span>

```
Add-AzureHDInsightMetastore -Config <AzureHDInsightConfig> -Credential <PSCredential> -DatabaseName <String>
 -MetastoreType <AzureHDInsightMetastoreType> -SqlAzureServerName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="4b9a1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4b9a1-105">DESCRIPTION</span></span>
<span data-ttu-id="4b9a1-106">이 버전의 Azure PowerShell HDInsight는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="4b9a1-107">이러한 cmdlet은 2017 년 1 월 1 일에 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="4b9a1-108">최신 버전의 Azure PowerShell HDInsight를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="4b9a1-109">새 HDInsight를 사용 하 여 클러스터를 만드는 방법에 대 한 자세한 내용은 [HDInsight에서 Azure PowerShell ()을 사용 하 여 Linux 기반 클러스터 만들기](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 를 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="4b9a1-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="4b9a1-110">Azure PowerShell 및 기타 접근 방법을 사용 하 여 작업을 제출 하는 방법에 대 한 자세한 내용은 [HDInsight에서 Hadoop 작업 제출](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ()을 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="4b9a1-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="4b9a1-111">Azure PowerShell HDInsight에 대 한 참조 정보는 [Azure Hdinsight cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ()을 참조 하세요 https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4b9a1-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="4b9a1-112">**AzureHDInsightMetastore** Cmdlet은 **새 AzureHDInsightClusterConfig** Cmdlet에서 만든 Azure HDINSIGHT 구성에 Microsoft SQL Server 데이터베이스를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-112">The **Add-AzureHDInsightMetastore** cmdlet adds a Microsoft SQL Server database to an Azure HDInsight configuration that is created by the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>
<span data-ttu-id="4b9a1-113">데이터베이스는 Hive 또는 Oozie에 대 한 메타 데이터를 저장 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-113">The database is used to store metadata for Hive or Oozie, or both.</span></span>

## <span data-ttu-id="4b9a1-114">예제의</span><span class="sxs-lookup"><span data-stu-id="4b9a1-114">EXAMPLES</span></span>

### <span data-ttu-id="4b9a1-115">예제 1: metastore 추가</span><span class="sxs-lookup"><span data-stu-id="4b9a1-115">Example 1: Add a metastore</span></span>
```
PS C:\>$Metaconfig = Add-AzureHDInsightMetastore -Config $Config -SqlAzureServerName "ContosoSQLServer" -DatabaseName "DBname" -Credential (Get-Credential) -MetastoreType HiveMetaStore
```

<span data-ttu-id="4b9a1-116">이 명령은 HDInsight 클러스터의 하이브 metastore 역할을 하는 ContosoSQLServer 이라는 SQL Server 데이터베이스를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-116">This command adds a SQL Server database named ContosoSQLServer to serve as a Hive metastore for an HDInsight cluster.</span></span>

### <span data-ttu-id="4b9a1-117">예제 2: 저장소 구성 및 metastores 추가</span><span class="sxs-lookup"><span data-stu-id="4b9a1-117">Example 2: Configure storage and add metastores</span></span>
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

<span data-ttu-id="4b9a1-118">첫 번째 명령은 **AzureSubscription** cmdlet을 사용 하 여 현재 구독 ID를 가져오고 $SubId 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-118">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="4b9a1-119">두 번째 및 세 번째 명령은 **가져오기-AzureStorageKey** cmdlet을 사용 하 여 MyBlobStorage 및 MySecondBlobStorage에 대 한 기본 저장소 키를 얻은 다음 키를 각각 $Key 1 및 $Key 2 개의 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-119">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="4b9a1-120">네 번째, 다섯 번째 및 여섯 번째 명령은 Oozie 및 Hive에 대 한 자격 증명을 가져오기 위해 **get-Credential** cmdlet을 사용 하 고 자격 증명을 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-120">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="4b9a1-121">마지막 명령은 다음 cmdlet을 사용 하 여 일련의 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-121">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="4b9a1-122">**AzureHDInsightClusterConfig-** HDInsight 클러스터 구성을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-122">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="4b9a1-123">**Set-AzureHDInsightDefaultStorage-** 구성에 대 한 기본 저장소 계정을 MyBlobStorage.blob.core.windows.net으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-123">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="4b9a1-124">**추가-AzureHDInsightStorage** MySecondBlobStorage.blob.core.windows.net 라는 두 번째 저장소 계정을 구성에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-124">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="4b9a1-125">**Add-AzureHDInsightMetastore** 를 추가 하 여 Oozie의 Metastore 및 Hive에 대 한 metastore를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-125">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="4b9a1-126">**AzureHDInsightCluster** 새 구성으로 HDInsight 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-126">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="4b9a1-127">변수</span><span class="sxs-lookup"><span data-stu-id="4b9a1-127">PARAMETERS</span></span>

### <span data-ttu-id="4b9a1-128">-구성</span><span class="sxs-lookup"><span data-stu-id="4b9a1-128">-Config</span></span>
<span data-ttu-id="4b9a1-129">구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-129">Specifies a configuration object.</span></span>
<span data-ttu-id="4b9a1-130">이 cmdlet은이 매개 변수에서 지정 하는 구성 개체에 metastore 정보를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-130">This cmdlet adds metastore information to the configuration object that this parameter specifies.</span></span>

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

### <span data-ttu-id="4b9a1-131">-Credential</span><span class="sxs-lookup"><span data-stu-id="4b9a1-131">-Credential</span></span>
<span data-ttu-id="4b9a1-132">SQL Server 데이터베이스에 액세스 하는 데 사용 되는 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-132">Specifies the credentials that are used to access a SQL Server database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b9a1-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4b9a1-133">-DatabaseName</span></span>
<span data-ttu-id="4b9a1-134">Hive 또는 Oozie 메타 데이터를 저장할 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-134">Specifies the name of the database to store Hive or Oozie metadata.</span></span>

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

### <span data-ttu-id="4b9a1-135">-MetastoreType</span><span class="sxs-lookup"><span data-stu-id="4b9a1-135">-MetastoreType</span></span>
<span data-ttu-id="4b9a1-136">Metastore 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-136">Specifies the metastore type.</span></span>
<span data-ttu-id="4b9a1-137">이 매개 변수에 허용 되는 값은 HiveMetaStore 또는 OozieMetaStore입니다.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-137">The acceptable values for this parameter are: HiveMetaStore or OozieMetaStore.</span></span>

```yaml
Type: AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b9a1-138">-프로필</span><span class="sxs-lookup"><span data-stu-id="4b9a1-138">-Profile</span></span>
<span data-ttu-id="4b9a1-139">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4b9a1-140">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4b9a1-141">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="4b9a1-141">-SqlAzureServerName</span></span>
<span data-ttu-id="4b9a1-142">메타 데이터를 저장할 데이터베이스를 포함 하는 SQL Server의 FQDN (정규화 된 도메인 이름)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-142">Specifies the fully qualified domain name (FQDN) of the SQL Server that contains the database to store metadata.</span></span>

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

### <span data-ttu-id="4b9a1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b9a1-143">CommonParameters</span></span>
<span data-ttu-id="4b9a1-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b9a1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b9a1-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b9a1-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b9a1-146">입력</span><span class="sxs-lookup"><span data-stu-id="4b9a1-146">INPUTS</span></span>

## <span data-ttu-id="4b9a1-147">출력</span><span class="sxs-lookup"><span data-stu-id="4b9a1-147">OUTPUTS</span></span>

## <span data-ttu-id="4b9a1-148">상속자</span><span class="sxs-lookup"><span data-stu-id="4b9a1-148">NOTES</span></span>

## <span data-ttu-id="4b9a1-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b9a1-149">RELATED LINKS</span></span>

[<span data-ttu-id="4b9a1-150">추가-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="4b9a1-150">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="4b9a1-151">새로운 AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4b9a1-151">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="4b9a1-152">새로운 AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="4b9a1-152">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="4b9a1-153">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="4b9a1-153">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)
