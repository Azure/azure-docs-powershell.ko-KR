---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: c0d3d6518025aab22add0859bde69cb1ad279138
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879781"
---
# <span data-ttu-id="6f25d-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="6f25d-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="6f25d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f25d-102">SYNOPSIS</span></span>
<span data-ttu-id="6f25d-103">현재 구독에 대 한 지정 된 리소스 그룹에 Azure HDInsight 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="6f25d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6f25d-104">SYNTAX</span></span>

### <span data-ttu-id="6f25d-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="6f25d-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [[-DefaultStorageAccountType] <StorageType>]
 [[-Config] <AzureHDInsightConfig>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>]
 [[-AdditionalStorageAccounts] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Configurations] <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [[-ScriptActions] <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [[-DefaultStorageContainer] <String>] [[-DefaultStorageRootPath] <String>] [[-Version] <String>]
 [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>] [[-EdgeNodeSize] <String>]
 [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>]
 [[-ComponentVersion] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-VirtualNetworkId] <String>] [[-SubnetName] <String>] [[-OSType] <OSType>] [[-ClusterTier] <Tier>]
 [[-SshCredential] <PSCredential>] [[-SshPublicKey] <String>] [[-RdpCredential] <PSCredential>]
 [[-RdpAccessExpiry] <DateTime>] [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>]
 [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>] [[-SecurityProfile] <AzureHDInsightSecurityProfile>]
 [[-DisksPerWorkerNode] <Int32>] [[-MinSupportedTlsVersion] <String>]
 [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f25d-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="6f25d-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [[-DefaultStorageAccountType] <StorageType>]
 [[-Config] <AzureHDInsightConfig>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>]
 [[-AdditionalStorageAccounts] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Configurations] <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [[-ScriptActions] <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [[-DefaultStorageContainer] <String>] [[-DefaultStorageRootPath] <String>] [[-Version] <String>]
 [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>] [[-EdgeNodeSize] <String>]
 [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>]
 [[-ComponentVersion] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-VirtualNetworkId] <String>] [[-SubnetName] <String>] [[-OSType] <OSType>] [[-ClusterTier] <Tier>]
 [[-SshCredential] <PSCredential>] [[-SshPublicKey] <String>] [[-RdpCredential] <PSCredential>]
 [[-RdpAccessExpiry] <DateTime>] [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>]
 [[-CertificateFilePath] <String>] [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>]
 [[-SecurityProfile] <AzureHDInsightSecurityProfile>] [[-DisksPerWorkerNode] <Int32>]
 [[-MinSupportedTlsVersion] <String>] [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f25d-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="6f25d-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [[-DefaultStorageAccountType] <StorageType>]
 [[-Config] <AzureHDInsightConfig>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>]
 [[-AdditionalStorageAccounts] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Configurations] <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [[-ScriptActions] <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [[-DefaultStorageContainer] <String>] [[-DefaultStorageRootPath] <String>] [[-Version] <String>]
 [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>] [[-EdgeNodeSize] <String>]
 [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>]
 [[-ComponentVersion] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-VirtualNetworkId] <String>] [[-SubnetName] <String>] [[-OSType] <OSType>] [[-ClusterTier] <Tier>]
 [[-SshCredential] <PSCredential>] [[-SshPublicKey] <String>] [[-RdpCredential] <PSCredential>]
 [[-RdpAccessExpiry] <DateTime>] [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>]
 [[-CertificateFileContents] <Byte[]>] [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>]
 [[-SecurityProfile] <AzureHDInsightSecurityProfile>] [[-DisksPerWorkerNode] <Int32>]
 [[-MinSupportedTlsVersion] <String>] [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f25d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6f25d-108">DESCRIPTION</span></span>
<span data-ttu-id="6f25d-109">New-AzHDInsightCluster는 지정 된 매개 변수를 사용 하거나 New-AzHDInsightClusterConfig cmdlet을 사용 하 여 만든 구성 개체를 사용 하 여 Azure HDInsight 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="6f25d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6f25d-110">EXAMPLES</span></span>

### <span data-ttu-id="6f25d-111">예제 1: Azure HDInsight 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="6f25d-111">Example 1: Create an Azure HDInsight cluster</span></span>
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

<span data-ttu-id="6f25d-112">이 명령은 현재 구독에 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-112">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="6f25d-113">변수</span><span class="sxs-lookup"><span data-stu-id="6f25d-113">PARAMETERS</span></span>

### <span data-ttu-id="6f25d-114">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="6f25d-114">-AadTenantId</span></span>
<span data-ttu-id="6f25d-115">Azure Data Lake Store에 액세스할 때 사용 되는 Azure AD 테 넌 트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-115">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="6f25d-116">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="6f25d-116">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="6f25d-117">클러스터에 대 한 추가 Azure 저장소 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-117">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="6f25d-118">또는 Add-AzHDInsightStorage cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-118">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="6f25d-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="6f25d-119">-ApplicationId</span></span>
<span data-ttu-id="6f25d-120">Azure Data Lake에 액세스 하기 위한 서비스 사용자 응용 프로그램 Id를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-120">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="6f25d-121">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="6f25d-121">-CertificateFileContents</span></span>
<span data-ttu-id="6f25d-122">Azure Data Lake Store에 액세스할 때 사용 될 인증서의 파일 내용을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-122">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="6f25d-123">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="6f25d-123">-CertificateFilePath</span></span>
<span data-ttu-id="6f25d-124">서비스 사용자로 인증 하는 데 사용 되는 인증서의 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-124">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="6f25d-125">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-125">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="6f25d-126">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="6f25d-126">-CertificatePassword</span></span>
<span data-ttu-id="6f25d-127">서비스 사용자로 인증 하는 데 사용 되는 인증서의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-127">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="6f25d-128">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-128">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="6f25d-129">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6f25d-129">-ClusterName</span></span>
<span data-ttu-id="6f25d-130">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-130">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="6f25d-131">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="6f25d-131">-ClusterSizeInNodes</span></span>
<span data-ttu-id="6f25d-132">클러스터에 대 한 작업자 노드 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-132">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="6f25d-133">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="6f25d-133">-ClusterTier</span></span>
<span data-ttu-id="6f25d-134">HDInsight 클러스터 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-134">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="6f25d-135">기본적으로이는 표준입니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-135">By default, this is Standard.</span></span>
<span data-ttu-id="6f25d-136">프리미엄 계층은 Linux 클러스터 에서만 사용할 수 있으며, 몇 가지 새로운 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-136">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="6f25d-137">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="6f25d-137">-ClusterType</span></span>
<span data-ttu-id="6f25d-138">만들 클러스터 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-138">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="6f25d-139">Hadoop, HBase, 폭풍, Spark, INTERACTIVEHIVE, Kafka, RServer 옵션은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-139">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="6f25d-140">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="6f25d-140">-ComponentVersion</span></span>
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

### <span data-ttu-id="6f25d-141">-구성</span><span class="sxs-lookup"><span data-stu-id="6f25d-141">-Config</span></span>
<span data-ttu-id="6f25d-142">클러스터를 만드는 데 사용할 클러스터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-142">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="6f25d-143">이 개체는 New-AzHDInsightClusterConfig cmdlet을 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-143">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="6f25d-144">-구성</span><span class="sxs-lookup"><span data-stu-id="6f25d-144">-Configurations</span></span>
<span data-ttu-id="6f25d-145">이 HDInsight 클러스터의 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-145">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="6f25d-146">또는 Add-AzHDInsightConfigValues cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-146">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="6f25d-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f25d-147">-DefaultProfile</span></span>
<span data-ttu-id="6f25d-148">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6f25d-148">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f25d-149">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="6f25d-149">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="6f25d-150">HDInsight 클러스터에서 사용할 기본 Azure 저장소 계정에 대 한 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-150">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="6f25d-151">또는 Set-AzHDInsightDefaultStorage cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-151">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="6f25d-152">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6f25d-152">-DefaultStorageAccountName</span></span>
<span data-ttu-id="6f25d-153">HDInsight 클러스터에 사용 되는 기본 Azure 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-153">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="6f25d-154">또는 Set-AzHDInsightDefaultStorage cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-154">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="6f25d-155">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="6f25d-155">-DefaultStorageAccountType</span></span>
<span data-ttu-id="6f25d-156">HDInsight 클러스터에 사용 되는 기본 저장소 계정의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-156">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="6f25d-157">사용할 수 있는 값은 AzureStorage 및 AzureDataLakeStore입니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-157">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="6f25d-158">지정 되지 않은 경우 AzureStorage가 기본값으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-158">Defaults to AzureStorage if not specified.</span></span>

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

### <span data-ttu-id="6f25d-159">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6f25d-159">-DefaultStorageContainer</span></span>
<span data-ttu-id="6f25d-160">HDInsight 클러스터에서 사용할 기본 Azure 저장소 계정에 있는 기본 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-160">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="6f25d-161">또는 Set-AzHDInsightDefaultStorage cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-161">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="6f25d-162">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="6f25d-162">-DefaultStorageRootPath</span></span>
<span data-ttu-id="6f25d-163">HDInsight 클러스터에서 기본 파일 시스템으로 사용할 Data Lake Store 계정에서 경로 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-163">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="6f25d-164">-Disksper. 노드</span><span class="sxs-lookup"><span data-stu-id="6f25d-164">-DisksPerWorkerNode</span></span>
<span data-ttu-id="6f25d-165">클러스터의 작업자 노드 역할에 대 한 디스크 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-165">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="6f25d-166">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="6f25d-166">-EdgeNodeSize</span></span>
<span data-ttu-id="6f25d-167">Edge 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-167">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="6f25d-168">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6f25d-168">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="6f25d-169">이 매개 변수는 RServer 클러스터에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-169">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="6f25d-170">-용 Nodesize</span><span class="sxs-lookup"><span data-stu-id="6f25d-170">-HeadNodeSize</span></span>
<span data-ttu-id="6f25d-171">헤드 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-171">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="6f25d-172">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6f25d-172">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="6f25d-173">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="6f25d-173">-HiveMetastore</span></span>
<span data-ttu-id="6f25d-174">하이브 메타 데이터를 저장할 SQL 데이터베이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-174">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="6f25d-175">또는 Add-AzHDInsightMetastore cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-175">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="6f25d-176">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="6f25d-176">-HttpCredential</span></span>
<span data-ttu-id="6f25d-177">클러스터에 대 한 HTTP (클러스터 로그인) 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-177">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="6f25d-178">-위치</span><span class="sxs-lookup"><span data-stu-id="6f25d-178">-Location</span></span>
<span data-ttu-id="6f25d-179">클러스터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-179">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="6f25d-180">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="6f25d-180">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="6f25d-181">지원 되는 최소 TLS 버전을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-181">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="6f25d-182">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6f25d-182">-ObjectId</span></span>
<span data-ttu-id="6f25d-183">클러스터를 나타내는 Azure AD 서비스 주체의 Azure AD 개체 ID (GUID)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-183">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="6f25d-184">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-184">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="6f25d-185">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="6f25d-185">-OozieMetastore</span></span>
<span data-ttu-id="6f25d-186">Oozie 메타 데이터를 저장할 SQL 데이터베이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-186">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="6f25d-187">또는 Add-AzHDInsightMetastore cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-187">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="6f25d-188">-OSType</span><span class="sxs-lookup"><span data-stu-id="6f25d-188">-OSType</span></span>
<span data-ttu-id="6f25d-189">클러스터의 운영 체제를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-189">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="6f25d-190">옵션: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="6f25d-190">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="6f25d-191">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="6f25d-191">-RdpAccessExpiry</span></span>
<span data-ttu-id="6f25d-192">클러스터에 대 한 RDP (원격 데스크톱 프로토콜) 액세스에 대 한 만료 날짜를 DateTime 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-192">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="6f25d-193">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="6f25d-193">-RdpCredential</span></span>
<span data-ttu-id="6f25d-194">클러스터의 RDP (원격 데스크톱) 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-194">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="6f25d-195">이는 Windows 클러스터에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-195">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="6f25d-196">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f25d-196">-ResourceGroupName</span></span>
<span data-ttu-id="6f25d-197">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-197">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6f25d-198">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="6f25d-198">-ScriptActions</span></span>
<span data-ttu-id="6f25d-199">클러스터 생성이 끝날 때 클러스터에서 실행할 스크립트 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-199">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="6f25d-200">또는 Add-AzHDInsightScriptAction를 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-200">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="6f25d-201">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="6f25d-201">-SecurityProfile</span></span>
<span data-ttu-id="6f25d-202">보안 클러스터를 만드는 데 사용 되는 보안 관련 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-202">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="6f25d-203">또는 Add-AzHDInsightSecurityProfile cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-203">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="6f25d-204">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="6f25d-204">-SshCredential</span></span>
<span data-ttu-id="6f25d-205">SSH 연결에 사용 되는 SSH 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-205">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="6f25d-206">이는 Linux 용 클러스터에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-206">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="6f25d-207">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="6f25d-207">-SshPublicKey</span></span>
<span data-ttu-id="6f25d-208">SSH 연결에 사용 되는 공개 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-208">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="6f25d-209">이는 Linux 용 클러스터에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-209">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="6f25d-210">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="6f25d-210">-SubnetName</span></span>
<span data-ttu-id="6f25d-211">클러스터에 대해 선택 된 가상 네트워크 내 서브넷의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-211">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="6f25d-212">-버전</span><span class="sxs-lookup"><span data-stu-id="6f25d-212">-Version</span></span>
<span data-ttu-id="6f25d-213">HDInsight 클러스터의 HDI 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-213">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="6f25d-214">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="6f25d-214">-VirtualNetworkId</span></span>
<span data-ttu-id="6f25d-215">클러스터를 프로 비전 할 가상 네트워크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-215">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="6f25d-216">-. 노드 크기</span><span class="sxs-lookup"><span data-stu-id="6f25d-216">-WorkerNodeSize</span></span>
<span data-ttu-id="6f25d-217">작업자 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-217">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="6f25d-218">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6f25d-218">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="6f25d-219">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="6f25d-219">-ZookeeperNodeSize</span></span>
<span data-ttu-id="6f25d-220">사육 사 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-220">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="6f25d-221">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6f25d-221">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="6f25d-222">이 매개 변수는 HBase 또는 폭풍 클러스터에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-222">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="6f25d-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f25d-223">CommonParameters</span></span>
<span data-ttu-id="6f25d-224">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f25d-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f25d-225">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6f25d-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f25d-226">입력</span><span class="sxs-lookup"><span data-stu-id="6f25d-226">INPUTS</span></span>

### <span data-ttu-id="6f25d-227">AzureHDInsightConfig의. m m.</span><span class="sxs-lookup"><span data-stu-id="6f25d-227">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="6f25d-228">출력</span><span class="sxs-lookup"><span data-stu-id="6f25d-228">OUTPUTS</span></span>

### <span data-ttu-id="6f25d-229">AzureHDInsightCluster의. m m.</span><span class="sxs-lookup"><span data-stu-id="6f25d-229">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="6f25d-230">상속자</span><span class="sxs-lookup"><span data-stu-id="6f25d-230">NOTES</span></span>
<span data-ttu-id="6f25d-231">키워드: azure, azurerm, arm, resource, 관리, 관리자, hadoop, hdinsight, hd, 통찰력</span><span class="sxs-lookup"><span data-stu-id="6f25d-231">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="6f25d-232">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f25d-232">RELATED LINKS</span></span>

[<span data-ttu-id="6f25d-233">새로운 AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="6f25d-233">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

