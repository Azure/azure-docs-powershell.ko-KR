---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: a372654faa9c3f157c44e5f60ff2f4244cd16d7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868253"
---
# <span data-ttu-id="274fc-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="274fc-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="274fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="274fc-102">SYNOPSIS</span></span>
<span data-ttu-id="274fc-103">현재 구독에 대 한 지정 된 리소스 그룹에 Azure HDInsight 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="274fc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="274fc-104">SYNTAX</span></span>

### <span data-ttu-id="274fc-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="274fc-105">Default (Default)</span></span>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificatePassword <String>] [-AadTenantId <Guid>]
 [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="274fc-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="274fc-106">CertificateFilePath</span></span>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="274fc-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="274fc-107">CertificateFileContents</span></span>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="274fc-108">설명은</span><span class="sxs-lookup"><span data-stu-id="274fc-108">DESCRIPTION</span></span>
<span data-ttu-id="274fc-109">New-AzHDInsightCluster는 지정 된 매개 변수를 사용 하거나 New-AzHDInsightClusterConfig cmdlet을 사용 하 여 만든 구성 개체를 사용 하 여 Azure HDInsight 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="274fc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="274fc-110">EXAMPLES</span></span>

### <span data-ttu-id="274fc-111">예제 1: Azure HDInsight 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="274fc-111">Example 1: Create an Azure HDInsight cluster</span></span>
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
        #   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
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

<span data-ttu-id="274fc-112">이 명령은 현재 구독에 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-112">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="274fc-113">변수</span><span class="sxs-lookup"><span data-stu-id="274fc-113">PARAMETERS</span></span>

### <span data-ttu-id="274fc-114">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="274fc-114">-AadTenantId</span></span>
<span data-ttu-id="274fc-115">Azure Data Lake Store에 액세스할 때 사용 되는 Azure AD 테 넌 트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-115">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="274fc-116">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="274fc-116">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="274fc-117">클러스터에 대 한 추가 Azure 저장소 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-117">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="274fc-118">또는 Add-AzHDInsightStorage cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-118">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="274fc-119">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="274fc-119">-CertificateFileContents</span></span>
<span data-ttu-id="274fc-120">Azure Data Lake Store에 액세스할 때 사용 될 인증서의 파일 내용을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-120">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="274fc-121">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="274fc-121">-CertificateFilePath</span></span>
<span data-ttu-id="274fc-122">서비스 사용자로 인증 하는 데 사용 되는 인증서의 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-122">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="274fc-123">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-123">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="274fc-124">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="274fc-124">-CertificatePassword</span></span>
<span data-ttu-id="274fc-125">서비스 사용자로 인증 하는 데 사용 되는 인증서의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-125">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="274fc-126">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-126">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="274fc-127">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="274fc-127">-ClusterName</span></span>
<span data-ttu-id="274fc-128">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-128">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="274fc-129">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="274fc-129">-ClusterSizeInNodes</span></span>
<span data-ttu-id="274fc-130">클러스터에 대 한 작업자 노드 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-130">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="274fc-131">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="274fc-131">-ClusterTier</span></span>
<span data-ttu-id="274fc-132">HDInsight 클러스터 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-132">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="274fc-133">기본적으로이는 표준입니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-133">By default, this is Standard.</span></span>
<span data-ttu-id="274fc-134">프리미엄 계층은 Linux 클러스터 에서만 사용할 수 있으며, 몇 가지 새로운 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-134">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="274fc-135">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="274fc-135">-ClusterType</span></span>
<span data-ttu-id="274fc-136">만들 클러스터 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-136">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="274fc-137">옵션: Hadoop, HBase, 폭풍, Spark</span><span class="sxs-lookup"><span data-stu-id="274fc-137">Options are: Hadoop, HBase, Storm, Spark</span></span>

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

### <span data-ttu-id="274fc-138">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="274fc-138">-ComponentVersion</span></span>
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

### <span data-ttu-id="274fc-139">-구성</span><span class="sxs-lookup"><span data-stu-id="274fc-139">-Config</span></span>
<span data-ttu-id="274fc-140">클러스터를 만드는 데 사용할 클러스터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-140">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="274fc-141">이 개체는 New-AzHDInsightClusterConfig cmdlet을 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-141">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="274fc-142">-구성</span><span class="sxs-lookup"><span data-stu-id="274fc-142">-Configurations</span></span>
<span data-ttu-id="274fc-143">이 HDInsight 클러스터의 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-143">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="274fc-144">또는 Add-AzHDInsightConfigValues cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-144">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="274fc-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="274fc-145">-DefaultProfile</span></span>
<span data-ttu-id="274fc-146">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="274fc-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="274fc-147">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="274fc-147">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="274fc-148">HDInsight 클러스터에서 사용할 기본 Azure 저장소 계정에 대 한 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-148">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="274fc-149">또는 Set-AzHDInsightDefaultStorage cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-149">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="274fc-150">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="274fc-150">-DefaultStorageAccountName</span></span>
<span data-ttu-id="274fc-151">HDInsight 클러스터에 사용 되는 기본 Azure 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-151">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="274fc-152">또는 Set-AzHDInsightDefaultStorage cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-152">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="274fc-153">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="274fc-153">-DefaultStorageAccountType</span></span>
<span data-ttu-id="274fc-154">HDInsight 클러스터에 사용 되는 기본 저장소 계정의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-154">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="274fc-155">사용할 수 있는 값은 AzureStorage 및 AzureDataLakeStore입니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-155">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="274fc-156">지정 되지 않은 경우 AzureStorage가 기본값으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-156">Defaults to AzureStorage if not specified.</span></span>

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

### <span data-ttu-id="274fc-157">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="274fc-157">-DefaultStorageContainer</span></span>
<span data-ttu-id="274fc-158">HDInsight 클러스터에서 사용할 기본 Azure 저장소 계정에 있는 기본 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-158">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="274fc-159">또는 Set-AzHDInsightDefaultStorage cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-159">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="274fc-160">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="274fc-160">-DefaultStorageRootPath</span></span>
<span data-ttu-id="274fc-161">HDInsight 클러스터에서 기본 파일 시스템으로 사용할 Data Lake Store 계정에서 경로 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-161">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="274fc-162">-Disksper. 노드</span><span class="sxs-lookup"><span data-stu-id="274fc-162">-DisksPerWorkerNode</span></span>
<span data-ttu-id="274fc-163">클러스터의 작업자 노드 역할에 대 한 디스크 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-163">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="274fc-164">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="274fc-164">-EdgeNodeSize</span></span>
<span data-ttu-id="274fc-165">Edge 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-165">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="274fc-166">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="274fc-166">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="274fc-167">이 매개 변수는 RServer 클러스터에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-167">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="274fc-168">-용 Nodesize</span><span class="sxs-lookup"><span data-stu-id="274fc-168">-HeadNodeSize</span></span>
<span data-ttu-id="274fc-169">헤드 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-169">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="274fc-170">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="274fc-170">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="274fc-171">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="274fc-171">-HiveMetastore</span></span>
<span data-ttu-id="274fc-172">하이브 메타 데이터를 저장할 SQL 데이터베이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-172">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="274fc-173">또는 Add-AzHDInsightMetastore cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-173">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="274fc-174">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="274fc-174">-HttpCredential</span></span>
<span data-ttu-id="274fc-175">클러스터에 대 한 HTTP (클러스터 로그인) 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-175">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="274fc-176">-위치</span><span class="sxs-lookup"><span data-stu-id="274fc-176">-Location</span></span>
<span data-ttu-id="274fc-177">클러스터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-177">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="274fc-178">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="274fc-178">-ObjectId</span></span>
<span data-ttu-id="274fc-179">클러스터를 나타내는 Azure AD 서비스 주체의 Azure AD 개체 ID (GUID)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-179">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="274fc-180">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-180">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="274fc-181">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="274fc-181">-OozieMetastore</span></span>
<span data-ttu-id="274fc-182">Oozie 메타 데이터를 저장할 SQL 데이터베이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-182">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="274fc-183">또는 Add-AzHDInsightMetastore cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-183">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="274fc-184">-OSType</span><span class="sxs-lookup"><span data-stu-id="274fc-184">-OSType</span></span>
<span data-ttu-id="274fc-185">클러스터의 운영 체제를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-185">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="274fc-186">옵션: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="274fc-186">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="274fc-187">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="274fc-187">-RdpAccessExpiry</span></span>
<span data-ttu-id="274fc-188">클러스터에 대 한 RDP (원격 데스크톱 프로토콜) 액세스에 대 한 만료 날짜를 DateTime 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-188">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="274fc-189">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="274fc-189">-RdpCredential</span></span>
<span data-ttu-id="274fc-190">클러스터의 RDP (원격 데스크톱) 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-190">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="274fc-191">이는 Windows 클러스터에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-191">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="274fc-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="274fc-192">-ResourceGroupName</span></span>
<span data-ttu-id="274fc-193">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-193">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="274fc-194">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="274fc-194">-ScriptActions</span></span>
<span data-ttu-id="274fc-195">클러스터 생성이 끝날 때 클러스터에서 실행할 스크립트 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-195">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="274fc-196">또는 Add-AzHDInsightScriptAction를 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-196">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="274fc-197">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="274fc-197">-SecurityProfile</span></span>
<span data-ttu-id="274fc-198">보안 클러스터를 만드는 데 사용 되는 보안 관련 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-198">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="274fc-199">또는 Add-AzHDInsightSecurityProfile cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-199">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="274fc-200">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="274fc-200">-SshCredential</span></span>
<span data-ttu-id="274fc-201">SSH 연결에 사용 되는 SSH 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-201">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="274fc-202">이는 Linux 용 클러스터에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-202">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="274fc-203">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="274fc-203">-SshPublicKey</span></span>
<span data-ttu-id="274fc-204">SSH 연결에 사용 되는 공개 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-204">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="274fc-205">이는 Linux 용 클러스터에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-205">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="274fc-206">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="274fc-206">-SubnetName</span></span>
<span data-ttu-id="274fc-207">클러스터에 대해 선택 된 가상 네트워크 내 서브넷의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-207">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="274fc-208">-버전</span><span class="sxs-lookup"><span data-stu-id="274fc-208">-Version</span></span>
<span data-ttu-id="274fc-209">HDInsight 클러스터의 HDI 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-209">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="274fc-210">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="274fc-210">-VirtualNetworkId</span></span>
<span data-ttu-id="274fc-211">클러스터를 프로 비전 할 가상 네트워크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-211">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="274fc-212">-. 노드 크기</span><span class="sxs-lookup"><span data-stu-id="274fc-212">-WorkerNodeSize</span></span>
<span data-ttu-id="274fc-213">작업자 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-213">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="274fc-214">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="274fc-214">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="274fc-215">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="274fc-215">-ZookeeperNodeSize</span></span>
<span data-ttu-id="274fc-216">사육 사 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-216">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="274fc-217">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="274fc-217">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="274fc-218">이 매개 변수는 HBase 또는 폭풍 클러스터에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-218">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="274fc-219">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="274fc-219">CommonParameters</span></span>
<span data-ttu-id="274fc-220">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="274fc-220">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="274fc-221">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="274fc-221">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="274fc-222">입력</span><span class="sxs-lookup"><span data-stu-id="274fc-222">INPUTS</span></span>

### <span data-ttu-id="274fc-223">AzureHDInsightConfig의. m m.</span><span class="sxs-lookup"><span data-stu-id="274fc-223">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="274fc-224">출력</span><span class="sxs-lookup"><span data-stu-id="274fc-224">OUTPUTS</span></span>

### <span data-ttu-id="274fc-225">AzureHDInsightCluster의. m m.</span><span class="sxs-lookup"><span data-stu-id="274fc-225">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="274fc-226">상속자</span><span class="sxs-lookup"><span data-stu-id="274fc-226">NOTES</span></span>
<span data-ttu-id="274fc-227">키워드: azure, azurerm, arm, resource, 관리, 관리자, hadoop, hdinsight, hd, 통찰력</span><span class="sxs-lookup"><span data-stu-id="274fc-227">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="274fc-228">관련 링크</span><span class="sxs-lookup"><span data-stu-id="274fc-228">RELATED LINKS</span></span>

[<span data-ttu-id="274fc-229">새로운 AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="274fc-229">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

