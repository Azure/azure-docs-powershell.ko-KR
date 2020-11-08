---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 66857c9d12bb23ffdccb893b8fae8bfc7c6e0f4f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049075"
---
# <span data-ttu-id="18c68-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="18c68-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="18c68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18c68-102">SYNOPSIS</span></span>
<span data-ttu-id="18c68-103">Azure HDInsight 클러스터 구성을 설명 하는 유지 되지 않는 클러스터 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="18c68-104">구문과</span><span class="sxs-lookup"><span data-stu-id="18c68-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-MinSupportedTlsVersion <String>]
 [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>]
 [-OutboundPublicNetworkAccessType <String>] [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18c68-105">설명은</span><span class="sxs-lookup"><span data-stu-id="18c68-105">DESCRIPTION</span></span>
<span data-ttu-id="18c68-106">**AzHDInsightClusterConfig** Cmdlet은 Azure HDInsight 클러스터 구성을 설명 하는 비지속형 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="18c68-107">예제의</span><span class="sxs-lookup"><span data-stu-id="18c68-107">EXAMPLES</span></span>

### <span data-ttu-id="18c68-108">예제 1: 클러스터 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="18c68-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
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
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="18c68-109">이 명령은 클러스터 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="18c68-110">변수</span><span class="sxs-lookup"><span data-stu-id="18c68-110">PARAMETERS</span></span>

### <span data-ttu-id="18c68-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="18c68-111">-AadTenantId</span></span>
<span data-ttu-id="18c68-112">Azure Data Lake Store에 액세스할 때 사용 되는 Azure AD 테 넌 트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="18c68-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="18c68-113">-ApplicationId</span></span>
<span data-ttu-id="18c68-114">Azure Data Lake에 액세스 하기 위한 서비스 사용자 응용 프로그램 Id를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="18c68-115">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="18c68-115">-AssignedIdentity</span></span>
<span data-ttu-id="18c68-116">할당 된 id를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-116">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="18c68-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="18c68-117">-CertificateFileContents</span></span>
<span data-ttu-id="18c68-118">Azure Data Lake Store에 액세스할 때 사용 될 인증서의 파일 내용을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="18c68-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="18c68-119">-CertificateFilePath</span></span>
<span data-ttu-id="18c68-120">서비스 사용자로 인증 하는 데 사용 되는 인증서의 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="18c68-121">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="18c68-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="18c68-122">-CertificatePassword</span></span>
<span data-ttu-id="18c68-123">서비스 사용자로 인증 하는 데 사용 되는 인증서의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="18c68-124">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="18c68-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="18c68-125">-ClusterTier</span></span>
<span data-ttu-id="18c68-126">HDInsight 클러스터 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="18c68-127">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="18c68-128">표준이</span><span class="sxs-lookup"><span data-stu-id="18c68-128">Standard</span></span>
- <span data-ttu-id="18c68-129">Premium 기본 값은 표준입니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="18c68-130">프리미엄 계층은 Linux 클러스터 에서만 사용할 수 있으며, 몇 가지 새로운 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="18c68-131">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="18c68-131">-ClusterType</span></span>
<span data-ttu-id="18c68-132">만들 클러스터 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="18c68-133">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="18c68-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="18c68-134">Hadoop</span></span>
- <span data-ttu-id="18c68-135">HBase</span><span class="sxs-lookup"><span data-stu-id="18c68-135">HBase</span></span>
- <span data-ttu-id="18c68-136">번개가</span><span class="sxs-lookup"><span data-stu-id="18c68-136">Storm</span></span>
- <span data-ttu-id="18c68-137">올리려면</span><span class="sxs-lookup"><span data-stu-id="18c68-137">Spark</span></span>
- <span data-ttu-id="18c68-138">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="18c68-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="18c68-139">Kafka</span><span class="sxs-lookup"><span data-stu-id="18c68-139">Kafka</span></span>
- <span data-ttu-id="18c68-140">RServer</span><span class="sxs-lookup"><span data-stu-id="18c68-140">RServer</span></span>

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

### <span data-ttu-id="18c68-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18c68-141">-DefaultProfile</span></span>
<span data-ttu-id="18c68-142">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="18c68-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18c68-143">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="18c68-143">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="18c68-144">HDInsight 클러스터에서 사용할 기본 Azure 저장소 계정에 대 한 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-144">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="18c68-145">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="18c68-145">-DefaultStorageAccountName</span></span>
<span data-ttu-id="18c68-146">HDInsight 클러스터에 사용 되는 기본 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-146">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="18c68-147">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="18c68-147">-DefaultStorageAccountType</span></span>
<span data-ttu-id="18c68-148">HDInsight 클러스터에 사용 되는 기본 저장소 계정의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-148">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="18c68-149">사용할 수 있는 값은 AzureStorage 및 AzureDataLakeStore입니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-149">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18c68-150">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="18c68-150">-EdgeNodeSize</span></span>
<span data-ttu-id="18c68-151">Edge 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-151">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="18c68-152">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="18c68-152">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="18c68-153">이 매개 변수는 RServer 클러스터에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-153">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="18c68-154">-A. 알고리즘</span><span class="sxs-lookup"><span data-stu-id="18c68-154">-EncryptionAlgorithm</span></span>
<span data-ttu-id="18c68-155">암호화 알고리즘을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-155">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="18c68-156">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="18c68-156">-EncryptionAtHost</span></span>
<span data-ttu-id="18c68-157">호스트에서 암호화를 사용할지 여부를 나타내는 플래그를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-157">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="18c68-158">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="18c68-158">-EncryptionInTransit</span></span>
<span data-ttu-id="18c68-159">전송에 암호화를 사용할지 여부를 나타내는 플래그를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-159">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="18c68-160">-A</span><span class="sxs-lookup"><span data-stu-id="18c68-160">-EncryptionKeyName</span></span>
<span data-ttu-id="18c68-161">암호화 키 이름을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-161">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="18c68-162">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="18c68-162">-EncryptionKeyVersion</span></span>
<span data-ttu-id="18c68-163">암호화 키 버전을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-163">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="18c68-164">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="18c68-164">-EncryptionVaultUri</span></span>
<span data-ttu-id="18c68-165">암호화 자격 증명 모음 uri를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-165">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="18c68-166">-용 Nodesize</span><span class="sxs-lookup"><span data-stu-id="18c68-166">-HeadNodeSize</span></span>
<span data-ttu-id="18c68-167">헤드 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-167">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="18c68-168">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="18c68-168">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="18c68-169">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="18c68-169">-HiveMetastore</span></span>
<span data-ttu-id="18c68-170">하이브 메타 데이터를 저장할 metastore를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-170">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="18c68-171">또는 Add-AzHDInsightMetastore cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-171">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="18c68-172">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="18c68-172">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="18c68-173">지원 되는 최소 TLS 버전을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-173">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="18c68-174">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="18c68-174">-ObjectId</span></span>
<span data-ttu-id="18c68-175">클러스터를 나타내는 Azure AD 서비스 주체의 Azure AD 개체 ID (GUID)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-175">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="18c68-176">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-176">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="18c68-177">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="18c68-177">-OozieMetastore</span></span>
<span data-ttu-id="18c68-178">Oozie 메타 데이터를 저장할 metastore를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-178">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="18c68-179">또는 **추가-AzHDInsightMetastore** cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-179">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="18c68-180">-OutboundPublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="18c68-180">-OutboundPublicNetworkAccessType</span></span>
<span data-ttu-id="18c68-181">공용 네트워크에 대 한 아웃 바운드 액세스 형식을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-181">Gets or sets the outbound access type to the public network.</span></span>

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

### <span data-ttu-id="18c68-182">-PublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="18c68-182">-PublicNetworkAccessType</span></span>
<span data-ttu-id="18c68-183">공용 네트워크 액세스 형식을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-183">Gets or sets the public network access type.</span></span>

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

### <span data-ttu-id="18c68-184">-. 노드 크기</span><span class="sxs-lookup"><span data-stu-id="18c68-184">-WorkerNodeSize</span></span>
<span data-ttu-id="18c68-185">작업자 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-185">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="18c68-186">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="18c68-186">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="18c68-187">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="18c68-187">-ZookeeperNodeSize</span></span>
<span data-ttu-id="18c68-188">사육 사 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-188">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="18c68-189">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="18c68-189">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="18c68-190">이 매개 변수는 HBase 또는 폭풍 클러스터에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-190">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="18c68-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18c68-191">CommonParameters</span></span>
<span data-ttu-id="18c68-192">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="18c68-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18c68-193">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="18c68-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18c68-194">입력</span><span class="sxs-lookup"><span data-stu-id="18c68-194">INPUTS</span></span>

### <span data-ttu-id="18c68-195">않아야</span><span class="sxs-lookup"><span data-stu-id="18c68-195">None</span></span>

## <span data-ttu-id="18c68-196">출력</span><span class="sxs-lookup"><span data-stu-id="18c68-196">OUTPUTS</span></span>

### <span data-ttu-id="18c68-197">AzureHDInsightConfig의. m m.</span><span class="sxs-lookup"><span data-stu-id="18c68-197">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="18c68-198">상속자</span><span class="sxs-lookup"><span data-stu-id="18c68-198">NOTES</span></span>

## <span data-ttu-id="18c68-199">관련 링크</span><span class="sxs-lookup"><span data-stu-id="18c68-199">RELATED LINKS</span></span>

[<span data-ttu-id="18c68-200">추가-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="18c68-200">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


