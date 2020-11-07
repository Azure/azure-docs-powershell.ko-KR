---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 38dc23c2bebe3c608833e55bcb4ffb2d687f9041
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879777"
---
# <span data-ttu-id="7656f-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="7656f-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="7656f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7656f-102">SYNOPSIS</span></span>
<span data-ttu-id="7656f-103">Azure HDInsight 클러스터 구성을 설명 하는 유지 되지 않는 클러스터 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="7656f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7656f-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [[-DefaultStorageAccountType] <StorageType>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>] [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>]
 [[-EdgeNodeSize] <String>] [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>] [[-ClusterTier] <Tier>]
 [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>] [[-CertificateFileContents] <Byte[]>]
 [[-CertificateFilePath] <String>] [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>]
 [[-MinSupportedTlsVersion] <String>] [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7656f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7656f-105">DESCRIPTION</span></span>
<span data-ttu-id="7656f-106">**AzHDInsightClusterConfig** Cmdlet은 Azure HDInsight 클러스터 구성을 설명 하는 비지속형 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="7656f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7656f-107">EXAMPLES</span></span>

### <span data-ttu-id="7656f-108">예제 1: 클러스터 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="7656f-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="7656f-109">이 명령은 클러스터 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="7656f-110">변수</span><span class="sxs-lookup"><span data-stu-id="7656f-110">PARAMETERS</span></span>

### <span data-ttu-id="7656f-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="7656f-111">-AadTenantId</span></span>
<span data-ttu-id="7656f-112">Azure Data Lake Store에 액세스할 때 사용 되는 Azure AD 테 넌 트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="7656f-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7656f-113">-ApplicationId</span></span>
<span data-ttu-id="7656f-114">Azure Data Lake에 액세스 하기 위한 서비스 사용자 응용 프로그램 Id를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="7656f-115">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="7656f-115">-CertificateFileContents</span></span>
<span data-ttu-id="7656f-116">Azure Data Lake Store에 액세스할 때 사용 될 인증서의 파일 내용을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-116">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="7656f-117">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="7656f-117">-CertificateFilePath</span></span>
<span data-ttu-id="7656f-118">서비스 사용자로 인증 하는 데 사용 되는 인증서의 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-118">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="7656f-119">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-119">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="7656f-120">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="7656f-120">-CertificatePassword</span></span>
<span data-ttu-id="7656f-121">서비스 사용자로 인증 하는 데 사용 되는 인증서의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-121">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="7656f-122">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-122">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="7656f-123">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="7656f-123">-ClusterTier</span></span>
<span data-ttu-id="7656f-124">HDInsight 클러스터 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-124">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="7656f-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7656f-126">표준이</span><span class="sxs-lookup"><span data-stu-id="7656f-126">Standard</span></span>
- <span data-ttu-id="7656f-127">Premium 기본 값은 표준입니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-127">Premium The default value is Standard.</span></span>
<span data-ttu-id="7656f-128">프리미엄 계층은 Linux 클러스터 에서만 사용할 수 있으며, 몇 가지 새로운 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-128">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="7656f-129">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="7656f-129">-ClusterType</span></span>
<span data-ttu-id="7656f-130">만들 클러스터 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-130">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="7656f-131">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7656f-132">Hadoop</span><span class="sxs-lookup"><span data-stu-id="7656f-132">Hadoop</span></span>
- <span data-ttu-id="7656f-133">HBase</span><span class="sxs-lookup"><span data-stu-id="7656f-133">HBase</span></span>
- <span data-ttu-id="7656f-134">번개가</span><span class="sxs-lookup"><span data-stu-id="7656f-134">Storm</span></span>
- <span data-ttu-id="7656f-135">올리려면</span><span class="sxs-lookup"><span data-stu-id="7656f-135">Spark</span></span>
- <span data-ttu-id="7656f-136">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="7656f-136">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="7656f-137">Kafka</span><span class="sxs-lookup"><span data-stu-id="7656f-137">Kafka</span></span>
- <span data-ttu-id="7656f-138">RServer</span><span class="sxs-lookup"><span data-stu-id="7656f-138">RServer</span></span>

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

### <span data-ttu-id="7656f-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7656f-139">-DefaultProfile</span></span>
<span data-ttu-id="7656f-140">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7656f-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7656f-141">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7656f-141">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="7656f-142">HDInsight 클러스터에서 사용할 기본 Azure 저장소 계정에 대 한 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-142">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="7656f-143">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7656f-143">-DefaultStorageAccountName</span></span>
<span data-ttu-id="7656f-144">HDInsight 클러스터에 사용 되는 기본 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-144">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="7656f-145">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="7656f-145">-DefaultStorageAccountType</span></span>
<span data-ttu-id="7656f-146">HDInsight 클러스터에 사용 되는 기본 저장소 계정의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-146">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="7656f-147">사용할 수 있는 값은 AzureStorage 및 AzureDataLakeStore입니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-147">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="7656f-148">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="7656f-148">-EdgeNodeSize</span></span>
<span data-ttu-id="7656f-149">Edge 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-149">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="7656f-150">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7656f-150">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="7656f-151">이 매개 변수는 RServer 클러스터에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-151">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="7656f-152">-용 Nodesize</span><span class="sxs-lookup"><span data-stu-id="7656f-152">-HeadNodeSize</span></span>
<span data-ttu-id="7656f-153">헤드 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-153">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="7656f-154">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7656f-154">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="7656f-155">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="7656f-155">-HiveMetastore</span></span>
<span data-ttu-id="7656f-156">하이브 메타 데이터를 저장할 metastore를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-156">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="7656f-157">또는 Add-AzHDInsightMetastore cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-157">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="7656f-158">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="7656f-158">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="7656f-159">지원 되는 최소 TLS 버전을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-159">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="7656f-160">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7656f-160">-ObjectId</span></span>
<span data-ttu-id="7656f-161">클러스터를 나타내는 Azure AD 서비스 주체의 Azure AD 개체 ID (GUID)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-161">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="7656f-162">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-162">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="7656f-163">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="7656f-163">-OozieMetastore</span></span>
<span data-ttu-id="7656f-164">Oozie 메타 데이터를 저장할 metastore를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-164">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="7656f-165">또는 **추가-AzHDInsightMetastore** cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-165">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="7656f-166">-. 노드 크기</span><span class="sxs-lookup"><span data-stu-id="7656f-166">-WorkerNodeSize</span></span>
<span data-ttu-id="7656f-167">작업자 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-167">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="7656f-168">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7656f-168">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="7656f-169">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="7656f-169">-ZookeeperNodeSize</span></span>
<span data-ttu-id="7656f-170">사육 사 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-170">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="7656f-171">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7656f-171">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="7656f-172">이 매개 변수는 HBase 또는 폭풍 클러스터에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-172">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="7656f-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7656f-173">CommonParameters</span></span>
<span data-ttu-id="7656f-174">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7656f-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7656f-175">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7656f-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7656f-176">입력</span><span class="sxs-lookup"><span data-stu-id="7656f-176">INPUTS</span></span>

### <span data-ttu-id="7656f-177">않아야</span><span class="sxs-lookup"><span data-stu-id="7656f-177">None</span></span>

## <span data-ttu-id="7656f-178">출력</span><span class="sxs-lookup"><span data-stu-id="7656f-178">OUTPUTS</span></span>

### <span data-ttu-id="7656f-179">AzureHDInsightConfig의. m m.</span><span class="sxs-lookup"><span data-stu-id="7656f-179">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="7656f-180">상속자</span><span class="sxs-lookup"><span data-stu-id="7656f-180">NOTES</span></span>

## <span data-ttu-id="7656f-181">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7656f-181">RELATED LINKS</span></span>

[<span data-ttu-id="7656f-182">추가-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="7656f-182">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


