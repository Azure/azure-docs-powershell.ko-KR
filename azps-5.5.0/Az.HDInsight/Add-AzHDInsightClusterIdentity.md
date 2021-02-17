---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightclusteridentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
ms.openlocfilehash: 6d3924f3613d01e515e58e1b35c3640b0447ca06
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209440"
---
# <span data-ttu-id="4b7ac-101">Add-AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="4b7ac-101">Add-AzHDInsightClusterIdentity</span></span>

## <span data-ttu-id="4b7ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b7ac-102">SYNOPSIS</span></span>
<span data-ttu-id="4b7ac-103">클러스터 구성 개체에 클러스터 ID를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ac-103">Adds a cluster identity to a cluster configuration object.</span></span>

## <span data-ttu-id="4b7ac-104">구문</span><span class="sxs-lookup"><span data-stu-id="4b7ac-104">SYNTAX</span></span>

### <span data-ttu-id="4b7ac-105">CertificateFilePath(기본값)</span><span class="sxs-lookup"><span data-stu-id="4b7ac-105">CertificateFilePath (Default)</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [[-ApplicationId] <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b7ac-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="4b7ac-106">CertificateFileContents</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [[-ApplicationId] <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b7ac-107">설명</span><span class="sxs-lookup"><span data-stu-id="4b7ac-107">DESCRIPTION</span></span>
<span data-ttu-id="4b7ac-108">**Add-AzHDInsightClusterIdentity** cmdlet은 클러스터 ID를 클러스터 cmdlet에서 만든 Azure HDInsight 구성 개체에 New-AzHDInsightClusterConfig 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ac-108">The **Add-AzHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="4b7ac-109">예제</span><span class="sxs-lookup"><span data-stu-id="4b7ac-109">EXAMPLES</span></span>

### <span data-ttu-id="4b7ac-110">예제 1: 클러스터 구성 개체에 클러스터 ID 정보 추가</span><span class="sxs-lookup"><span data-stu-id="4b7ac-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value 
PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Cluster Identity values
PS C:\> $tenantId = (Get-AzContext).Tenant.TenantId
PS C:\> $objectId = "<Azure AD Service Principal Object ID>"
PS C:\> $applicationId = "<Azure AD Service Principal Application ID>"
PS C:\> $certificateFilePath = "<Path to Azure AD Service Principal Certificate>"
PS C:\> $certificatePassword = "<Password for Azure AD Service Principal Certificate>"

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightClusterIdentity `
                -AadTenantId $tenantId `
                -ObjectId $objectId `
                -Application $applicationId
                -CertificateFilePath $certificateFilePath `
                -CertificatePassword $certificatePassword `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageAccountContainer
```

<span data-ttu-id="4b7ac-111">이 명령은 클러스터가 Azure Data Lake Store에 액세스할 수 있도록 hadoop-001이라는 클러스터에 클러스터 ID 정보를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ac-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="4b7ac-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b7ac-112">PARAMETERS</span></span>

### <span data-ttu-id="4b7ac-113">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="4b7ac-113">-AadTenantId</span></span>
<span data-ttu-id="4b7ac-114">Azure Data Lake Store에 액세스할 때 사용할 Azure AD 테넌트 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ac-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7ac-115">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="4b7ac-115">-ApplicationId</span></span>
<span data-ttu-id="4b7ac-116">Azure Data Lake에 액세스하기 위한 서비스 주체 애플리케이션 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ac-116">The Service Principal Application Id for accessing Azure Data Lake.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7ac-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="4b7ac-117">-CertificateFileContents</span></span>
<span data-ttu-id="4b7ac-118">Azure Data Lake Store에 액세스할 때 사용할 인증서의 파일 내용을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ac-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: CertificateFileContents
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7ac-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="4b7ac-119">-CertificateFilePath</span></span>
<span data-ttu-id="4b7ac-120">서비스 주체로 인증하는 데 사용할 인증서의 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ac-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="4b7ac-121">클러스터는 Azure Data Lake Store에 액세스할 때 이 기능을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ac-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: CertificateFilePath
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7ac-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="4b7ac-122">-CertificatePassword</span></span>
<span data-ttu-id="4b7ac-123">서비스 주체로 인증하는 데 사용할 인증서의 암호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ac-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="4b7ac-124">클러스터는 Azure Data Lake Store에 액세스할 때 이 기능을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ac-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7ac-125">-Config</span><span class="sxs-lookup"><span data-stu-id="4b7ac-125">-Config</span></span>
<span data-ttu-id="4b7ac-126">이 cmdlet이 수정하는 HDInsight 클러스터 구성 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ac-126">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="4b7ac-127">이 개체는 New-AzHDInsightClusterConfig cmdlet에 의해 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ac-127">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b7ac-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b7ac-128">-DefaultProfile</span></span>
<span data-ttu-id="4b7ac-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4b7ac-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b7ac-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4b7ac-130">-ObjectId</span></span>
<span data-ttu-id="4b7ac-131">클러스터를 나타내는 Azure AD 서비스 주체의 Azure AD 개체 ID(GUID)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ac-131">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="4b7ac-132">클러스터는 Azure Data Lake Store에 액세스할 때 이 기능을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ac-132">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b7ac-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b7ac-133">CommonParameters</span></span>
<span data-ttu-id="4b7ac-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7ac-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b7ac-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4b7ac-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b7ac-136">입력</span><span class="sxs-lookup"><span data-stu-id="4b7ac-136">INPUTS</span></span>

### <span data-ttu-id="4b7ac-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="4b7ac-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

### <span data-ttu-id="4b7ac-138">System.Guid</span><span class="sxs-lookup"><span data-stu-id="4b7ac-138">System.Guid</span></span>

## <span data-ttu-id="4b7ac-139">출력</span><span class="sxs-lookup"><span data-stu-id="4b7ac-139">OUTPUTS</span></span>

### <span data-ttu-id="4b7ac-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="4b7ac-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="4b7ac-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4b7ac-141">NOTES</span></span>

## <span data-ttu-id="4b7ac-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b7ac-142">RELATED LINKS</span></span>

[<span data-ttu-id="4b7ac-143">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="4b7ac-143">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


