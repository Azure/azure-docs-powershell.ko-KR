---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: fad988977cf5fe24e440d654206e0f1a212be6b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868249"
---
# <span data-ttu-id="d652c-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="d652c-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="d652c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d652c-102">SYNOPSIS</span></span>
<span data-ttu-id="d652c-103">Azure HDInsight 클러스터 구성을 설명 하는 유지 되지 않는 클러스터 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="d652c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d652c-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d652c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d652c-105">DESCRIPTION</span></span>
<span data-ttu-id="d652c-106">**AzHDInsightClusterConfig** Cmdlet은 Azure HDInsight 클러스터 구성을 설명 하는 비지속형 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="d652c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d652c-107">EXAMPLES</span></span>

### <span data-ttu-id="d652c-108">예제 1: 클러스터 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="d652c-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="d652c-109">이 명령은 클러스터 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="d652c-110">변수</span><span class="sxs-lookup"><span data-stu-id="d652c-110">PARAMETERS</span></span>

### <span data-ttu-id="d652c-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="d652c-111">-AadTenantId</span></span>
<span data-ttu-id="d652c-112">Azure Data Lake Store에 액세스할 때 사용 되는 Azure AD 테 넌 트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="d652c-113">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="d652c-113">-CertificateFileContents</span></span>
<span data-ttu-id="d652c-114">Azure Data Lake Store에 액세스할 때 사용 될 인증서의 파일 내용을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-114">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="d652c-115">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="d652c-115">-CertificateFilePath</span></span>
<span data-ttu-id="d652c-116">서비스 사용자로 인증 하는 데 사용 되는 인증서의 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-116">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="d652c-117">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-117">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="d652c-118">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="d652c-118">-CertificatePassword</span></span>
<span data-ttu-id="d652c-119">서비스 사용자로 인증 하는 데 사용 되는 인증서의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-119">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="d652c-120">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-120">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="d652c-121">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="d652c-121">-ClusterTier</span></span>
<span data-ttu-id="d652c-122">HDInsight 클러스터 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-122">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="d652c-123">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d652c-124">표준이</span><span class="sxs-lookup"><span data-stu-id="d652c-124">Standard</span></span>
- <span data-ttu-id="d652c-125">Premium 기본 값은 표준입니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-125">Premium The default value is Standard.</span></span>
<span data-ttu-id="d652c-126">프리미엄 계층은 Linux 클러스터 에서만 사용할 수 있으며, 몇 가지 새로운 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-126">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="d652c-127">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="d652c-127">-ClusterType</span></span>
<span data-ttu-id="d652c-128">만들 클러스터 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-128">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="d652c-129">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d652c-130">Hadoop</span><span class="sxs-lookup"><span data-stu-id="d652c-130">Hadoop</span></span>
- <span data-ttu-id="d652c-131">HBase</span><span class="sxs-lookup"><span data-stu-id="d652c-131">HBase</span></span>
- <span data-ttu-id="d652c-132">번개가</span><span class="sxs-lookup"><span data-stu-id="d652c-132">Storm</span></span>
- <span data-ttu-id="d652c-133">올리려면</span><span class="sxs-lookup"><span data-stu-id="d652c-133">Spark</span></span>

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

### <span data-ttu-id="d652c-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d652c-134">-DefaultProfile</span></span>
<span data-ttu-id="d652c-135">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d652c-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d652c-136">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d652c-136">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="d652c-137">HDInsight 클러스터에서 사용할 기본 Azure 저장소 계정에 대 한 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-137">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="d652c-138">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d652c-138">-DefaultStorageAccountName</span></span>
<span data-ttu-id="d652c-139">HDInsight 클러스터에 사용 되는 기본 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-139">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="d652c-140">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="d652c-140">-DefaultStorageAccountType</span></span>
<span data-ttu-id="d652c-141">HDInsight 클러스터에 사용 되는 기본 저장소 계정의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-141">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="d652c-142">사용할 수 있는 값은 AzureStorage 및 AzureDataLakeStore입니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-142">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="d652c-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="d652c-143">-EdgeNodeSize</span></span>
<span data-ttu-id="d652c-144">Edge 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="d652c-145">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d652c-145">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="d652c-146">이 매개 변수는 RServer 클러스터에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-146">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="d652c-147">-용 Nodesize</span><span class="sxs-lookup"><span data-stu-id="d652c-147">-HeadNodeSize</span></span>
<span data-ttu-id="d652c-148">헤드 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-148">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="d652c-149">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d652c-149">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="d652c-150">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="d652c-150">-HiveMetastore</span></span>
<span data-ttu-id="d652c-151">하이브 메타 데이터를 저장할 metastore를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-151">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="d652c-152">또는 Add-AzHDInsightMetastore cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-152">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="d652c-153">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d652c-153">-ObjectId</span></span>
<span data-ttu-id="d652c-154">클러스터를 나타내는 Azure AD 서비스 주체의 Azure AD 개체 ID (GUID)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-154">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="d652c-155">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-155">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="d652c-156">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="d652c-156">-OozieMetastore</span></span>
<span data-ttu-id="d652c-157">Oozie 메타 데이터를 저장할 metastore를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-157">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="d652c-158">또는 **추가-AzHDInsightMetastore** cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-158">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="d652c-159">-. 노드 크기</span><span class="sxs-lookup"><span data-stu-id="d652c-159">-WorkerNodeSize</span></span>
<span data-ttu-id="d652c-160">작업자 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-160">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="d652c-161">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d652c-161">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="d652c-162">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="d652c-162">-ZookeeperNodeSize</span></span>
<span data-ttu-id="d652c-163">사육 사 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-163">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="d652c-164">허용 되는 VM 크기에 대해 Get-AzVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d652c-164">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="d652c-165">이 매개 변수는 HBase 또는 폭풍 클러스터에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-165">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="d652c-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d652c-166">CommonParameters</span></span>
<span data-ttu-id="d652c-167">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d652c-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d652c-168">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d652c-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d652c-169">입력</span><span class="sxs-lookup"><span data-stu-id="d652c-169">INPUTS</span></span>

### <span data-ttu-id="d652c-170">않아야</span><span class="sxs-lookup"><span data-stu-id="d652c-170">None</span></span>

## <span data-ttu-id="d652c-171">출력</span><span class="sxs-lookup"><span data-stu-id="d652c-171">OUTPUTS</span></span>

### <span data-ttu-id="d652c-172">AzureHDInsightConfig의. m m.</span><span class="sxs-lookup"><span data-stu-id="d652c-172">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="d652c-173">상속자</span><span class="sxs-lookup"><span data-stu-id="d652c-173">NOTES</span></span>

## <span data-ttu-id="d652c-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d652c-174">RELATED LINKS</span></span>

[<span data-ttu-id="d652c-175">추가-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="d652c-175">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


