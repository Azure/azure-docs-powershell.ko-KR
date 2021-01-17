---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: f4592a371e528c7779e07251bf79677dac47e6df
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489599"
---
# <span data-ttu-id="7edd0-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="7edd0-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="7edd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7edd0-102">SYNOPSIS</span></span>
<span data-ttu-id="7edd0-103">현재 구독에 대해 지정된 리소스 그룹에 Azure HDInsight 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="7edd0-104">구문</span><span class="sxs-lookup"><span data-stu-id="7edd0-104">SYNTAX</span></span>

### <span data-ttu-id="7edd0-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="7edd0-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AmbariDatabase <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-StorageContainer <String>] [-StorageRootPath <String>] [-StorageFileSystem <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>]
 [-KafkaManagementNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificatePassword <String>]
 [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>] [-StorageAccountManagedIdentity <String>]
 [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>]
 [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-EnableIDBroker] [-KafkaClientGroupId <String>]
 [-KafkaClientGroupName <String>] [-ResourceProviderConnection <String>] [-PrivateLink <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7edd0-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="7edd0-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AmbariDatabase <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-StorageContainer <String>] [-StorageRootPath <String>] [-StorageFileSystem <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>]
 [-KafkaManagementNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-StorageAccountManagedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-EnableIDBroker]
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-ResourceProviderConnection <String>]
 [-PrivateLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7edd0-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="7edd0-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AmbariDatabase <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-StorageContainer <String>] [-StorageRootPath <String>] [-StorageFileSystem <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>]
 [-KafkaManagementNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-StorageAccountManagedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-EnableIDBroker]
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-ResourceProviderConnection <String>]
 [-PrivateLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7edd0-108">설명</span><span class="sxs-lookup"><span data-stu-id="7edd0-108">DESCRIPTION</span></span>
<span data-ttu-id="7edd0-109">이 New-AzHDInsightCluster 지정된 매개 변수를 사용하여 또는 New-AzHDInsightClusterConfig cmdlet을 사용하여 만든 구성 개체를 사용하여 Azure HDInsight 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="7edd0-110">예제</span><span class="sxs-lookup"><span data-stu-id="7edd0-110">EXAMPLES</span></span>

### <span data-ttu-id="7edd0-111">예제 1: Azure HDInsight 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="7edd0-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
```

<span data-ttu-id="7edd0-112">이 명령은 현재 구독에 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="7edd0-113">예제 2: 고객 관리 키 디스크 암호화를 사용하여 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="7edd0-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-cmk-cluster"
        $clusterCreds = Get-Credential

        # Customer-managed Key info
        $assignedIdentity = "your-ami-resource-id"
        $encryptionKeyName = "new-key"
        $encryptionVaultUri = "https://MyKeyVault.vault.azure.net"
        $encryptionKeyVersion = "00000000000000000000000000000000"

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Spark `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AssignedIdentity $assignedIdentity `
            -EncryptionKeyName $encryptionKeyName `
            -EncryptionVaultUri $encryptionVaultUri `
            -EncryptionKeyVersion $encryptionKeyVersion
```

### <span data-ttu-id="7edd0-114">예제 3: 전송 중 암호화를 사용할 수 있는 Azure HDInsight 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="7edd0-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionInTransit $true `
```

### <span data-ttu-id="7edd0-115">예제 4: 릴레이 아웃바운드 및 개인 링크 기능을 사용하여 Azure HDInsight 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="7edd0-115">Example 4: Create an Azure HDInsight cluster with relay outbound and private link feature</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Virtual network info
        $virtualNetworkId="yourvnetresourceid"
        $subnetName="yoursubnetname"

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -VirtualNetworkId $virtualNetworkId -SubnetName $subnetName `
            -ResourceProviderConnection Outbound -PrivateLink Enabled `
```

### <span data-ttu-id="7edd0-116">예제 5: 호스트에서 암호화를 사용할 수 있는 Azure HDInsight 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="7edd0-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionAtHost $true `
```

### <span data-ttu-id="7edd0-117">예제 6: 자동 조정을 사용할 수 있는 Azure HDInsight 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="7edd0-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create autoscale configuration
        $autoscaleConfiguration=New-AzHDInsightClusterAutoscaleConfiguration `
            -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AutoscaleConfiguration $autoscaleConfiguration
```

### <span data-ttu-id="7edd0-118">예제 7: Kafka Rest 프록시를 사용하여 Azure HDInsight 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="7edd0-118">Example 7: Create an Azure HDInsight cluster with Kafka Rest Proxy.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Kafka Rest Proxy configuration info
        $kafkaClientGroupName = "yourclientgroupname"
        $kafkaClientGroupId = "yourclientgroupid"
        $kafkaManagementNodeSize = "Standard_D4_v2"
        $disksPerWorkerNode = 2

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Kafka `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -KafkaClientGroupId  $kafkaClientGroupId -KafkaClientGroupName $kafkaClientGroupName `
            -KafkaManagementNodeSize $kafkaManagementNodeSize -DisksPerWorkerNode $disksPerWorkerNode
```

### <span data-ttu-id="7edd0-119">예제 8: Azure Data Lake Gen2 저장소를 사용하여 Azure HDInsight 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="7edd0-119">Example 8: Create an Azure HDInsight cluster with Azure Data Lake Gen2 storage.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageManagedIdentity = "yourstorageusermanagedidentity"
        $storageFileSystem = "filesystem01"
        $storageAccountType=AzureDataLakeStorageGen2

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 3 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountManagedIdentity $storageManagedIdentity `
            -StorageFileSystem $storageFileSystem `
            -StorageAccountType $storageAccountType `
            -SshCredential $clusterCreds
```

### <span data-ttu-id="7edd0-120">예제 9: ESP(Enterprise Security Package)를 사용하여 Azure HDInsight 클러스터를 만들고 HDInsight ID Broker를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-120">Example 9: Create an Azure HDInsight cluster with Enterprise Security Package(ESP) and Enable HDInsight ID Broker.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountKey = "yourstorageaccountaccesskey"
        $storageContainer = "yourcontainer01"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # ESP configuration
        $domainResourceId = "your Azure AD Domin Service resource id"
        $domainUser = "yourdomainuser"
        $domainPassword = "yourdoaminpasswd"
        $domainPassword = ConvertTo-SecureString $domainPassword -AsPlainText -Force
        $domainCredential = New-Object System.Management.Automation.PSCredential($domainUser, $domainPassword)
        $clusterUserGroupDns = "dominusergroup"
        $ldapUrls = "ldaps://{your domain name}:636"

        $clusterTier = Premium
        $vnetId = "yourvnetid"
        $subnetName = "yoursubnetname"
        $assignedIdentity = "your user managed assigned identity resourcee id"

        #Create security profile
        $config= New-AzHDInsightClusterConfig|Add-AzHDInsightSecurityProfile -DomainResourceId $domainResourceId -DomainUserCredential $domainCredential -LdapsUrls $ldapUrls -ClusterUsersGroupDNs $clusterUserGroupDns

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusteTier $clusterTier `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 3 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -VirtualNetworkId $vnetId -SubnetName $subnetName `
            -AssignedIdentity $assignedIdentity `
            -SecurityProfile $config.SecurityProfile -EnableIDBroker
```

## <span data-ttu-id="7edd0-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7edd0-121">PARAMETERS</span></span>

### <span data-ttu-id="7edd0-122">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="7edd0-122">-AadTenantId</span></span>
<span data-ttu-id="7edd0-123">Azure Data Lake Store에 액세스할 때 사용할 Azure AD 테넌트 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-123">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="7edd0-124">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="7edd0-124">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="7edd0-125">클러스터에 대한 추가 Azure Storage 계정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-125">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="7edd0-126">또는 Add-AzHDInsightStorage cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-126">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="7edd0-127">-AmbariDatabase</span><span class="sxs-lookup"><span data-stu-id="7edd0-127">-AmbariDatabase</span></span>
<span data-ttu-id="7edd0-128">ambari에 대한 데이터베이스를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-128">Gets or sets the database for ambari.</span></span>

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

### <span data-ttu-id="7edd0-129">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7edd0-129">-ApplicationId</span></span>
<span data-ttu-id="7edd0-130">Azure Data Lake에 액세스하기 위한 서비스 주체 애플리케이션 ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-130">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="7edd0-131">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="7edd0-131">-AssignedIdentity</span></span>
<span data-ttu-id="7edd0-132">할당된 ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-132">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="7edd0-133">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="7edd0-133">-AutoscaleConfiguration</span></span>
<span data-ttu-id="7edd0-134">자동 조정 구성을 얻거나 설정</span><span class="sxs-lookup"><span data-stu-id="7edd0-134">Gets or sets the autoscale configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7edd0-135">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="7edd0-135">-CertificateFileContents</span></span>
<span data-ttu-id="7edd0-136">Azure Data Lake Store에 액세스할 때 사용할 인증서의 파일 내용을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-136">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="7edd0-137">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="7edd0-137">-CertificateFilePath</span></span>
<span data-ttu-id="7edd0-138">서비스 주체로 인증하는 데 사용할 인증서의 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-138">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="7edd0-139">클러스터는 Azure Data Lake Store에 액세스할 때 이 기능을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-139">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="7edd0-140">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="7edd0-140">-CertificatePassword</span></span>
<span data-ttu-id="7edd0-141">서비스 주체로 인증하는 데 사용할 인증서의 암호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-141">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="7edd0-142">클러스터는 Azure Data Lake Store에 액세스할 때 이 기능을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-142">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="7edd0-143">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7edd0-143">-ClusterName</span></span>
<span data-ttu-id="7edd0-144">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-144">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="7edd0-145">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="7edd0-145">-ClusterSizeInNodes</span></span>
<span data-ttu-id="7edd0-146">클러스터에 대한 Worker 노드 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-146">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="7edd0-147">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="7edd0-147">-ClusterTier</span></span>
<span data-ttu-id="7edd0-148">HDInsight 클러스터 계층을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-148">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="7edd0-149">기본적으로 표준입니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-149">By default, this is Standard.</span></span>
<span data-ttu-id="7edd0-150">프리미엄 계층은 Linux 클러스터에서만 사용할 수 있으며 몇 가지 새로운 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-150">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="7edd0-151">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="7edd0-151">-ClusterType</span></span>
<span data-ttu-id="7edd0-152">만들 클러스터의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-152">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="7edd0-153">옵션: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka 및 RServer</span><span class="sxs-lookup"><span data-stu-id="7edd0-153">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="7edd0-154">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="7edd0-154">-ComponentVersion</span></span>
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

### <span data-ttu-id="7edd0-155">-Config</span><span class="sxs-lookup"><span data-stu-id="7edd0-155">-Config</span></span>
<span data-ttu-id="7edd0-156">클러스터를 만드는 데 사용할 클러스터 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-156">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="7edd0-157">이 개체는 New-AzHDInsightClusterConfig cmdlet을 사용하여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-157">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="7edd0-158">-Configurations</span><span class="sxs-lookup"><span data-stu-id="7edd0-158">-Configurations</span></span>
<span data-ttu-id="7edd0-159">이 HDInsight 클러스터의 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-159">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="7edd0-160">또는 Add-AzHDInsightConfigValues cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-160">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="7edd0-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7edd0-161">-DefaultProfile</span></span>
<span data-ttu-id="7edd0-162">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7edd0-162">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7edd0-163">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="7edd0-163">-DisksPerWorkerNode</span></span>
<span data-ttu-id="7edd0-164">클러스터의 작업 노드 역할에 대한 디스크 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-164">Specifies the number of disks for worker node role in the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7edd0-165">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="7edd0-165">-EdgeNodeSize</span></span>
<span data-ttu-id="7edd0-166">에지 노드에 대한 가상 머신의 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-166">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="7edd0-167">허용 Get-AzVMSize VM 크기에 대한 자세한 내용은 HDInsight의 가격 책정 페이지를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7edd0-167">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="7edd0-168">이 매개 변수는 RServer 클러스터에만 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-168">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="7edd0-169">-EnableIDBroker</span><span class="sxs-lookup"><span data-stu-id="7edd0-169">-EnableIDBroker</span></span>
<span data-ttu-id="7edd0-170">HDInsight Identity Broker 기능을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-170">Enables HDInsight Identity Broker feature.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7edd0-171">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="7edd0-171">-EncryptionAlgorithm</span></span>
<span data-ttu-id="7edd0-172">암호화 알고리즘을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-172">Gets or sets the encryption algorithm.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA-OAEP-256, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7edd0-173">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="7edd0-173">-EncryptionAtHost</span></span>
<span data-ttu-id="7edd0-174">호스트에서 암호화를 사용할지 여부를 나타내는 플래그를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-174">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7edd0-175">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="7edd0-175">-EncryptionInTransit</span></span>
<span data-ttu-id="7edd0-176">전송 중 암호화를 사용할지 여부를 나타내는 플래그를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-176">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7edd0-177">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="7edd0-177">-EncryptionKeyName</span></span>
<span data-ttu-id="7edd0-178">암호화 키 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-178">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="7edd0-179">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="7edd0-179">-EncryptionKeyVersion</span></span>
<span data-ttu-id="7edd0-180">암호화 키 버전을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-180">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="7edd0-181">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="7edd0-181">-EncryptionVaultUri</span></span>
<span data-ttu-id="7edd0-182">암호화 자격 증명 모음 URI를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-182">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="7edd0-183">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="7edd0-183">-HeadNodeSize</span></span>
<span data-ttu-id="7edd0-184">헤드 노드에 대한 가상 머신의 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-184">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="7edd0-185">허용 Get-AzVMSize VM 크기에 대한 자세한 내용은 HDInsight의 가격 책정 페이지를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7edd0-185">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="7edd0-186">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="7edd0-186">-HiveMetastore</span></span>
<span data-ttu-id="7edd0-187">Hive 메타데이터를 SQL 데이터베이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-187">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="7edd0-188">또는 Add-AzHDInsightMetastore cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-188">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="7edd0-189">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="7edd0-189">-HttpCredential</span></span>
<span data-ttu-id="7edd0-190">클러스터에 대한 클러스터 로그인(HTTP) 자격 증명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-190">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="7edd0-191">-KafkaClientGroupId</span><span class="sxs-lookup"><span data-stu-id="7edd0-191">-KafkaClientGroupId</span></span>
<span data-ttu-id="7edd0-192">Kafka Rest 프록시 액세스에 대한 클라이언트 그룹 ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-192">Gets or sets the client group id for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="7edd0-193">-KafkaClientGroupName</span><span class="sxs-lookup"><span data-stu-id="7edd0-193">-KafkaClientGroupName</span></span>
<span data-ttu-id="7edd0-194">Kafka Rest 프록시 액세스에 대한 클라이언트 그룹 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-194">Gets or sets the client group name for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="7edd0-195">-KafkaManagementNodeSize</span><span class="sxs-lookup"><span data-stu-id="7edd0-195">-KafkaManagementNodeSize</span></span>
<span data-ttu-id="7edd0-196">Kafka 관리 노드의 크기를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-196">Gets or sets the size of the Kafka Management Node.</span></span>

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

### <span data-ttu-id="7edd0-197">-Location</span><span class="sxs-lookup"><span data-stu-id="7edd0-197">-Location</span></span>
<span data-ttu-id="7edd0-198">클러스터의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-198">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="7edd0-199">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="7edd0-199">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="7edd0-200">지원되는 최소 TLS 버전을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-200">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="7edd0-201">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7edd0-201">-ObjectId</span></span>
<span data-ttu-id="7edd0-202">클러스터를 나타내는 Azure AD 서비스 주체의 Azure AD 개체 ID(GUID)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-202">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="7edd0-203">클러스터는 Azure Data Lake Store에 액세스할 때 이 기능을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-203">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="7edd0-204">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="7edd0-204">-OozieMetastore</span></span>
<span data-ttu-id="7edd0-205">Oozie 메타데이터를 SQL 데이터베이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-205">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="7edd0-206">또는 Add-AzHDInsightMetastore cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-206">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="7edd0-207">-OSType</span><span class="sxs-lookup"><span data-stu-id="7edd0-207">-OSType</span></span>
<span data-ttu-id="7edd0-208">클러스터의 운영 체제를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-208">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="7edd0-209">옵션: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="7edd0-209">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="7edd0-210">-PrivateLink</span><span class="sxs-lookup"><span data-stu-id="7edd0-210">-PrivateLink</span></span>
<span data-ttu-id="7edd0-211">개인 링크 형식을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-211">Gets or sets the private link type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7edd0-212">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="7edd0-212">-RdpAccessExpiry</span></span>
<span data-ttu-id="7edd0-213">클러스터에 대한 RDP(원격 데스크톱 프로토콜) 액세스에 대한 만료를 DateTime 개체로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-213">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="7edd0-214">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="7edd0-214">-RdpCredential</span></span>
<span data-ttu-id="7edd0-215">클러스터에 대한 RDP(원격 데스크톱) 자격 증명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-215">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="7edd0-216">이는 Windows 클러스터에만 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-216">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="7edd0-217">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7edd0-217">-ResourceGroupName</span></span>
<span data-ttu-id="7edd0-218">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-218">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7edd0-219">-ResourceProviderConnection</span><span class="sxs-lookup"><span data-stu-id="7edd0-219">-ResourceProviderConnection</span></span>
<span data-ttu-id="7edd0-220">리소스 공급자 연결 형식을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-220">Gets or sets the resource provider connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7edd0-221">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="7edd0-221">-ScriptActions</span></span>
<span data-ttu-id="7edd0-222">클러스터 만들기가 끝날 때 클러스터에서 실행할 스크립트 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-222">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="7edd0-223">또는 Add-AzHDInsightScriptAction을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-223">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="7edd0-224">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="7edd0-224">-SecurityProfile</span></span>
<span data-ttu-id="7edd0-225">보안 클러스터를 만드는 데 사용되는 보안 관련 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-225">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="7edd0-226">또는 Add-AzHDInsightSecurityProfile cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-226">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="7edd0-227">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="7edd0-227">-SshCredential</span></span>
<span data-ttu-id="7edd0-228">SSH 연결에 사용할 SSH 자격 증명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-228">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="7edd0-229">Linux 클러스터에만 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-229">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="7edd0-230">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="7edd0-230">-SshPublicKey</span></span>
<span data-ttu-id="7edd0-231">SSH 연결에 사용할 공개 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-231">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="7edd0-232">Linux 클러스터에만 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-232">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="7edd0-233">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7edd0-233">-StorageAccountKey</span></span>
<span data-ttu-id="7edd0-234">Storage 계정에 대한 Storage 계정 액세스 키를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-234">Gets or sets the Storage Account Access Key for the Storage Account.</span></span>

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

### <span data-ttu-id="7edd0-235">-StorageAccountManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="7edd0-235">-StorageAccountManagedIdentity</span></span>
<span data-ttu-id="7edd0-236">저장소 계정 관리 ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-236">Gets or sets the storage account managed identity.</span></span>

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

### <span data-ttu-id="7edd0-237">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="7edd0-237">-StorageAccountResourceId</span></span>
<span data-ttu-id="7edd0-238">Storage 계정에 대한 저장소 리소스 ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-238">Gets or sets the Storage Resource Id for the Storage Account.</span></span>

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

### <span data-ttu-id="7edd0-239">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="7edd0-239">-StorageAccountType</span></span>
<span data-ttu-id="7edd0-240">저장소 계정의 형식을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-240">Gets or sets the type of the storage account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7edd0-241">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="7edd0-241">-StorageContainer</span></span>
<span data-ttu-id="7edd0-242">기본 Azure Storage 계정에 대한 StorageContainer 이름을 얻거나 설정</span><span class="sxs-lookup"><span data-stu-id="7edd0-242">Gets or sets the StorageContainer name for the default Azure Storage Account</span></span>

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

### <span data-ttu-id="7edd0-243">-StorageFileSystem</span><span class="sxs-lookup"><span data-stu-id="7edd0-243">-StorageFileSystem</span></span>
<span data-ttu-id="7edd0-244">기본 Azure Data Lake Storage Gen2 계정에 대한 파일 시스템을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-244">Gets or sets the file system for the default Azure Data Lake Storage Gen2 account.</span></span>

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

### <span data-ttu-id="7edd0-245">-StorageRootPath</span><span class="sxs-lookup"><span data-stu-id="7edd0-245">-StorageRootPath</span></span>
<span data-ttu-id="7edd0-246">기본 Data Lake Store 계정에서 클러스터의 루트 경로를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-246">Gets or sets the path to the root of the cluster in the default Data Lake Store Account.</span></span>

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

### <span data-ttu-id="7edd0-247">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="7edd0-247">-SubnetName</span></span>
<span data-ttu-id="7edd0-248">이 HDInsight 클러스터에 대한 서브넷 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-248">Gets or sets the subnet name for this HDInsight cluster.</span></span>

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

### <span data-ttu-id="7edd0-249">-Version</span><span class="sxs-lookup"><span data-stu-id="7edd0-249">-Version</span></span>
<span data-ttu-id="7edd0-250">HDInsight 클러스터의 HDI 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-250">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="7edd0-251">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="7edd0-251">-VirtualNetworkId</span></span>
<span data-ttu-id="7edd0-252">클러스터를 프로비전할 가상 네트워크의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-252">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="7edd0-253">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="7edd0-253">-WorkerNodeSize</span></span>
<span data-ttu-id="7edd0-254">Worker 노드에 대한 가상 머신의 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-254">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="7edd0-255">허용 Get-AzVMSize VM 크기에 대한 자세한 내용은 HDInsight의 가격 책정 페이지를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7edd0-255">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="7edd0-256">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="7edd0-256">-ZookeeperNodeSize</span></span>
<span data-ttu-id="7edd0-257">Zookeeper 노드에 대한 가상 머신의 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-257">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="7edd0-258">허용 Get-AzVMSize VM 크기에 대한 자세한 내용은 HDInsight의 가격 책정 페이지를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7edd0-258">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="7edd0-259">이 매개 변수는 HBase 또는 Storm 클러스터에만 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-259">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="7edd0-260">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7edd0-260">CommonParameters</span></span>
<span data-ttu-id="7edd0-261">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7edd0-261">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7edd0-262">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7edd0-262">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7edd0-263">입력</span><span class="sxs-lookup"><span data-stu-id="7edd0-263">INPUTS</span></span>

### <span data-ttu-id="7edd0-264">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="7edd0-264">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="7edd0-265">출력</span><span class="sxs-lookup"><span data-stu-id="7edd0-265">OUTPUTS</span></span>

### <span data-ttu-id="7edd0-266">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="7edd0-266">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="7edd0-267">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7edd0-267">NOTES</span></span>
<span data-ttu-id="7edd0-268">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, hadoop, hdinsight, hd, insight</span><span class="sxs-lookup"><span data-stu-id="7edd0-268">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="7edd0-269">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7edd0-269">RELATED LINKS</span></span>

[<span data-ttu-id="7edd0-270">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="7edd0-270">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

