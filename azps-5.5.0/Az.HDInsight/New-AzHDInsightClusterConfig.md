---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 1124136a580d0079690c60e31fe8de8649e3cafb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200268"
---
# <span data-ttu-id="95516-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="95516-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="95516-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95516-102">SYNOPSIS</span></span>
<span data-ttu-id="95516-103">Azure HDInsight 클러스터 구성을 설명하는 비 지속형 클러스터 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="95516-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="95516-104">구문</span><span class="sxs-lookup"><span data-stu-id="95516-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [-StorageAccountResourceId <String>] [-StorageAccountKey <String>]
 [-StorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-MinSupportedTlsVersion <String>]
 [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95516-105">설명</span><span class="sxs-lookup"><span data-stu-id="95516-105">DESCRIPTION</span></span>
<span data-ttu-id="95516-106">**New-AzHDInsightClusterConfig** cmdlet은 Azure HDInsight 클러스터 구성을 설명하는 비 지속형 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="95516-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="95516-107">예제</span><span class="sxs-lookup"><span data-stu-id="95516-107">EXAMPLES</span></span>

### <span data-ttu-id="95516-108">예제 1: 클러스터 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="95516-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageaccountname"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

<span data-ttu-id="95516-109">이 명령은 클러스터 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="95516-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="95516-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95516-110">PARAMETERS</span></span>

### <span data-ttu-id="95516-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="95516-111">-AadTenantId</span></span>
<span data-ttu-id="95516-112">Azure Data Lake Store에 액세스할 때 사용할 Azure AD 테넌트 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="95516-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="95516-113">-ApplicationId</span></span>
<span data-ttu-id="95516-114">Azure Data Lake에 액세스하기 위한 서비스 주체 애플리케이션 ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="95516-115">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="95516-115">-AssignedIdentity</span></span>
<span data-ttu-id="95516-116">할당된 ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-116">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="95516-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="95516-117">-CertificateFileContents</span></span>
<span data-ttu-id="95516-118">Azure Data Lake Store에 액세스할 때 사용할 인증서의 파일 콘텐츠를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95516-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="95516-119">-CertificateFilePath</span></span>
<span data-ttu-id="95516-120">서비스 주체로 인증하는 데 사용할 인증서의 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="95516-121">클러스터는 Azure Data Lake Store에 액세스할 때 이 기능을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95516-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="95516-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="95516-122">-CertificatePassword</span></span>
<span data-ttu-id="95516-123">서비스 주체로 인증하는 데 사용할 인증서의 암호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="95516-124">클러스터는 Azure Data Lake Store에 액세스할 때 이 기능을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95516-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="95516-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="95516-125">-ClusterTier</span></span>
<span data-ttu-id="95516-126">HDInsight 클러스터 계층을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="95516-127">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="95516-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="95516-128">표준</span><span class="sxs-lookup"><span data-stu-id="95516-128">Standard</span></span>
- <span data-ttu-id="95516-129">Premium 기본값은 Standard입니다.</span><span class="sxs-lookup"><span data-stu-id="95516-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="95516-130">프리미엄 계층은 Linux 클러스터에서만 사용할 수 있으며 몇 가지 새로운 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95516-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="95516-131">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="95516-131">-ClusterType</span></span>
<span data-ttu-id="95516-132">만들 클러스터의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="95516-133">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="95516-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="95516-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="95516-134">Hadoop</span></span>
- <span data-ttu-id="95516-135">HBase</span><span class="sxs-lookup"><span data-stu-id="95516-135">HBase</span></span>
- <span data-ttu-id="95516-136">Storm</span><span class="sxs-lookup"><span data-stu-id="95516-136">Storm</span></span>
- <span data-ttu-id="95516-137">Spark</span><span class="sxs-lookup"><span data-stu-id="95516-137">Spark</span></span>
- <span data-ttu-id="95516-138">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="95516-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="95516-139">Kafka</span><span class="sxs-lookup"><span data-stu-id="95516-139">Kafka</span></span>
- <span data-ttu-id="95516-140">RServer</span><span class="sxs-lookup"><span data-stu-id="95516-140">RServer</span></span>

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

### <span data-ttu-id="95516-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95516-141">-DefaultProfile</span></span>
<span data-ttu-id="95516-142">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="95516-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95516-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="95516-143">-EdgeNodeSize</span></span>
<span data-ttu-id="95516-144">에지 노드에 대한 가상 머신의 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="95516-145">허용 Get-AzVMSize VM 크기에 대한 자세한 내용은 HDInsight의 가격 책정 페이지를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="95516-145">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="95516-146">이 매개 변수는 RServer 클러스터에만 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-146">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="95516-147">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="95516-147">-EncryptionAlgorithm</span></span>
<span data-ttu-id="95516-148">암호화 알고리즘을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-148">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="95516-149">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="95516-149">-EncryptionAtHost</span></span>
<span data-ttu-id="95516-150">호스트에서 암호화를 사용할지 여부를 나타내는 플래그를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-150">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="95516-151">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="95516-151">-EncryptionInTransit</span></span>
<span data-ttu-id="95516-152">전송 중 암호화를 사용할지 여부를 나타내는 플래그를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-152">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="95516-153">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="95516-153">-EncryptionKeyName</span></span>
<span data-ttu-id="95516-154">암호화 키 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-154">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="95516-155">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="95516-155">-EncryptionKeyVersion</span></span>
<span data-ttu-id="95516-156">암호화 키 버전을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-156">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="95516-157">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="95516-157">-EncryptionVaultUri</span></span>
<span data-ttu-id="95516-158">암호화 자격 증명 모음 URI를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-158">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="95516-159">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="95516-159">-HeadNodeSize</span></span>
<span data-ttu-id="95516-160">헤드 노드에 대한 가상 머신의 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-160">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="95516-161">허용 Get-AzVMSize VM 크기에 대한 자세한 내용은 HDInsight의 가격 책정 페이지를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="95516-161">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="95516-162">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="95516-162">-HiveMetastore</span></span>
<span data-ttu-id="95516-163">Hive 메타데이터를 저장할 metastore를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-163">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="95516-164">또는 Add-AzHDInsightMetastore cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95516-164">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="95516-165">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="95516-165">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="95516-166">지원되는 최소 TLS 버전을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-166">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="95516-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="95516-167">-ObjectId</span></span>
<span data-ttu-id="95516-168">클러스터를 나타내는 Azure AD 서비스 주체의 Azure AD 개체 ID(GUID)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-168">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="95516-169">클러스터는 Azure Data Lake Store에 액세스할 때 이 기능을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95516-169">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="95516-170">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="95516-170">-OozieMetastore</span></span>
<span data-ttu-id="95516-171">Oozie 메타데이터를 저장할 metastore를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-171">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="95516-172">또는 **Add-AzHDInsightMetastore** cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95516-172">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="95516-173">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="95516-173">-StorageAccountKey</span></span>
<span data-ttu-id="95516-174">저장소 계정 액세스 키를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-174">Gets or sets the storage account access key.</span></span>

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

### <span data-ttu-id="95516-175">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="95516-175">-StorageAccountResourceId</span></span>
<span data-ttu-id="95516-176">저장소 계정 리소스 ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-176">Gets or sets the storage account resource id.</span></span>

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

### <span data-ttu-id="95516-177">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="95516-177">-StorageAccountType</span></span>
<span data-ttu-id="95516-178">기본 저장소 계정의 유형을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-178">Gets or sets the type of the default storage account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95516-179">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="95516-179">-WorkerNodeSize</span></span>
<span data-ttu-id="95516-180">Worker 노드에 대한 가상 머신의 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-180">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="95516-181">허용 Get-AzVMSize VM 크기에 대한 자세한 내용은 HDInsight의 가격 책정 페이지를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="95516-181">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="95516-182">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="95516-182">-ZookeeperNodeSize</span></span>
<span data-ttu-id="95516-183">Zookeeper 노드에 대한 가상 머신의 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-183">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="95516-184">허용 Get-AzVMSize VM 크기에 대한 자세한 내용은 HDInsight의 가격 책정 페이지를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="95516-184">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="95516-185">이 매개 변수는 HBase 또는 Storm 클러스터에만 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-185">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="95516-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95516-186">CommonParameters</span></span>
<span data-ttu-id="95516-187">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="95516-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95516-188">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="95516-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95516-189">입력</span><span class="sxs-lookup"><span data-stu-id="95516-189">INPUTS</span></span>

### <span data-ttu-id="95516-190">없음</span><span class="sxs-lookup"><span data-stu-id="95516-190">None</span></span>

## <span data-ttu-id="95516-191">출력</span><span class="sxs-lookup"><span data-stu-id="95516-191">OUTPUTS</span></span>

### <span data-ttu-id="95516-192">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="95516-192">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="95516-193">참고 사항</span><span class="sxs-lookup"><span data-stu-id="95516-193">NOTES</span></span>

## <span data-ttu-id="95516-194">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95516-194">RELATED LINKS</span></span>

[<span data-ttu-id="95516-195">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="95516-195">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


