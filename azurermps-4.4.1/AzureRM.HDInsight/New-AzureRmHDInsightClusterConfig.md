---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
ms.openlocfilehash: 381143b356202a7b6b76e173b233f2fffe87f6a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537212"
---
# <span data-ttu-id="39ccc-101">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="39ccc-101">New-AzureRmHDInsightClusterConfig</span></span>

## <span data-ttu-id="39ccc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39ccc-102">SYNOPSIS</span></span>
<span data-ttu-id="39ccc-103">Azure HDInsight 클러스터 구성을 설명 하는 유지 되지 않는 클러스터 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39ccc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="39ccc-104">SYNTAX</span></span>

```
New-AzureRmHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39ccc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="39ccc-105">DESCRIPTION</span></span>
<span data-ttu-id="39ccc-106">**AzureRmHDInsightClusterConfig** Cmdlet은 Azure HDInsight 클러스터 구성을 설명 하는 비지속형 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-106">The **New-AzureRmHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="39ccc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="39ccc-107">EXAMPLES</span></span>

### <span data-ttu-id="39ccc-108">예제 1: 클러스터 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="39ccc-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
            | New-AzureRmHDInsightCluster `
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

<span data-ttu-id="39ccc-109">이 명령은 클러스터 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="39ccc-110">변수</span><span class="sxs-lookup"><span data-stu-id="39ccc-110">PARAMETERS</span></span>

### <span data-ttu-id="39ccc-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="39ccc-111">-AadTenantId</span></span>
<span data-ttu-id="39ccc-112">Azure Data Lake Store에 액세스할 때 사용 되는 Azure AD 테 넌 트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="39ccc-113">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="39ccc-113">-CertificateFileContents</span></span>
<span data-ttu-id="39ccc-114">Azure Data Lake Store에 액세스할 때 사용 될 인증서의 파일 내용을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-114">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="39ccc-115">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="39ccc-115">-CertificateFilePath</span></span>
<span data-ttu-id="39ccc-116">서비스 사용자로 인증 하는 데 사용 되는 인증서의 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-116">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="39ccc-117">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-117">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="39ccc-118">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="39ccc-118">-CertificatePassword</span></span>
<span data-ttu-id="39ccc-119">서비스 사용자로 인증 하는 데 사용 되는 인증서의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-119">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="39ccc-120">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-120">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="39ccc-121">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="39ccc-121">-ClusterTier</span></span>
<span data-ttu-id="39ccc-122">HDInsight 클러스터 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-122">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="39ccc-123">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="39ccc-124">표준이</span><span class="sxs-lookup"><span data-stu-id="39ccc-124">Standard</span></span>
- <span data-ttu-id="39ccc-125">Premium</span><span class="sxs-lookup"><span data-stu-id="39ccc-125">Premium</span></span>

<span data-ttu-id="39ccc-126">기본값은 표준입니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-126">The default value is Standard.</span></span>
<span data-ttu-id="39ccc-127">프리미엄 계층은 Linux 클러스터 에서만 사용할 수 있으며, 몇 가지 새로운 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-127">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="39ccc-128">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="39ccc-128">-ClusterType</span></span>
<span data-ttu-id="39ccc-129">만들 클러스터 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-129">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="39ccc-130">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="39ccc-131">Hadoop</span><span class="sxs-lookup"><span data-stu-id="39ccc-131">Hadoop</span></span>
- <span data-ttu-id="39ccc-132">HBase</span><span class="sxs-lookup"><span data-stu-id="39ccc-132">HBase</span></span>
- <span data-ttu-id="39ccc-133">번개가</span><span class="sxs-lookup"><span data-stu-id="39ccc-133">Storm</span></span>
- <span data-ttu-id="39ccc-134">올리려면</span><span class="sxs-lookup"><span data-stu-id="39ccc-134">Spark</span></span>

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

### <span data-ttu-id="39ccc-135">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="39ccc-135">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="39ccc-136">HDInsight 클러스터에서 사용할 기본 Azure 저장소 계정에 대 한 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-136">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="39ccc-137">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="39ccc-137">-DefaultStorageAccountName</span></span>
<span data-ttu-id="39ccc-138">HDInsight 클러스터에 사용 되는 기본 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-138">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="39ccc-139">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="39ccc-139">-DefaultStorageAccountType</span></span>
<span data-ttu-id="39ccc-140">HDInsight 클러스터에 사용 되는 기본 저장소 계정의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-140">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="39ccc-141">사용할 수 있는 값은 AzureStorage 및 AzureDataLakeStore입니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-141">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="39ccc-142">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="39ccc-142">-EdgeNodeSize</span></span>
<span data-ttu-id="39ccc-143">Edge 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-143">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="39ccc-144">허용 되는 VM 크기에 대해 Get-AzureRmVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="39ccc-144">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="39ccc-145">이 매개 변수는 RServer 클러스터에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-145">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="39ccc-146">-용 Nodesize</span><span class="sxs-lookup"><span data-stu-id="39ccc-146">-HeadNodeSize</span></span>
<span data-ttu-id="39ccc-147">헤드 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-147">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="39ccc-148">허용 되는 VM 크기에 대해 Get-AzureRMVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="39ccc-148">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="39ccc-149">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="39ccc-149">-HiveMetastore</span></span>
<span data-ttu-id="39ccc-150">하이브 메타 데이터를 저장할 metastore를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-150">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="39ccc-151">또는 Add-AzureRmHDInsightMetastore cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-151">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="39ccc-152">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="39ccc-152">-ObjectId</span></span>
<span data-ttu-id="39ccc-153">클러스터를 나타내는 Azure AD 서비스 주체의 Azure AD 개체 ID (GUID)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-153">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="39ccc-154">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-154">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="39ccc-155">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="39ccc-155">-OozieMetastore</span></span>
<span data-ttu-id="39ccc-156">Oozie 메타 데이터를 저장할 metastore를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-156">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="39ccc-157">또는 **추가-AzureRmHDInsightMetastore** cmdlet을 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-157">You can alternatively use the **Add-AzureRmHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="39ccc-158">-. 노드 크기</span><span class="sxs-lookup"><span data-stu-id="39ccc-158">-WorkerNodeSize</span></span>
<span data-ttu-id="39ccc-159">작업자 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-159">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="39ccc-160">허용 되는 VM 크기에 대해 Get-AzureRMVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="39ccc-160">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="39ccc-161">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="39ccc-161">-ZookeeperNodeSize</span></span>
<span data-ttu-id="39ccc-162">사육 사 노드에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-162">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="39ccc-163">허용 되는 VM 크기에 대해 Get-AzureRMVMSize를 사용 하 고 HDInsight의 가격 책정 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="39ccc-163">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="39ccc-164">이 매개 변수는 HBase 또는 폭풍 클러스터에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-164">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="39ccc-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39ccc-165">-DefaultProfile</span></span>
<span data-ttu-id="39ccc-166">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39ccc-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39ccc-167">CommonParameters</span></span>
<span data-ttu-id="39ccc-168">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ccc-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39ccc-169">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39ccc-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39ccc-170">입력</span><span class="sxs-lookup"><span data-stu-id="39ccc-170">INPUTS</span></span>

## <span data-ttu-id="39ccc-171">출력</span><span class="sxs-lookup"><span data-stu-id="39ccc-171">OUTPUTS</span></span>

### <span data-ttu-id="39ccc-172">AzureHDInsightConfig의. m m.</span><span class="sxs-lookup"><span data-stu-id="39ccc-172">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="39ccc-173">상속자</span><span class="sxs-lookup"><span data-stu-id="39ccc-173">NOTES</span></span>

## <span data-ttu-id="39ccc-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39ccc-174">RELATED LINKS</span></span>

[<span data-ttu-id="39ccc-175">추가-AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="39ccc-175">Add-AzureRmHDInsightStorage</span></span>](./Add-AzureRmHDInsightStorage.md)


