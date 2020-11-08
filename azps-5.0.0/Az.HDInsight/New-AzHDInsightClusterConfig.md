---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 1124136a580d0079690c60e31fe8de8649e3cafb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217841"
---
# <span data-ttu-id="dde0b-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="dde0b-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="dde0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dde0b-102">SYNOPSIS</span></span>
<span data-ttu-id="dde0b-103">Azure HDInsight 클러스터 구성을 설명 하는 유지 되지 않는 클러스터 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="dde0b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dde0b-104">SYNTAX</span></span>

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

## <span data-ttu-id="dde0b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dde0b-105">DESCRIPTION</span></span>
<span data-ttu-id="dde0b-106">**AzHDInsightClusterConfig** Cmdlet은 Azure HDInsight 클러스터 구성을 설명 하는 비지속형 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="dde0b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dde0b-107">EXAMPLES</span></span>

### <span data-ttu-id="dde0b-108">예제 1: 클러스터 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="dde0b-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="dde0b-109">이 명령은 클러스터 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="dde0b-110">변수</span><span class="sxs-lookup"><span data-stu-id="dde0b-110">PARAMETERS</span></span>

### <span data-ttu-id="dde0b-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="dde0b-111">-AadTenantId</span></span>
<span data-ttu-id="dde0b-112">Azure Data Lake Store에 액세스할 때 사용 되는 Azure AD 테 넌 트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="dde0b-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="dde0b-113">-ApplicationId</span></span>
<span data-ttu-id="dde0b-114">Azure Data Lake에 액세스 하기 위한 서비스 사용자 응용 프로그램 Id를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="dde0b-115">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="dde0b-115">-AssignedIdentity</span></span>
<span data-ttu-id="dde0b-116">할당 된 id를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-116">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="dde0b-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="dde0b-117">-CertificateFileContents</span></span>
<span data-ttu-id="dde0b-118">Azure Data Lake Store에 액세스할 때 사용 될 인증서의 파일 내용을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="dde0b-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="dde0b-119">-CertificateFilePath</span></span>
<span data-ttu-id="dde0b-120">서비스 사용자로 인증 하는 데 사용 되는 인증서의 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="dde0b-121">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="dde0b-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="dde0b-122">-CertificatePassword</span></span>
<span data-ttu-id="dde0b-123">서비스 사용자로 인증 하는 데 사용 되는 인증서의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="dde0b-124">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="dde0b-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="dde0b-125">-ClusterTier</span></span>
<span data-ttu-id="dde0b-126">HDInsight 클러스터 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="dde0b-127">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dde0b-128">표준이</span><span class="sxs-lookup"><span data-stu-id="dde0b-128">Standard</span></span>
- <span data-ttu-id="dde0b-129">Premium 기본 값은 표준입니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="dde0b-130">프리미엄 계층은 Linux 클러스터 에서만 사용할 수 있으며, 몇 가지 새로운 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="dde0b-131">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="dde0b-131">-ClusterType</span></span>
<span data-ttu-id="dde0b-132">만들 클러스터 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="dde0b-133">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dde0b-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="dde0b-134">Hadoop</span></span>
- <span data-ttu-id="dde0b-135">HBase</span><span class="sxs-lookup"><span data-stu-id="dde0b-135">HBase</span></span>
- <span data-ttu-id="dde0b-136">번개가</span><span class="sxs-lookup"><span data-stu-id="dde0b-136">Storm</span></span>
- <span data-ttu-id="dde0b-137">올리려면</span><span class="sxs-lookup"><span data-stu-id="dde0b-137">Spark</span></span>
- <span data-ttu-id="dde0b-138">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="dde0b-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="dde0b-139">Kafka</span><span class="sxs-lookup"><span data-stu-id="dde0b-139">Kafka</span></span>
- <span data-ttu-id="dde0b-140">RServer</span><span class="sxs-lookup"><span data-stu-id="dde0b-140">RServer</span></span>

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

### <span data-ttu-id="dde0b-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dde0b-141">-DefaultProfile</span></span>
<span data-ttu-id="dde0b-142">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="dde0b-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dde0b-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="dde0b-143">-EdgeNodeSize</span></span>
<span data-ttu-id="dde0b-144">Edge 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="dde0b-145">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dde0b-145">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="dde0b-146">이 매개 변수는 RServer 클러스터에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-146">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="dde0b-147">-A. 알고리즘</span><span class="sxs-lookup"><span data-stu-id="dde0b-147">-EncryptionAlgorithm</span></span>
<span data-ttu-id="dde0b-148">암호화 알고리즘을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-148">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="dde0b-149">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="dde0b-149">-EncryptionAtHost</span></span>
<span data-ttu-id="dde0b-150">호스트에서 암호화를 사용할지 여부를 나타내는 플래그를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-150">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="dde0b-151">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="dde0b-151">-EncryptionInTransit</span></span>
<span data-ttu-id="dde0b-152">전송에 암호화를 사용할지 여부를 나타내는 플래그를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-152">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="dde0b-153">-A</span><span class="sxs-lookup"><span data-stu-id="dde0b-153">-EncryptionKeyName</span></span>
<span data-ttu-id="dde0b-154">암호화 키 이름을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-154">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="dde0b-155">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="dde0b-155">-EncryptionKeyVersion</span></span>
<span data-ttu-id="dde0b-156">암호화 키 버전을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-156">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="dde0b-157">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="dde0b-157">-EncryptionVaultUri</span></span>
<span data-ttu-id="dde0b-158">암호화 자격 증명 모음 uri를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-158">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="dde0b-159">-용 Nodesize</span><span class="sxs-lookup"><span data-stu-id="dde0b-159">-HeadNodeSize</span></span>
<span data-ttu-id="dde0b-160">헤드 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-160">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="dde0b-161">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dde0b-161">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="dde0b-162">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="dde0b-162">-HiveMetastore</span></span>
<span data-ttu-id="dde0b-163">하이브 메타 데이터를 저장할 metastore를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-163">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="dde0b-164">또는 Add-AzHDInsightMetastore cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-164">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="dde0b-165">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="dde0b-165">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="dde0b-166">지원 되는 최소 TLS 버전을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-166">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="dde0b-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="dde0b-167">-ObjectId</span></span>
<span data-ttu-id="dde0b-168">클러스터를 나타내는 Azure AD 서비스 주체의 Azure AD 개체 ID (GUID)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-168">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="dde0b-169">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-169">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="dde0b-170">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="dde0b-170">-OozieMetastore</span></span>
<span data-ttu-id="dde0b-171">Oozie 메타 데이터를 저장할 metastore를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-171">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="dde0b-172">또는 **추가-AzHDInsightMetastore** cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-172">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="dde0b-173">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="dde0b-173">-StorageAccountKey</span></span>
<span data-ttu-id="dde0b-174">저장소 계정 액세스 키를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-174">Gets or sets the storage account access key.</span></span>

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

### <span data-ttu-id="dde0b-175">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="dde0b-175">-StorageAccountResourceId</span></span>
<span data-ttu-id="dde0b-176">저장소 계정 리소스 id를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-176">Gets or sets the storage account resource id.</span></span>

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

### <span data-ttu-id="dde0b-177">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="dde0b-177">-StorageAccountType</span></span>
<span data-ttu-id="dde0b-178">기본 저장소 계정의 유형을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-178">Gets or sets the type of the default storage account.</span></span>

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

### <span data-ttu-id="dde0b-179">-. 노드 크기</span><span class="sxs-lookup"><span data-stu-id="dde0b-179">-WorkerNodeSize</span></span>
<span data-ttu-id="dde0b-180">작업자 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-180">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="dde0b-181">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dde0b-181">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="dde0b-182">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="dde0b-182">-ZookeeperNodeSize</span></span>
<span data-ttu-id="dde0b-183">사육 사 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-183">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="dde0b-184">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dde0b-184">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="dde0b-185">이 매개 변수는 HBase 또는 폭풍 클러스터에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-185">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="dde0b-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dde0b-186">CommonParameters</span></span>
<span data-ttu-id="dde0b-187">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dde0b-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dde0b-188">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dde0b-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dde0b-189">입력</span><span class="sxs-lookup"><span data-stu-id="dde0b-189">INPUTS</span></span>

### <span data-ttu-id="dde0b-190">않아야</span><span class="sxs-lookup"><span data-stu-id="dde0b-190">None</span></span>

## <span data-ttu-id="dde0b-191">출력</span><span class="sxs-lookup"><span data-stu-id="dde0b-191">OUTPUTS</span></span>

### <span data-ttu-id="dde0b-192">AzureHDInsightConfig의. m m.</span><span class="sxs-lookup"><span data-stu-id="dde0b-192">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="dde0b-193">상속자</span><span class="sxs-lookup"><span data-stu-id="dde0b-193">NOTES</span></span>

## <span data-ttu-id="dde0b-194">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dde0b-194">RELATED LINKS</span></span>

[<span data-ttu-id="dde0b-195">추가-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="dde0b-195">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


