---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: b5ae1de58a7c3862379e73e852d7b367063c3629
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009024"
---
# <span data-ttu-id="18cda-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="18cda-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="18cda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18cda-102">SYNOPSIS</span></span>
<span data-ttu-id="18cda-103">Azure HDInsight 클러스터 구성을 설명하는 지속되지 않는 클러스터 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="18cda-104">구문</span><span class="sxs-lookup"><span data-stu-id="18cda-104">SYNTAX</span></span>

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

## <span data-ttu-id="18cda-105">설명</span><span class="sxs-lookup"><span data-stu-id="18cda-105">DESCRIPTION</span></span>
<span data-ttu-id="18cda-106">**New-AzHDInsightClusterConfig** cmdlet은 Azure HDInsight 클러스터 구성을 설명하는 지속되지 않는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="18cda-107">예제</span><span class="sxs-lookup"><span data-stu-id="18cda-107">EXAMPLES</span></span>

### <span data-ttu-id="18cda-108">예제 1: 클러스터 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="18cda-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="18cda-109">이 명령은 클러스터 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="18cda-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="18cda-110">PARAMETERS</span></span>

### <span data-ttu-id="18cda-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="18cda-111">-AadTenantId</span></span>
<span data-ttu-id="18cda-112">Azure Data Lake Store에 액세스할 때 사용할 Azure AD 테넌트 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="18cda-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="18cda-113">-ApplicationId</span></span>
<span data-ttu-id="18cda-114">Azure Data Lake에 액세스하기 위해 서비스 주체 애플리케이션 ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="18cda-115">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="18cda-115">-AssignedIdentity</span></span>
<span data-ttu-id="18cda-116">할당된 ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-116">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="18cda-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="18cda-117">-CertificateFileContents</span></span>
<span data-ttu-id="18cda-118">Azure Data Lake Store에 액세스할 때 사용할 인증서의 파일 콘텐츠를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="18cda-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="18cda-119">-CertificateFilePath</span></span>
<span data-ttu-id="18cda-120">서비스 주체로 인증하는 데 사용할 인증서에 대한 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="18cda-121">클러스터는 Azure Data Lake Store에 액세스할 때 이 기능을 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="18cda-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="18cda-122">-CertificatePassword</span></span>
<span data-ttu-id="18cda-123">서비스 주체로 인증하는 데 사용할 인증서에 대한 암호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="18cda-124">클러스터는 Azure Data Lake Store에 액세스할 때 이 기능을 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="18cda-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="18cda-125">-ClusterTier</span></span>
<span data-ttu-id="18cda-126">HDInsight 클러스터 계층을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="18cda-127">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="18cda-128">표준</span><span class="sxs-lookup"><span data-stu-id="18cda-128">Standard</span></span>
- <span data-ttu-id="18cda-129">Premium 기본값은 Standard입니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="18cda-130">Premium 계층은 Linux 클러스터에서만 사용할 수 있으며, 일부 새 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="18cda-131">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="18cda-131">-ClusterType</span></span>
<span data-ttu-id="18cda-132">만들 클러스터 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="18cda-133">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="18cda-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="18cda-134">Hadoop</span></span>
- <span data-ttu-id="18cda-135">HBase</span><span class="sxs-lookup"><span data-stu-id="18cda-135">HBase</span></span>
- <span data-ttu-id="18cda-136">Storm</span><span class="sxs-lookup"><span data-stu-id="18cda-136">Storm</span></span>
- <span data-ttu-id="18cda-137">Spark</span><span class="sxs-lookup"><span data-stu-id="18cda-137">Spark</span></span>
- <span data-ttu-id="18cda-138">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="18cda-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="18cda-139">Kafka</span><span class="sxs-lookup"><span data-stu-id="18cda-139">Kafka</span></span>
- <span data-ttu-id="18cda-140">RServer</span><span class="sxs-lookup"><span data-stu-id="18cda-140">RServer</span></span>

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

### <span data-ttu-id="18cda-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18cda-141">-DefaultProfile</span></span>
<span data-ttu-id="18cda-142">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="18cda-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18cda-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="18cda-143">-EdgeNodeSize</span></span>
<span data-ttu-id="18cda-144">에지 노드에 대한 가상 머신의 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="18cda-145">허용 Get-AzVMSize VM 크기에 대한 사용 및 HDInsight의 가격 책정 페이지를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="18cda-145">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="18cda-146">이 매개 변수는 RServer 클러스터에만 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-146">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="18cda-147">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="18cda-147">-EncryptionAlgorithm</span></span>
<span data-ttu-id="18cda-148">암호화 알고리즘을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-148">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="18cda-149">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="18cda-149">-EncryptionAtHost</span></span>
<span data-ttu-id="18cda-150">호스트에서 암호화를 사용하도록 설정하는지 여부를 나타내는 플래그를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-150">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="18cda-151">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="18cda-151">-EncryptionInTransit</span></span>
<span data-ttu-id="18cda-152">전송 중 암호화를 사용하도록 설정하는지 여부를 나타내는 플래그를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-152">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="18cda-153">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="18cda-153">-EncryptionKeyName</span></span>
<span data-ttu-id="18cda-154">암호화 키 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-154">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="18cda-155">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="18cda-155">-EncryptionKeyVersion</span></span>
<span data-ttu-id="18cda-156">암호화 키 버전을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-156">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="18cda-157">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="18cda-157">-EncryptionVaultUri</span></span>
<span data-ttu-id="18cda-158">암호화 자격 증명 모음 uri를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-158">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="18cda-159">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="18cda-159">-HeadNodeSize</span></span>
<span data-ttu-id="18cda-160">헤드 노드에 대한 가상 머신의 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-160">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="18cda-161">허용 Get-AzVMSize VM 크기에 대한 사용 및 HDInsight의 가격 책정 페이지를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="18cda-161">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="18cda-162">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="18cda-162">-HiveMetastore</span></span>
<span data-ttu-id="18cda-163">Hive 메타데이터를 저장할 메타스토어를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-163">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="18cda-164">또는 cmdlet을 Add-AzHDInsightMetastore 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-164">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="18cda-165">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="18cda-165">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="18cda-166">지원되는 최소 TLS 버전을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-166">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="18cda-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="18cda-167">-ObjectId</span></span>
<span data-ttu-id="18cda-168">클러스터를 나타내는 Azure AD 서비스 주체의 AZURE AD 개체 ID(GUID)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-168">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="18cda-169">클러스터는 Azure Data Lake Store에 액세스할 때 이 기능을 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-169">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="18cda-170">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="18cda-170">-OozieMetastore</span></span>
<span data-ttu-id="18cda-171">Oozie 메타데이터를 저장할 메타스토어를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-171">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="18cda-172">또는 **Add-AzHDInsightMetastore cmdlet을** 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-172">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="18cda-173">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="18cda-173">-StorageAccountKey</span></span>
<span data-ttu-id="18cda-174">저장소 계정 액세스 키를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-174">Gets or sets the storage account access key.</span></span>

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

### <span data-ttu-id="18cda-175">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="18cda-175">-StorageAccountResourceId</span></span>
<span data-ttu-id="18cda-176">저장소 계정 리소스 ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-176">Gets or sets the storage account resource id.</span></span>

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

### <span data-ttu-id="18cda-177">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="18cda-177">-StorageAccountType</span></span>
<span data-ttu-id="18cda-178">기본 저장소 계정의 형식을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-178">Gets or sets the type of the default storage account.</span></span>

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

### <span data-ttu-id="18cda-179">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="18cda-179">-WorkerNodeSize</span></span>
<span data-ttu-id="18cda-180">Worker 노드에 대한 가상 머신 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-180">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="18cda-181">허용 Get-AzVMSize VM 크기에 대한 사용 및 HDInsight의 가격 책정 페이지를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="18cda-181">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="18cda-182">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="18cda-182">-ZookeeperNodeSize</span></span>
<span data-ttu-id="18cda-183">Zookeeper 노드에 대한 가상 머신 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-183">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="18cda-184">허용 Get-AzVMSize VM 크기에 대한 사용 및 HDInsight의 가격 책정 페이지를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="18cda-184">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="18cda-185">이 매개 변수는 HBase 또는 Storm 클러스터에만 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-185">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="18cda-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18cda-186">CommonParameters</span></span>
<span data-ttu-id="18cda-187">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="18cda-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18cda-188">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18cda-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18cda-189">입력</span><span class="sxs-lookup"><span data-stu-id="18cda-189">INPUTS</span></span>

### <span data-ttu-id="18cda-190">없음</span><span class="sxs-lookup"><span data-stu-id="18cda-190">None</span></span>

## <span data-ttu-id="18cda-191">출력</span><span class="sxs-lookup"><span data-stu-id="18cda-191">OUTPUTS</span></span>

### <span data-ttu-id="18cda-192">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="18cda-192">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="18cda-193">참고 사항</span><span class="sxs-lookup"><span data-stu-id="18cda-193">NOTES</span></span>

## <span data-ttu-id="18cda-194">관련 링크</span><span class="sxs-lookup"><span data-stu-id="18cda-194">RELATED LINKS</span></span>

[<span data-ttu-id="18cda-195">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="18cda-195">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


