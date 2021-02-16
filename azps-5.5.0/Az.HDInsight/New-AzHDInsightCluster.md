---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: d4353e49c72f280ee89a1861682ab5d7c3061a9c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200276"
---
# <span data-ttu-id="4ad24-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4ad24-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="4ad24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ad24-102">SYNOPSIS</span></span>
<span data-ttu-id="4ad24-103">현재 구독에 대해 지정된 리소스 그룹에 Azure HDInsight 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="4ad24-104">구문</span><span class="sxs-lookup"><span data-stu-id="4ad24-104">SYNTAX</span></span>

### <span data-ttu-id="4ad24-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="4ad24-105">Default (Default)</span></span>
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
 [-EnableComputeIsolation] [-ComputeIsolationHostSku <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4ad24-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="4ad24-106">CertificateFilePath</span></span>
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
 [-PrivateLink <String>] [-EnableComputeIsolation] [-ComputeIsolationHostSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ad24-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="4ad24-107">CertificateFileContents</span></span>
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
 [-PrivateLink <String>] [-EnableComputeIsolation] [-ComputeIsolationHostSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ad24-108">설명</span><span class="sxs-lookup"><span data-stu-id="4ad24-108">DESCRIPTION</span></span>
<span data-ttu-id="4ad24-109">이 New-AzHDInsightCluster 지정된 매개 변수를 사용하여 또는 New-AzHDInsightClusterConfig cmdlet을 사용하여 만든 구성 개체를 사용하여 Azure HDInsight 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="4ad24-110">예제</span><span class="sxs-lookup"><span data-stu-id="4ad24-110">EXAMPLES</span></span>

### <span data-ttu-id="4ad24-111">예제 1: Azure HDInsight 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="4ad24-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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

<span data-ttu-id="4ad24-112">이 명령은 현재 구독에 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="4ad24-113">예제 2: 고객 관리 키 디스크 암호화를 사용하여 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="4ad24-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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

### <span data-ttu-id="4ad24-114">예제 3: 전송 중 암호화를 사용할 수 있는 Azure HDInsight 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="4ad24-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}}
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

### <span data-ttu-id="4ad24-115">예제 4: 릴레이 아웃바운드 및 개인 링크 기능을 사용하여 Azure HDInsight 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="4ad24-115">Example 4: Create an Azure HDInsight cluster with relay outbound and private link feature</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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

### <span data-ttu-id="4ad24-116">예제 5: 호스트에서 암호화를 사용할 수 있는 Azure HDInsight 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="4ad24-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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

### <span data-ttu-id="4ad24-117">예제 6: 자동 조정을 사용할 수 있는 Azure HDInsight 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="4ad24-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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

### <span data-ttu-id="4ad24-118">예제 7: Kafka Rest 프록시를 사용하여 Azure HDInsight 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="4ad24-118">Example 7: Create an Azure HDInsight cluster with Kafka Rest Proxy.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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

### <span data-ttu-id="4ad24-119">예제 8: Azure Data Lake Gen2 저장소를 사용하여 Azure HDInsight 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="4ad24-119">Example 8: Create an Azure HDInsight cluster with Azure Data Lake Gen2 storage.</span></span>
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

### <span data-ttu-id="4ad24-120">예제 9: ESP(Enterprise Security Package)를 사용하여 Azure HDInsight 클러스터를 만들고 HDInsight ID Broker를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-120">Example 9: Create an Azure HDInsight cluster with Enterprise Security Package(ESP) and Enable HDInsight ID Broker.</span></span>
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

### <span data-ttu-id="4ad24-121">예제 10: 계산을 사용할 수 있는 Azure HDInsight 클러스터를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-121">Example 10: Create an Azure HDInsight cluster which enables compute isolation.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential
        $workerNodeSize="Standard_E16S_V3" # here is just an example
        $headNodeSize="Standard_E8S_V3"
        $zookeeperNodeSize="Standard_E2S_V3"

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -WorkerNodeSize $workerNodeSize `
            -HeadNodeSize $headNodeSize `
            -ZookeeperNodeSize $zookeeperNodeSize `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EnableComputeIsolation `
```

## <span data-ttu-id="4ad24-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ad24-122">PARAMETERS</span></span>

### <span data-ttu-id="4ad24-123">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="4ad24-123">-AadTenantId</span></span>
<span data-ttu-id="4ad24-124">Azure Data Lake Store에 액세스할 때 사용할 Azure AD 테넌트 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-124">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4ad24-125">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="4ad24-125">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="4ad24-126">클러스터에 대한 추가 Azure Storage 계정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-126">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="4ad24-127">또는 다음 cmdlet을 Add-AzHDInsightStorage 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-127">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="4ad24-128">-AmbariDatabase</span><span class="sxs-lookup"><span data-stu-id="4ad24-128">-AmbariDatabase</span></span>
<span data-ttu-id="4ad24-129">ambari에 대한 데이터베이스를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-129">Gets or sets the database for ambari.</span></span>

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

### <span data-ttu-id="4ad24-130">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="4ad24-130">-ApplicationId</span></span>
<span data-ttu-id="4ad24-131">Azure Data Lake에 액세스하기 위한 서비스 주체 애플리케이션 ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-131">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="4ad24-132">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4ad24-132">-AssignedIdentity</span></span>
<span data-ttu-id="4ad24-133">할당된 ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-133">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="4ad24-134">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ad24-134">-AutoscaleConfiguration</span></span>
<span data-ttu-id="4ad24-135">자동 조정 구성을 얻거나 설정</span><span class="sxs-lookup"><span data-stu-id="4ad24-135">Gets or sets the autoscale configuration</span></span>

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

### <span data-ttu-id="4ad24-136">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="4ad24-136">-CertificateFileContents</span></span>
<span data-ttu-id="4ad24-137">Azure Data Lake Store에 액세스할 때 사용할 인증서의 파일 콘텐츠를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-137">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4ad24-138">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="4ad24-138">-CertificateFilePath</span></span>
<span data-ttu-id="4ad24-139">서비스 주체로 인증하는 데 사용할 인증서의 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-139">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="4ad24-140">클러스터는 Azure Data Lake Store에 액세스할 때 이 기능을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-140">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4ad24-141">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="4ad24-141">-CertificatePassword</span></span>
<span data-ttu-id="4ad24-142">서비스 주체로 인증하는 데 사용할 인증서의 암호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-142">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="4ad24-143">클러스터는 Azure Data Lake Store에 액세스할 때 이 기능을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-143">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4ad24-144">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4ad24-144">-ClusterName</span></span>
<span data-ttu-id="4ad24-145">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-145">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="4ad24-146">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="4ad24-146">-ClusterSizeInNodes</span></span>
<span data-ttu-id="4ad24-147">클러스터에 대한 Worker 노드 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-147">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="4ad24-148">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="4ad24-148">-ClusterTier</span></span>
<span data-ttu-id="4ad24-149">HDInsight 클러스터 계층을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-149">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="4ad24-150">기본적으로 표준입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-150">By default, this is Standard.</span></span>
<span data-ttu-id="4ad24-151">프리미엄 계층은 Linux 클러스터에서만 사용할 수 있으며 몇 가지 새로운 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-151">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="4ad24-152">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="4ad24-152">-ClusterType</span></span>
<span data-ttu-id="4ad24-153">만들 클러스터의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-153">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="4ad24-154">옵션: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka 및 RServer</span><span class="sxs-lookup"><span data-stu-id="4ad24-154">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="4ad24-155">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="4ad24-155">-ComponentVersion</span></span>
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

### <span data-ttu-id="4ad24-156">-ComputeIsolationHostSku</span><span class="sxs-lookup"><span data-stu-id="4ad24-156">-ComputeIsolationHostSku</span></span>
<span data-ttu-id="4ad24-157">계산을 위한 전용 호스트 SKU를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-157">Gets or sets the dedicated host sku for compute isolation.</span></span>

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

### <span data-ttu-id="4ad24-158">-Config</span><span class="sxs-lookup"><span data-stu-id="4ad24-158">-Config</span></span>
<span data-ttu-id="4ad24-159">클러스터를 만드는 데 사용할 클러스터 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-159">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="4ad24-160">이 개체는 New-AzHDInsightClusterConfig cmdlet을 사용하여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-160">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="4ad24-161">-Configurations</span><span class="sxs-lookup"><span data-stu-id="4ad24-161">-Configurations</span></span>
<span data-ttu-id="4ad24-162">이 HDInsight 클러스터의 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-162">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="4ad24-163">또는 다음 cmdlet을 Add-AzHDInsightConfigValues 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-163">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="4ad24-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ad24-164">-DefaultProfile</span></span>
<span data-ttu-id="4ad24-165">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4ad24-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ad24-166">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="4ad24-166">-DisksPerWorkerNode</span></span>
<span data-ttu-id="4ad24-167">클러스터의 작업 노드 역할에 대한 디스크 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-167">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="4ad24-168">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="4ad24-168">-EdgeNodeSize</span></span>
<span data-ttu-id="4ad24-169">에지 노드에 대한 가상 머신의 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-169">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="4ad24-170">허용 Get-AzVMSize VM 크기에 대한 자세한 내용은 HDInsight의 가격 책정 페이지를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4ad24-170">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="4ad24-171">이 매개 변수는 RServer 클러스터에만 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-171">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="4ad24-172">-EnableComputeIsolation</span><span class="sxs-lookup"><span data-stu-id="4ad24-172">-EnableComputeIsolation</span></span>
<span data-ttu-id="4ad24-173">HDInsight 계산 고리 기능을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-173">Enables HDInsight compute isolation feature.</span></span>

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

### <span data-ttu-id="4ad24-174">-EnableIDBroker</span><span class="sxs-lookup"><span data-stu-id="4ad24-174">-EnableIDBroker</span></span>
<span data-ttu-id="4ad24-175">HDInsight Identity Broker 기능을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-175">Enables HDInsight Identity Broker feature.</span></span>

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

### <span data-ttu-id="4ad24-176">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="4ad24-176">-EncryptionAlgorithm</span></span>
<span data-ttu-id="4ad24-177">암호화 알고리즘을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-177">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="4ad24-178">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="4ad24-178">-EncryptionAtHost</span></span>
<span data-ttu-id="4ad24-179">호스트에서 암호화를 사용할지 여부를 나타내는 플래그를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-179">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="4ad24-180">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="4ad24-180">-EncryptionInTransit</span></span>
<span data-ttu-id="4ad24-181">전송 중 암호화를 사용할지 여부를 나타내는 플래그를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-181">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="4ad24-182">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="4ad24-182">-EncryptionKeyName</span></span>
<span data-ttu-id="4ad24-183">암호화 키 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-183">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="4ad24-184">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="4ad24-184">-EncryptionKeyVersion</span></span>
<span data-ttu-id="4ad24-185">암호화 키 버전을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-185">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="4ad24-186">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="4ad24-186">-EncryptionVaultUri</span></span>
<span data-ttu-id="4ad24-187">암호화 자격 증명 모음 URI를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-187">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="4ad24-188">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="4ad24-188">-HeadNodeSize</span></span>
<span data-ttu-id="4ad24-189">헤드 노드에 대한 가상 머신의 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-189">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="4ad24-190">허용 Get-AzVMSize VM 크기에 대한 자세한 내용은 HDInsight의 가격 책정 페이지를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4ad24-190">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="4ad24-191">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="4ad24-191">-HiveMetastore</span></span>
<span data-ttu-id="4ad24-192">Hive 메타데이터를 SQL 데이터베이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-192">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="4ad24-193">또는 다음 cmdlet을 Add-AzHDInsightMetastore 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-193">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="4ad24-194">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="4ad24-194">-HttpCredential</span></span>
<span data-ttu-id="4ad24-195">클러스터에 대한 클러스터 로그인(HTTP) 자격 증명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-195">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="4ad24-196">-KafkaClientGroupId</span><span class="sxs-lookup"><span data-stu-id="4ad24-196">-KafkaClientGroupId</span></span>
<span data-ttu-id="4ad24-197">Kafka Rest 프록시 액세스에 대한 클라이언트 그룹 ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-197">Gets or sets the client group id for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="4ad24-198">-KafkaClientGroupName</span><span class="sxs-lookup"><span data-stu-id="4ad24-198">-KafkaClientGroupName</span></span>
<span data-ttu-id="4ad24-199">Kafka Rest 프록시 액세스에 대한 클라이언트 그룹 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-199">Gets or sets the client group name for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="4ad24-200">-KafkaManagementNodeSize</span><span class="sxs-lookup"><span data-stu-id="4ad24-200">-KafkaManagementNodeSize</span></span>
<span data-ttu-id="4ad24-201">Kafka 관리 노드의 크기를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-201">Gets or sets the size of the Kafka Management Node.</span></span>

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

### <span data-ttu-id="4ad24-202">-Location</span><span class="sxs-lookup"><span data-stu-id="4ad24-202">-Location</span></span>
<span data-ttu-id="4ad24-203">클러스터의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-203">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="4ad24-204">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="4ad24-204">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="4ad24-205">지원되는 최소 TLS 버전을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-205">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="4ad24-206">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4ad24-206">-ObjectId</span></span>
<span data-ttu-id="4ad24-207">클러스터를 나타내는 Azure AD 서비스 주체의 Azure AD 개체 ID(GUID)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-207">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="4ad24-208">클러스터는 Azure Data Lake Store에 액세스할 때 이 기능을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-208">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4ad24-209">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="4ad24-209">-OozieMetastore</span></span>
<span data-ttu-id="4ad24-210">Oozie 메타데이터를 SQL 데이터베이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-210">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="4ad24-211">또는 다음 cmdlet을 Add-AzHDInsightMetastore 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-211">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="4ad24-212">-OSType</span><span class="sxs-lookup"><span data-stu-id="4ad24-212">-OSType</span></span>
<span data-ttu-id="4ad24-213">클러스터의 운영 체제를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-213">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="4ad24-214">옵션: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="4ad24-214">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="4ad24-215">-PrivateLink</span><span class="sxs-lookup"><span data-stu-id="4ad24-215">-PrivateLink</span></span>
<span data-ttu-id="4ad24-216">개인 링크 형식을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-216">Gets or sets the private link type.</span></span>

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

### <span data-ttu-id="4ad24-217">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="4ad24-217">-RdpAccessExpiry</span></span>
<span data-ttu-id="4ad24-218">클러스터에 대한 RDP(원격 데스크톱 프로토콜) 액세스에 대한 만료를 DateTime 개체로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-218">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="4ad24-219">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="4ad24-219">-RdpCredential</span></span>
<span data-ttu-id="4ad24-220">클러스터에 대한 RDP(원격 데스크톱) 자격 증명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-220">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="4ad24-221">이는 Windows 클러스터에만 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-221">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="4ad24-222">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ad24-222">-ResourceGroupName</span></span>
<span data-ttu-id="4ad24-223">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-223">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4ad24-224">-ResourceProviderConnection</span><span class="sxs-lookup"><span data-stu-id="4ad24-224">-ResourceProviderConnection</span></span>
<span data-ttu-id="4ad24-225">리소스 공급자 연결 형식을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-225">Gets or sets the resource provider connection type.</span></span>

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

### <span data-ttu-id="4ad24-226">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="4ad24-226">-ScriptActions</span></span>
<span data-ttu-id="4ad24-227">클러스터 만들기가 끝날 때 클러스터에서 실행할 스크립트 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-227">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="4ad24-228">또는 Add-AzHDInsightScriptAction을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-228">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="4ad24-229">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="4ad24-229">-SecurityProfile</span></span>
<span data-ttu-id="4ad24-230">보안 클러스터를 만드는 데 사용되는 보안 관련 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-230">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="4ad24-231">또는 다음 cmdlet을 Add-AzHDInsightSecurityProfile 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-231">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="4ad24-232">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="4ad24-232">-SshCredential</span></span>
<span data-ttu-id="4ad24-233">SSH 연결에 사용할 SSH 자격 증명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-233">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="4ad24-234">Linux 클러스터에만 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-234">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="4ad24-235">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="4ad24-235">-SshPublicKey</span></span>
<span data-ttu-id="4ad24-236">SSH 연결에 사용할 공개 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-236">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="4ad24-237">Linux 클러스터에만 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-237">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="4ad24-238">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4ad24-238">-StorageAccountKey</span></span>
<span data-ttu-id="4ad24-239">Storage 계정에 대한 Storage 계정 액세스 키를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-239">Gets or sets the Storage Account Access Key for the Storage Account.</span></span>

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

### <span data-ttu-id="4ad24-240">-StorageAccountManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="4ad24-240">-StorageAccountManagedIdentity</span></span>
<span data-ttu-id="4ad24-241">저장소 계정 관리 ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-241">Gets or sets the storage account managed identity.</span></span>

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

### <span data-ttu-id="4ad24-242">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="4ad24-242">-StorageAccountResourceId</span></span>
<span data-ttu-id="4ad24-243">Storage 계정에 대한 저장소 리소스 ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-243">Gets or sets the Storage Resource Id for the Storage Account.</span></span>

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

### <span data-ttu-id="4ad24-244">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="4ad24-244">-StorageAccountType</span></span>
<span data-ttu-id="4ad24-245">저장소 계정의 형식을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-245">Gets or sets the type of the storage account.</span></span>

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

### <span data-ttu-id="4ad24-246">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="4ad24-246">-StorageContainer</span></span>
<span data-ttu-id="4ad24-247">기본 Azure Storage 계정에 대한 StorageContainer 이름을 얻거나 설정</span><span class="sxs-lookup"><span data-stu-id="4ad24-247">Gets or sets the StorageContainer name for the default Azure Storage Account</span></span>

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

### <span data-ttu-id="4ad24-248">-StorageFileSystem</span><span class="sxs-lookup"><span data-stu-id="4ad24-248">-StorageFileSystem</span></span>
<span data-ttu-id="4ad24-249">기본 Azure Data Lake Storage Gen2 계정에 대한 파일 시스템을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-249">Gets or sets the file system for the default Azure Data Lake Storage Gen2 account.</span></span>

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

### <span data-ttu-id="4ad24-250">-StorageRootPath</span><span class="sxs-lookup"><span data-stu-id="4ad24-250">-StorageRootPath</span></span>
<span data-ttu-id="4ad24-251">기본 Data Lake Store 계정에서 클러스터의 루트 경로를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-251">Gets or sets the path to the root of the cluster in the default Data Lake Store Account.</span></span>

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

### <span data-ttu-id="4ad24-252">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="4ad24-252">-SubnetName</span></span>
<span data-ttu-id="4ad24-253">이 HDInsight 클러스터에 대한 서브넷 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-253">Gets or sets the subnet name for this HDInsight cluster.</span></span>

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

### <span data-ttu-id="4ad24-254">-Version</span><span class="sxs-lookup"><span data-stu-id="4ad24-254">-Version</span></span>
<span data-ttu-id="4ad24-255">HDInsight 클러스터의 HDI 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-255">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="4ad24-256">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="4ad24-256">-VirtualNetworkId</span></span>
<span data-ttu-id="4ad24-257">클러스터를 프로비전할 가상 네트워크의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-257">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="4ad24-258">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="4ad24-258">-WorkerNodeSize</span></span>
<span data-ttu-id="4ad24-259">Worker 노드에 대한 가상 머신의 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-259">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="4ad24-260">허용 Get-AzVMSize VM 크기에 대한 자세한 내용은 HDInsight의 가격 책정 페이지를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4ad24-260">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="4ad24-261">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="4ad24-261">-ZookeeperNodeSize</span></span>
<span data-ttu-id="4ad24-262">Zookeeper 노드에 대한 가상 머신의 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-262">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="4ad24-263">허용 Get-AzVMSize VM 크기에 대한 자세한 내용은 HDInsight의 가격 책정 페이지를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4ad24-263">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="4ad24-264">이 매개 변수는 HBase 또는 Storm 클러스터에만 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-264">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="4ad24-265">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ad24-265">CommonParameters</span></span>
<span data-ttu-id="4ad24-266">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad24-266">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ad24-267">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4ad24-267">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ad24-268">입력</span><span class="sxs-lookup"><span data-stu-id="4ad24-268">INPUTS</span></span>

### <span data-ttu-id="4ad24-269">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="4ad24-269">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="4ad24-270">출력</span><span class="sxs-lookup"><span data-stu-id="4ad24-270">OUTPUTS</span></span>

### <span data-ttu-id="4ad24-271">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4ad24-271">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="4ad24-272">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4ad24-272">NOTES</span></span>
<span data-ttu-id="4ad24-273">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, hadoop, hdinsight, hd, insight</span><span class="sxs-lookup"><span data-stu-id="4ad24-273">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="4ad24-274">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ad24-274">RELATED LINKS</span></span>

[<span data-ttu-id="4ad24-275">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="4ad24-275">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

