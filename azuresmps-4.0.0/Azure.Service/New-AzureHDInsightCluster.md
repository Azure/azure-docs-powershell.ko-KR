---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3EDD612F-AC5D-4D4D-BB14-2FB8DE5EDCCE
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4652cb1b30717b5ea11d596646dc43e2a5ec4a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045923"
---
# <span data-ttu-id="ad77b-101">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ad77b-101">New-AzureHDInsightCluster</span></span>

## <span data-ttu-id="ad77b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad77b-102">SYNOPSIS</span></span>
<span data-ttu-id="ad77b-103">HDInsight 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-103">Creates an HDInsight cluster.</span></span>

## <span data-ttu-id="ad77b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ad77b-104">SYNTAX</span></span>

### <span data-ttu-id="ad77b-105">구성별 클러스터 (특정 구독 자격 증명과 함께) (기본값)</span><span class="sxs-lookup"><span data-stu-id="ad77b-105">Cluster By Config (with Specific Subscription Credential) (Default)</span></span>
```
New-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>]
 -Config <AzureHDInsightConfig> -Credential <PSCredential> [-EndPoint <Uri>] [-IgnoreSslErrors <Boolean>]
 -Location <String> -Name <String> [-Subscription <String>] [-Version <String>] [-OSType <OSType>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ad77b-106">이름별 클러스터 (특정 구독 자격 증명 포함)</span><span class="sxs-lookup"><span data-stu-id="ad77b-106">Cluster By Name (with Specific Subscription Credential)</span></span>
```
New-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>]
 -ClusterSizeInNodes <Int32> -Credential <PSCredential> -DefaultStorageAccountKey <String>
 -DefaultStorageAccountName <String> -DefaultStorageContainerName <String> [-EndPoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String> [-Subscription <String>] [-Version <String>]
 [-HeadNodeVMSize <String>] [-ClusterType <ClusterType>] [-VirtualNetworkId <String>] [-SubnetName <String>]
 [-DataNodeVMSize <String>] [-ZookeeperNodeVMSize <String>] [-OSType <OSType>] [-SshCredential <PSCredential>]
 [-SshPublicKey <String>] [-RdpCredential <PSCredential>] [-RdpAccessExpiry <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ad77b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ad77b-107">DESCRIPTION</span></span>
<span data-ttu-id="ad77b-108">이 버전의 Azure PowerShell HDInsight는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="ad77b-109">이러한 cmdlet은 2017 년 1 월 1 일에 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="ad77b-110">최신 버전의 Azure PowerShell HDInsight를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="ad77b-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="ad77b-111">새 HDInsight를 사용 하 여 클러스터를 만드는 방법에 대 한 자세한 내용은 [HDInsight에서 Azure PowerShell ()을 사용 하 여 Linux 기반 클러스터 만들기](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 를 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="ad77b-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="ad77b-112">Azure PowerShell 및 기타 접근 방법을 사용 하 여 작업을 제출 하는 방법에 대 한 자세한 내용은 [HDInsight에서 Hadoop 작업 제출](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ()을 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="ad77b-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="ad77b-113">Azure PowerShell HDInsight에 대 한 참조 정보는 [Azure Hdinsight cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ()을 참조 하세요 https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ad77b-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="ad77b-114">**AzureHDInsightCluster** cmdlet은 지정 된 매개 변수를 사용 하거나 **새-AzureHDInsightClusterConfig** cmdlet을 사용 하 여 만든 구성 개체를 사용 하 여 Azure HDInsight 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-114">The **New-AzureHDInsightCluster** cmdlet creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>

## <span data-ttu-id="ad77b-115">예제의</span><span class="sxs-lookup"><span data-stu-id="ad77b-115">EXAMPLES</span></span>

### <span data-ttu-id="ad77b-116">예제 1: HDInsight 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="ad77b-116">Example 1: Create an HDInsight cluster</span></span>
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
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds
```

<span data-ttu-id="ad77b-117">이 예제에서는 현재 구독에 대 한 HDInsight 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-117">This example creates an HDInsight cluster for the current subscription.</span></span>

<span data-ttu-id="ad77b-118">첫 번째 명령은 **AzureSubscription** cmdlet을 사용 하 여 현재 구독 ID를 가져오고 $SubId 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-118">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="ad77b-119">두 번째 및 세 번째 명령은 **가져오기-AzureStorageKey** cmdlet을 사용 하 여 MyBlobStorage 및 MySecondBlobStorage에 대 한 기본 저장소 키를 얻은 다음 키를 각각 $Key 1 및 $Key 2 개의 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-119">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="ad77b-120">네 번째, 다섯 번째 및 여섯 번째 명령은 Oozie 및 Hive에 대 한 자격 증명을 가져오기 위해 **get-Credential** cmdlet을 사용 하 고 자격 증명을 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-120">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="ad77b-121">마지막 명령은 다음 cmdlet을 사용 하 여 일련의 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-121">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="ad77b-122">**AzureHDInsightClusterConfig-** HDInsight 클러스터 구성을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-122">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="ad77b-123">**Set-AzureHDInsightDefaultStorage-** 구성에 대 한 기본 저장소 계정을 MyBlobStorage.blob.core.windows.net으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-123">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="ad77b-124">**추가-AzureHDInsightStorage** MySecondBlobStorage.blob.core.windows.net 라는 두 번째 저장소 계정을 구성에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-124">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="ad77b-125">**Add-AzureHDInsightMetastore** 를 추가 하 여 Oozie의 Metastore 및 Hive에 대 한 metastore를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-125">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="ad77b-126">**AzureHDInsightCluster** 새 구성으로 HDInsight 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-126">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="ad77b-127">변수</span><span class="sxs-lookup"><span data-stu-id="ad77b-127">PARAMETERS</span></span>

### <span data-ttu-id="ad77b-128">-인증서</span><span class="sxs-lookup"><span data-stu-id="ad77b-128">-Certificate</span></span>
<span data-ttu-id="ad77b-129">Azure 구독에 대 한 관리 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-129">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad77b-130">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="ad77b-130">-ClusterSizeInNodes</span></span>
<span data-ttu-id="ad77b-131">클러스터에 대해 만들 데이터 노드 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-131">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Nodes, Size

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad77b-132">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="ad77b-132">-ClusterType</span></span>
<span data-ttu-id="ad77b-133">만들 클러스터 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-133">Specifies the type of cluster to create.</span></span>

```yaml
Type: ClusterType
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad77b-134">-구성</span><span class="sxs-lookup"><span data-stu-id="ad77b-134">-Config</span></span>
<span data-ttu-id="ad77b-135">**새 AzureHDInsightClusterConfig** cmdlet을 사용 하 여 만든 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-135">Specifies a configuration object that is created by using the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: Cluster By Config (with Specific Subscription Credential)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad77b-136">-Credential</span><span class="sxs-lookup"><span data-stu-id="ad77b-136">-Credential</span></span>
<span data-ttu-id="ad77b-137">Hadoop 클러스터에 원격으로 액세스 하는 데 사용 되는 기본 계정에 사용할 HDInsight에 대 한 사용자 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-137">Specifies the user credentials for HDInsight to use for the default account that is used to remotely access a Hadoop cluster.</span></span>
<span data-ttu-id="ad77b-138">이러한 자격 증명은 사용자의 구독 자격 증명과는 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-138">These credentials are distinct from the subscription credentials of the user.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: Cred

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad77b-139">-DataNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="ad77b-139">-DataNodeVMSize</span></span>
<span data-ttu-id="ad77b-140">데이터 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-140">Specifies the size of the virtual machine for the data node.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad77b-141">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ad77b-141">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="ad77b-142">HDInsight 클러스터에서 사용 하는 기본 저장소 계정에 대 한 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-142">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad77b-143">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ad77b-143">-DefaultStorageAccountName</span></span>
<span data-ttu-id="ad77b-144">HDInsight 클러스터에서 사용 하는 기본 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-144">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad77b-145">-DefaultStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="ad77b-145">-DefaultStorageContainerName</span></span>
<span data-ttu-id="ad77b-146">HDInsight 클러스터에서 사용 하는 기본 Azure 저장소 계정에서 기본 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-146">Specifies the name of the default container in the default Azure storage account that an HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad77b-147">-끝점</span><span class="sxs-lookup"><span data-stu-id="ad77b-147">-EndPoint</span></span>
<span data-ttu-id="ad77b-148">Azure에 연결 하는 데 사용할 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-148">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="ad77b-149">이 매개 변수를 지정 하지 않으면이 cmdlet은 기본 끝점을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-149">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad77b-150">-인원 용 Nodevmsize</span><span class="sxs-lookup"><span data-stu-id="ad77b-150">-HeadNodeVMSize</span></span>
<span data-ttu-id="ad77b-151">헤드 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-151">Specifies the size of the virtual machine for the head node.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad77b-152">-HostedService</span><span class="sxs-lookup"><span data-stu-id="ad77b-152">-HostedService</span></span>
<span data-ttu-id="ad77b-153">HDInsight 서비스의 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-153">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="ad77b-154">이 매개 변수를 지정 하지 않으면이 cmdlet은 기본 네임 스페이스를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-154">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad77b-155">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="ad77b-155">-IgnoreSslErrors</span></span>
<span data-ttu-id="ad77b-156">SSL (Secure Sockets Layer) 오류가 무시 되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-156">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad77b-157">-위치</span><span class="sxs-lookup"><span data-stu-id="ad77b-157">-Location</span></span>
<span data-ttu-id="ad77b-158">HDInsight 클러스터를 만들 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-158">Specifies the region in which to create an HDInsight cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Loc

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad77b-159">-이름</span><span class="sxs-lookup"><span data-stu-id="ad77b-159">-Name</span></span>
<span data-ttu-id="ad77b-160">만들 Azure HDInsight 클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-160">Specifies the name of the Azure HDInsight cluster to create.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Config (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad77b-161">-OSType</span><span class="sxs-lookup"><span data-stu-id="ad77b-161">-OSType</span></span>
<span data-ttu-id="ad77b-162">클러스터의 운영 체제를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-162">Specifies the operating system for a cluster.</span></span>

```yaml
Type: OSType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad77b-163">-프로필</span><span class="sxs-lookup"><span data-stu-id="ad77b-163">-Profile</span></span>
<span data-ttu-id="ad77b-164">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-164">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ad77b-165">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-165">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ad77b-166">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="ad77b-166">-RdpAccessExpiry</span></span>
<span data-ttu-id="ad77b-167">클러스터에 대 한 RDP (원격 데스크톱 프로토콜) 액세스에 대 한 만료 **날짜를 DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-167">Specifies the expiration, as a **DateTime** object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad77b-168">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="ad77b-168">-RdpCredential</span></span>
<span data-ttu-id="ad77b-169">클러스터에 대 한 RDP 액세스에 대 한 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-169">Specifies the credentials for RDP access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad77b-170">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="ad77b-170">-SshCredential</span></span>
<span data-ttu-id="ad77b-171">HDInsight 클러스터에 대 한 보안 셸 (SSH) 사용자 이름 및 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-171">Specifies the Secure Shell (SSH) user name and password for the HDInsight cluster.</span></span>
<span data-ttu-id="ad77b-172">이 매개 변수는 Linux 클러스터에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-172">This parameter is valid only for Linux clusters.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad77b-173">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="ad77b-173">-SshPublicKey</span></span>
<span data-ttu-id="ad77b-174">HDInsight 클러스터에 대 한 SSH 공개 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-174">Specifies the SSH public key for an HDInsight cluster.</span></span>
<span data-ttu-id="ad77b-175">이 매개 변수는 Linux 클러스터에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-175">This parameter is valid only for Linux clusters.</span></span>

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

### <span data-ttu-id="ad77b-176">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="ad77b-176">-SubnetName</span></span>
<span data-ttu-id="ad77b-177">서브넷의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-177">Specifies the name of a subnet.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad77b-178">-구독</span><span class="sxs-lookup"><span data-stu-id="ad77b-178">-Subscription</span></span>
<span data-ttu-id="ad77b-179">HDInsight 클러스터를 만들 Azure 구독을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-179">Specifies the Azure subscription in which to create an HDInsight cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad77b-180">-버전</span><span class="sxs-lookup"><span data-stu-id="ad77b-180">-Version</span></span>
<span data-ttu-id="ad77b-181">만들 HDInsight 클러스터 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-181">Specifies the HDInsight cluster version to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Ver

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad77b-182">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="ad77b-182">-VirtualNetworkId</span></span>
<span data-ttu-id="ad77b-183">클러스터를 프로 비전 할 가상 네트워크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-183">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad77b-184">-ZookeeperNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="ad77b-184">-ZookeeperNodeVMSize</span></span>
<span data-ttu-id="ad77b-185">사육 사 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-185">Specifies the size of the virtual machine for the ZooKeeper node.</span></span>
<span data-ttu-id="ad77b-186">이 매개 변수는 HBase 또는 폭풍 클러스터에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-186">This parameter is valid only for HBase or Storm clusters.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad77b-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad77b-187">CommonParameters</span></span>
<span data-ttu-id="ad77b-188">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad77b-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad77b-189">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad77b-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad77b-190">입력</span><span class="sxs-lookup"><span data-stu-id="ad77b-190">INPUTS</span></span>

## <span data-ttu-id="ad77b-191">출력</span><span class="sxs-lookup"><span data-stu-id="ad77b-191">OUTPUTS</span></span>

## <span data-ttu-id="ad77b-192">상속자</span><span class="sxs-lookup"><span data-stu-id="ad77b-192">NOTES</span></span>

## <span data-ttu-id="ad77b-193">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad77b-193">RELATED LINKS</span></span>

[<span data-ttu-id="ad77b-194">추가-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="ad77b-194">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="ad77b-195">추가-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="ad77b-195">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="ad77b-196">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ad77b-196">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="ad77b-197">새로운 AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="ad77b-197">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="ad77b-198">제거-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ad77b-198">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)

[<span data-ttu-id="ad77b-199">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="ad77b-199">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)

[<span data-ttu-id="ad77b-200">-AzureHDInsightCluster 사용</span><span class="sxs-lookup"><span data-stu-id="ad77b-200">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


