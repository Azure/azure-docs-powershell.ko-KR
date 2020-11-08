---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: 9008cb1dba2c39a2c552b2395f4115ca50a17fdf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049080"
---
# <span data-ttu-id="3d98f-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="3d98f-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="3d98f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d98f-102">SYNOPSIS</span></span>
<span data-ttu-id="3d98f-103">현재 구독에 대 한 지정 된 리소스 그룹에 Azure HDInsight 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="3d98f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3d98f-104">SYNTAX</span></span>

### <span data-ttu-id="3d98f-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="3d98f-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificatePassword <String>]
 [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>]
 [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>]
 [-PublicNetworkAccessType <String>] [-OutboundPublicNetworkAccessType <String>]
 [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d98f-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="3d98f-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>]
 [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>] [-OutboundPublicNetworkAccessType <String>]
 [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d98f-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="3d98f-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>]
 [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>] [-OutboundPublicNetworkAccessType <String>]
 [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d98f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3d98f-108">DESCRIPTION</span></span>
<span data-ttu-id="3d98f-109">New-AzHDInsightCluster는 지정 된 매개 변수를 사용 하거나 New-AzHDInsightClusterConfig cmdlet을 사용 하 여 만든 구성 개체를 사용 하 여 Azure HDInsight 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="3d98f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3d98f-110">EXAMPLES</span></span>

### <span data-ttu-id="3d98f-111">예제 1: Azure HDInsight 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="3d98f-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
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
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
```

<span data-ttu-id="3d98f-112">이 명령은 현재 구독에 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="3d98f-113">예제 2: 고객 관리 키 디스크 암호화를 사용 하 여 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="3d98f-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
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
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AssignedIdentity $assignedIdentity `
            -EncryptionKeyName $encryptionKeyName `
            -EncryptionVaultUri $encryptionVaultUri `
            -EncryptionKeyVersion $encryptionKeyVersion
```

### <span data-ttu-id="3d98f-114">예제 3: 암호화를 통과 하도록 설정 하는 Azure HDInsight 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="3d98f-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
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
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionInTransit $true `
```

### <span data-ttu-id="3d98f-115">예제 4: 비공개 링크 기능을 사용 하 여 Azure HDInsight 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="3d98f-115">Example 4: Create an Azure HDInsight cluster with private link feature</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
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
        $subnetName="yoursubnetresourceid"

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -VirtualNetworkId $virtualNetworkId -SubnetName $subnetName `
            -PublicNetworkAccessType OutboundOnly -OutboundPublicNetworkAccessType PublicLoadBalancer `
```

### <span data-ttu-id="3d98f-116">예제 5: 호스트에서 암호화를 사용 하도록 설정 하는 Azure HDInsight 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="3d98f-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
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
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionAtHost $true `
```

### <span data-ttu-id="3d98f-117">예제 6: 자동 크기 조정을 사용 하는 Azure HDInsight 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="3d98f-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
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
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AutoscaleConfiguration $autoscaleConfiguration
```

## <span data-ttu-id="3d98f-118">변수</span><span class="sxs-lookup"><span data-stu-id="3d98f-118">PARAMETERS</span></span>

### <span data-ttu-id="3d98f-119">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="3d98f-119">-AadTenantId</span></span>
<span data-ttu-id="3d98f-120">Azure Data Lake Store에 액세스할 때 사용 되는 Azure AD 테 넌 트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-120">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="3d98f-121">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="3d98f-121">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="3d98f-122">클러스터에 대 한 추가 Azure 저장소 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-122">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="3d98f-123">또는 Add-AzHDInsightStorage cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-123">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="3d98f-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3d98f-124">-ApplicationId</span></span>
<span data-ttu-id="3d98f-125">Azure Data Lake에 액세스 하기 위한 서비스 사용자 응용 프로그램 Id를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-125">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="3d98f-126">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="3d98f-126">-AssignedIdentity</span></span>
<span data-ttu-id="3d98f-127">할당 된 id를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-127">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="3d98f-128">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d98f-128">-AutoscaleConfiguration</span></span>
<span data-ttu-id="3d98f-129">자동 크기 조정 구성을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-129">Gets or sets the autoscale configuration</span></span>

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

### <span data-ttu-id="3d98f-130">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="3d98f-130">-CertificateFileContents</span></span>
<span data-ttu-id="3d98f-131">Azure Data Lake Store에 액세스할 때 사용 될 인증서의 파일 내용을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-131">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="3d98f-132">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="3d98f-132">-CertificateFilePath</span></span>
<span data-ttu-id="3d98f-133">서비스 사용자로 인증 하는 데 사용 되는 인증서의 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-133">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="3d98f-134">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-134">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="3d98f-135">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="3d98f-135">-CertificatePassword</span></span>
<span data-ttu-id="3d98f-136">서비스 사용자로 인증 하는 데 사용 되는 인증서의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-136">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="3d98f-137">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-137">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="3d98f-138">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3d98f-138">-ClusterName</span></span>
<span data-ttu-id="3d98f-139">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-139">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="3d98f-140">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="3d98f-140">-ClusterSizeInNodes</span></span>
<span data-ttu-id="3d98f-141">클러스터에 대 한 작업자 노드 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-141">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="3d98f-142">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="3d98f-142">-ClusterTier</span></span>
<span data-ttu-id="3d98f-143">HDInsight 클러스터 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-143">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="3d98f-144">기본적으로이는 표준입니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-144">By default, this is Standard.</span></span>
<span data-ttu-id="3d98f-145">프리미엄 계층은 Linux 클러스터 에서만 사용할 수 있으며, 몇 가지 새로운 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-145">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="3d98f-146">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="3d98f-146">-ClusterType</span></span>
<span data-ttu-id="3d98f-147">만들 클러스터 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-147">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="3d98f-148">Hadoop, HBase, 폭풍, Spark, INTERACTIVEHIVE, Kafka, RServer 옵션은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-148">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="3d98f-149">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="3d98f-149">-ComponentVersion</span></span>
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

### <span data-ttu-id="3d98f-150">-구성</span><span class="sxs-lookup"><span data-stu-id="3d98f-150">-Config</span></span>
<span data-ttu-id="3d98f-151">클러스터를 만드는 데 사용할 클러스터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-151">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="3d98f-152">이 개체는 New-AzHDInsightClusterConfig cmdlet을 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-152">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="3d98f-153">-구성</span><span class="sxs-lookup"><span data-stu-id="3d98f-153">-Configurations</span></span>
<span data-ttu-id="3d98f-154">이 HDInsight 클러스터의 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-154">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="3d98f-155">또는 Add-AzHDInsightConfigValues cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-155">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="3d98f-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d98f-156">-DefaultProfile</span></span>
<span data-ttu-id="3d98f-157">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3d98f-157">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d98f-158">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="3d98f-158">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="3d98f-159">HDInsight 클러스터에서 사용할 기본 Azure 저장소 계정에 대 한 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-159">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="3d98f-160">또는 Set-AzHDInsightDefaultStorage cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-160">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="3d98f-161">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3d98f-161">-DefaultStorageAccountName</span></span>
<span data-ttu-id="3d98f-162">HDInsight 클러스터에 사용 되는 기본 Azure 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-162">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="3d98f-163">또는 Set-AzHDInsightDefaultStorage cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-163">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="3d98f-164">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="3d98f-164">-DefaultStorageAccountType</span></span>
<span data-ttu-id="3d98f-165">HDInsight 클러스터에 사용 되는 기본 저장소 계정의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-165">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="3d98f-166">사용할 수 있는 값은 AzureStorage 및 AzureDataLakeStore입니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-166">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="3d98f-167">지정 되지 않은 경우 AzureStorage가 기본값으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-167">Defaults to AzureStorage if not specified.</span></span>

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

### <span data-ttu-id="3d98f-168">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3d98f-168">-DefaultStorageContainer</span></span>
<span data-ttu-id="3d98f-169">HDInsight 클러스터에서 사용할 기본 Azure 저장소 계정에 있는 기본 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-169">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="3d98f-170">또는 Set-AzHDInsightDefaultStorage cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-170">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="3d98f-171">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="3d98f-171">-DefaultStorageRootPath</span></span>
<span data-ttu-id="3d98f-172">HDInsight 클러스터에서 기본 파일 시스템으로 사용할 Data Lake Store 계정에서 경로 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-172">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="3d98f-173">-Disksper. 노드</span><span class="sxs-lookup"><span data-stu-id="3d98f-173">-DisksPerWorkerNode</span></span>
<span data-ttu-id="3d98f-174">클러스터의 작업자 노드 역할에 대 한 디스크 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-174">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="3d98f-175">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="3d98f-175">-EdgeNodeSize</span></span>
<span data-ttu-id="3d98f-176">Edge 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-176">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="3d98f-177">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3d98f-177">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="3d98f-178">이 매개 변수는 RServer 클러스터에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-178">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="3d98f-179">-A. 알고리즘</span><span class="sxs-lookup"><span data-stu-id="3d98f-179">-EncryptionAlgorithm</span></span>
<span data-ttu-id="3d98f-180">암호화 알고리즘을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-180">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="3d98f-181">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="3d98f-181">-EncryptionAtHost</span></span>
<span data-ttu-id="3d98f-182">호스트에서 암호화를 사용할지 여부를 나타내는 플래그를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-182">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="3d98f-183">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="3d98f-183">-EncryptionInTransit</span></span>
<span data-ttu-id="3d98f-184">전송에 암호화를 사용할지 여부를 나타내는 플래그를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-184">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="3d98f-185">-A</span><span class="sxs-lookup"><span data-stu-id="3d98f-185">-EncryptionKeyName</span></span>
<span data-ttu-id="3d98f-186">암호화 키 이름을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-186">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="3d98f-187">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="3d98f-187">-EncryptionKeyVersion</span></span>
<span data-ttu-id="3d98f-188">암호화 키 버전을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-188">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="3d98f-189">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="3d98f-189">-EncryptionVaultUri</span></span>
<span data-ttu-id="3d98f-190">암호화 자격 증명 모음 uri를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-190">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="3d98f-191">-용 Nodesize</span><span class="sxs-lookup"><span data-stu-id="3d98f-191">-HeadNodeSize</span></span>
<span data-ttu-id="3d98f-192">헤드 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-192">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="3d98f-193">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3d98f-193">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="3d98f-194">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="3d98f-194">-HiveMetastore</span></span>
<span data-ttu-id="3d98f-195">하이브 메타 데이터를 저장할 SQL 데이터베이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-195">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="3d98f-196">또는 Add-AzHDInsightMetastore cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-196">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="3d98f-197">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="3d98f-197">-HttpCredential</span></span>
<span data-ttu-id="3d98f-198">클러스터에 대 한 HTTP (클러스터 로그인) 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-198">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="3d98f-199">-위치</span><span class="sxs-lookup"><span data-stu-id="3d98f-199">-Location</span></span>
<span data-ttu-id="3d98f-200">클러스터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-200">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="3d98f-201">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="3d98f-201">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="3d98f-202">지원 되는 최소 TLS 버전을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-202">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="3d98f-203">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3d98f-203">-ObjectId</span></span>
<span data-ttu-id="3d98f-204">클러스터를 나타내는 Azure AD 서비스 주체의 Azure AD 개체 ID (GUID)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-204">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="3d98f-205">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-205">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="3d98f-206">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="3d98f-206">-OozieMetastore</span></span>
<span data-ttu-id="3d98f-207">Oozie 메타 데이터를 저장할 SQL 데이터베이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-207">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="3d98f-208">또는 Add-AzHDInsightMetastore cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-208">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="3d98f-209">-OSType</span><span class="sxs-lookup"><span data-stu-id="3d98f-209">-OSType</span></span>
<span data-ttu-id="3d98f-210">클러스터의 운영 체제를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-210">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="3d98f-211">옵션: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="3d98f-211">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="3d98f-212">-OutboundPublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="3d98f-212">-OutboundPublicNetworkAccessType</span></span>
<span data-ttu-id="3d98f-213">공용 네트워크에 대 한 아웃 바운드 액세스 형식을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-213">Gets or sets the outbound access type to the public network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PublicLoadBalancer, UDR

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d98f-214">-PublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="3d98f-214">-PublicNetworkAccessType</span></span>
<span data-ttu-id="3d98f-215">공용 네트워크 액세스 형식을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-215">Gets or sets the public network access type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: InboundAndOutbound, OutboundOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d98f-216">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="3d98f-216">-RdpAccessExpiry</span></span>
<span data-ttu-id="3d98f-217">클러스터에 대 한 RDP (원격 데스크톱 프로토콜) 액세스에 대 한 만료 날짜를 DateTime 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-217">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="3d98f-218">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="3d98f-218">-RdpCredential</span></span>
<span data-ttu-id="3d98f-219">클러스터의 RDP (원격 데스크톱) 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-219">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="3d98f-220">이는 Windows 클러스터에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-220">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="3d98f-221">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d98f-221">-ResourceGroupName</span></span>
<span data-ttu-id="3d98f-222">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-222">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="3d98f-223">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="3d98f-223">-ScriptActions</span></span>
<span data-ttu-id="3d98f-224">클러스터 생성이 끝날 때 클러스터에서 실행할 스크립트 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-224">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="3d98f-225">또는 Add-AzHDInsightScriptAction를 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-225">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="3d98f-226">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="3d98f-226">-SecurityProfile</span></span>
<span data-ttu-id="3d98f-227">보안 클러스터를 만드는 데 사용 되는 보안 관련 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-227">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="3d98f-228">또는 Add-AzHDInsightSecurityProfile cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-228">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="3d98f-229">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="3d98f-229">-SshCredential</span></span>
<span data-ttu-id="3d98f-230">SSH 연결에 사용 되는 SSH 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-230">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="3d98f-231">이는 Linux 용 클러스터에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-231">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="3d98f-232">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="3d98f-232">-SshPublicKey</span></span>
<span data-ttu-id="3d98f-233">SSH 연결에 사용 되는 공개 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-233">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="3d98f-234">이는 Linux 용 클러스터에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-234">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="3d98f-235">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="3d98f-235">-SubnetName</span></span>
<span data-ttu-id="3d98f-236">클러스터에 대해 선택 된 가상 네트워크 내 서브넷의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-236">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="3d98f-237">-버전</span><span class="sxs-lookup"><span data-stu-id="3d98f-237">-Version</span></span>
<span data-ttu-id="3d98f-238">HDInsight 클러스터의 HDI 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-238">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="3d98f-239">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="3d98f-239">-VirtualNetworkId</span></span>
<span data-ttu-id="3d98f-240">클러스터를 프로 비전 할 가상 네트워크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-240">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="3d98f-241">-. 노드 크기</span><span class="sxs-lookup"><span data-stu-id="3d98f-241">-WorkerNodeSize</span></span>
<span data-ttu-id="3d98f-242">작업자 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-242">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="3d98f-243">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3d98f-243">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="3d98f-244">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="3d98f-244">-ZookeeperNodeSize</span></span>
<span data-ttu-id="3d98f-245">사육 사 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-245">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="3d98f-246">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3d98f-246">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="3d98f-247">이 매개 변수는 HBase 또는 폭풍 클러스터에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-247">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="3d98f-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d98f-248">CommonParameters</span></span>
<span data-ttu-id="3d98f-249">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d98f-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d98f-250">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3d98f-250">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d98f-251">입력</span><span class="sxs-lookup"><span data-stu-id="3d98f-251">INPUTS</span></span>

### <span data-ttu-id="3d98f-252">AzureHDInsightConfig의. m m.</span><span class="sxs-lookup"><span data-stu-id="3d98f-252">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="3d98f-253">출력</span><span class="sxs-lookup"><span data-stu-id="3d98f-253">OUTPUTS</span></span>

### <span data-ttu-id="3d98f-254">AzureHDInsightCluster의. m m.</span><span class="sxs-lookup"><span data-stu-id="3d98f-254">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="3d98f-255">상속자</span><span class="sxs-lookup"><span data-stu-id="3d98f-255">NOTES</span></span>
<span data-ttu-id="3d98f-256">키워드: azure, azurerm, arm, resource, 관리, 관리자, hadoop, hdinsight, hd, 통찰력</span><span class="sxs-lookup"><span data-stu-id="3d98f-256">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="3d98f-257">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d98f-257">RELATED LINKS</span></span>

[<span data-ttu-id="3d98f-258">새로운 AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="3d98f-258">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

