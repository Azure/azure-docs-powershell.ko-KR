---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
ms.openlocfilehash: bc89dff9fa6feecf38f0d9f81efb3bdc18c70641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711563"
---
# <span data-ttu-id="e07f4-101">New-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e07f4-101">New-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="e07f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e07f4-102">SYNOPSIS</span></span>
<span data-ttu-id="e07f4-103">현재 구독에 대 한 지정 된 리소스 그룹에 Azure HDInsight 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e07f4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e07f4-104">SYNTAX</span></span>

### <span data-ttu-id="e07f4-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e07f4-105">Default (Default)</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificatePassword <String>] [-AadTenantId <Guid>]
 [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e07f4-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="e07f4-106">CertificateFilePath</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e07f4-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="e07f4-107">CertificateFileContents</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e07f4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e07f4-108">DESCRIPTION</span></span>
<span data-ttu-id="e07f4-109">New-AzureHDInsightCluster는 지정 된 매개 변수를 사용 하거나 New-AzureRmHDInsightClusterConfig cmdlet을 사용 하 여 만든 구성 개체를 사용 하 여 Azure HDInsight 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-109">The New-AzureHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="e07f4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e07f4-110">EXAMPLES</span></span>

### <span data-ttu-id="e07f4-111">--------------------------예제 1: Azure HDInsight 클러스터 만들기--------------------------</span><span class="sxs-lookup"><span data-stu-id="e07f4-111">--------------------------  Example 1: Create an Azure HDInsight cluster  --------------------------</span></span>
<span data-ttu-id="e07f4-112">@ {paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="e07f4-112">@{paragraph=PS C:\\\>}</span></span>









```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzureStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        #   New-AzureRMResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzureRmHDInsightCluster `
            -ClusterType Hadoop `
            -OSType Windows `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="e07f4-113">이 명령은 현재 구독에 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-113">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="e07f4-114">변수</span><span class="sxs-lookup"><span data-stu-id="e07f4-114">PARAMETERS</span></span>

### <span data-ttu-id="e07f4-115">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="e07f4-115">-AadTenantId</span></span>
<span data-ttu-id="e07f4-116">Azure Data Lake Store에 액세스할 때 사용 되는 Azure AD 테 넌 트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-116">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07f4-117">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="e07f4-117">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="e07f4-118">클러스터에 대 한 추가 Azure 저장소 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-118">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="e07f4-119">또는 Add-AzureRmHDInsightStorage cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-119">You can alternatively use the Add-AzureRmHDInsightStorage cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07f4-120">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="e07f4-120">-CertificateFileContents</span></span>
<span data-ttu-id="e07f4-121">Azure Data Lake Store에 액세스할 때 사용 될 인증서의 파일 내용을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-121">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: CertificateFileContents
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07f4-122">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="e07f4-122">-CertificateFilePath</span></span>
<span data-ttu-id="e07f4-123">서비스 사용자로 인증 하는 데 사용 되는 인증서의 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-123">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="e07f4-124">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: CertificateFilePath
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07f4-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="e07f4-125">-CertificatePassword</span></span>
<span data-ttu-id="e07f4-126">서비스 사용자로 인증 하는 데 사용 되는 인증서의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-126">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="e07f4-127">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-127">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="e07f4-128">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e07f4-128">-ClusterName</span></span>
<span data-ttu-id="e07f4-129">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-129">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07f4-130">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="e07f4-130">-ClusterSizeInNodes</span></span>
<span data-ttu-id="e07f4-131">클러스터에 대 한 작업자 노드 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-131">Specifies the number of Worker nodes for the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07f4-132">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="e07f4-132">-ClusterTier</span></span>
<span data-ttu-id="e07f4-133">HDInsight 클러스터 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-133">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="e07f4-134">기본적으로이는 표준입니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-134">By default, this is Standard.</span></span>
<span data-ttu-id="e07f4-135">프리미엄 계층은 Linux 클러스터 에서만 사용할 수 있으며, 몇 가지 새로운 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-135">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.Tier
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07f4-136">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="e07f4-136">-ClusterType</span></span>
<span data-ttu-id="e07f4-137">만들 클러스터 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-137">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="e07f4-138">옵션: Hadoop, HBase, 폭풍, Spark</span><span class="sxs-lookup"><span data-stu-id="e07f4-138">Options are: Hadoop, HBase, Storm, Spark</span></span>

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

### <span data-ttu-id="e07f4-139">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="e07f4-139">-ComponentVersion</span></span>
```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07f4-140">-구성</span><span class="sxs-lookup"><span data-stu-id="e07f4-140">-Config</span></span>
<span data-ttu-id="e07f4-141">클러스터를 만드는 데 사용할 클러스터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-141">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="e07f4-142">이 개체는 New-AzureRmHDInsightClusterConfig cmdlet을 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-142">This object can be created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e07f4-143">-구성</span><span class="sxs-lookup"><span data-stu-id="e07f4-143">-Configurations</span></span>
<span data-ttu-id="e07f4-144">이 HDInsight 클러스터의 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-144">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="e07f4-145">또는 Add-AzureRmHDInsightConfigValues cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-145">You can alternatively use the Add-AzureRmHDInsightConfigValues cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07f4-146">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e07f4-146">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="e07f4-147">HDInsight 클러스터에서 사용할 기본 Azure 저장소 계정에 대 한 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-147">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="e07f4-148">또는 Set-AzureRmHDInsightDefaultStorage cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-148">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07f4-149">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e07f4-149">-DefaultStorageAccountName</span></span>
<span data-ttu-id="e07f4-150">HDInsight 클러스터에 사용 되는 기본 Azure 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-150">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="e07f4-151">또는 Set-AzureRmHDInsightDefaultStorage cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-151">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07f4-152">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e07f4-152">-DefaultStorageAccountType</span></span>
<span data-ttu-id="e07f4-153">HDInsight 클러스터에 사용 되는 기본 저장소 계정의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-153">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="e07f4-154">사용할 수 있는 값은 AzureStorage 및 AzureDataLakeStore입니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-154">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="e07f4-155">지정 되지 않은 경우 AzureStorage가 기본값으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-155">Defaults to AzureStorage if not specified.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases: 
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07f4-156">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e07f4-156">-DefaultStorageContainer</span></span>
<span data-ttu-id="e07f4-157">HDInsight 클러스터에서 사용할 기본 Azure 저장소 계정에 있는 기본 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-157">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="e07f4-158">또는 Set-AzureRmHDInsightDefaultStorage cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-158">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="e07f4-159">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="e07f4-159">-DefaultStorageRootPath</span></span>
<span data-ttu-id="e07f4-160">HDInsight 클러스터에서 기본 파일 시스템으로 사용할 Data Lake Store 계정에서 경로 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-160">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="e07f4-161">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="e07f4-161">-EdgeNodeSize</span></span>
<span data-ttu-id="e07f4-162">Edge 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-162">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="e07f4-163">허용 되는 VM 크기에 대해 Get-AzureRmVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e07f4-163">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="e07f4-164">이 매개 변수는 RServer 클러스터에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-164">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="e07f4-165">-용 Nodesize</span><span class="sxs-lookup"><span data-stu-id="e07f4-165">-HeadNodeSize</span></span>
<span data-ttu-id="e07f4-166">헤드 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-166">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="e07f4-167">허용 되는 VM 크기에 대해 Get-AzureRmVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e07f4-167">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="e07f4-168">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="e07f4-168">-HiveMetastore</span></span>
<span data-ttu-id="e07f4-169">하이브 메타 데이터를 저장할 SQL 데이터베이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-169">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="e07f4-170">또는 Add-AzureRmHDInsightMetastore cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-170">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07f4-171">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="e07f4-171">-HttpCredential</span></span>
<span data-ttu-id="e07f4-172">클러스터에 대 한 HTTP (클러스터 로그인) 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-172">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07f4-173">-위치</span><span class="sxs-lookup"><span data-stu-id="e07f4-173">-Location</span></span>
<span data-ttu-id="e07f4-174">클러스터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-174">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="e07f4-175">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e07f4-175">-ObjectId</span></span>
<span data-ttu-id="e07f4-176">클러스터를 나타내는 Azure AD 서비스 주체의 Azure AD 개체 ID (GUID)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-176">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="e07f4-177">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-177">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07f4-178">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="e07f4-178">-OozieMetastore</span></span>
<span data-ttu-id="e07f4-179">Oozie 메타 데이터를 저장할 SQL 데이터베이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-179">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="e07f4-180">또는 Add-AzureRmHDInsightMetastore cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-180">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07f4-181">-OSType</span><span class="sxs-lookup"><span data-stu-id="e07f4-181">-OSType</span></span>
<span data-ttu-id="e07f4-182">클러스터의 운영 체제를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-182">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="e07f4-183">옵션: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="e07f4-183">Options are: Windows, Linux</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.OSType
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07f4-184">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="e07f4-184">-RdpAccessExpiry</span></span>
<span data-ttu-id="e07f4-185">클러스터에 대 한 RDP (원격 데스크톱 프로토콜) 액세스에 대 한 만료 날짜를 DateTime 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-185">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07f4-186">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="e07f4-186">-RdpCredential</span></span>
<span data-ttu-id="e07f4-187">클러스터의 RDP (원격 데스크톱) 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-187">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="e07f4-188">이는 Windows 클러스터에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-188">This is only for Windows clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07f4-189">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e07f4-189">-ResourceGroupName</span></span>
<span data-ttu-id="e07f4-190">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-190">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e07f4-191">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="e07f4-191">-ScriptActions</span></span>
<span data-ttu-id="e07f4-192">클러스터 생성이 끝날 때 클러스터에서 실행할 스크립트 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-192">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="e07f4-193">또는 Add-AzureRmHDInsightScriptAction를 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-193">You can alternatively use Add-AzureRmHDInsightScriptAction.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]
Parameter Sets: (All)
Aliases: 
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07f4-194">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="e07f4-194">-SecurityProfile</span></span>
<span data-ttu-id="e07f4-195">보안 클러스터를 만드는 데 사용 되는 보안 관련 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-195">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="e07f4-196">또는 Add-AzureRmHDInsightSecurityProfile cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-196">You can alternatively use the Add-AzureRmHDInsightSecurityProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07f4-197">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="e07f4-197">-SshCredential</span></span>
<span data-ttu-id="e07f4-198">SSH 연결에 사용 되는 SSH 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-198">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="e07f4-199">이는 Linux 용 클러스터에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-199">This is only for Linux clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07f4-200">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="e07f4-200">-SshPublicKey</span></span>
<span data-ttu-id="e07f4-201">SSH 연결에 사용 되는 공개 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-201">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="e07f4-202">이는 Linux 용 클러스터에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-202">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="e07f4-203">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="e07f4-203">-SubnetName</span></span>
<span data-ttu-id="e07f4-204">클러스터에 대해 선택 된 가상 네트워크 내 서브넷의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-204">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="e07f4-205">-버전</span><span class="sxs-lookup"><span data-stu-id="e07f4-205">-Version</span></span>
<span data-ttu-id="e07f4-206">HDInsight 클러스터의 HDI 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-206">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="e07f4-207">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="e07f4-207">-VirtualNetworkId</span></span>
<span data-ttu-id="e07f4-208">클러스터를 프로 비전 할 가상 네트워크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-208">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="e07f4-209">-. 노드 크기</span><span class="sxs-lookup"><span data-stu-id="e07f4-209">-WorkerNodeSize</span></span>
<span data-ttu-id="e07f4-210">작업자 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-210">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="e07f4-211">허용 되는 VM 크기에 대해 Get-AzureRmVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e07f4-211">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="e07f4-212">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="e07f4-212">-ZookeeperNodeSize</span></span>
<span data-ttu-id="e07f4-213">사육 사 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-213">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="e07f4-214">허용 되는 VM 크기에 대해 Get-AzureRmVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e07f4-214">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="e07f4-215">이 매개 변수는 HBase 또는 폭풍 클러스터에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-215">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="e07f4-216">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e07f4-216">-DefaultProfile</span></span>
<span data-ttu-id="e07f4-217">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-217">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07f4-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e07f4-218">CommonParameters</span></span>
<span data-ttu-id="e07f4-219">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e07f4-220">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e07f4-220">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e07f4-221">입력</span><span class="sxs-lookup"><span data-stu-id="e07f4-221">INPUTS</span></span>

### <span data-ttu-id="e07f4-222">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="e07f4-222">AzureHDInsightConfig</span></span>
<span data-ttu-id="e07f4-223">' Config ' 매개 변수는 파이프라인에서 ' AzureHDInsightConfig ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e07f4-223">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="e07f4-224">출력</span><span class="sxs-lookup"><span data-stu-id="e07f4-224">OUTPUTS</span></span>

### <span data-ttu-id="e07f4-225">AzureHDInsightCluster의. m m.</span><span class="sxs-lookup"><span data-stu-id="e07f4-225">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="e07f4-226">상속자</span><span class="sxs-lookup"><span data-stu-id="e07f4-226">NOTES</span></span>
<span data-ttu-id="e07f4-227">키워드: azure, azurerm, arm, resource, 관리, 관리자, hadoop, hdinsight, hd, 통찰력</span><span class="sxs-lookup"><span data-stu-id="e07f4-227">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="e07f4-228">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e07f4-228">RELATED LINKS</span></span>

[<span data-ttu-id="e07f4-229">새로운 AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="e07f4-229">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)

