---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightClusterIdentity.md
ms.openlocfilehash: fc992b427e0c07b1f9db634f9369c21917ec9556
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711896"
---
# <span data-ttu-id="b08a1-101">Add-AzureRmHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="b08a1-101">Add-AzureRmHDInsightClusterIdentity</span></span>

## <span data-ttu-id="b08a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b08a1-102">SYNOPSIS</span></span>
<span data-ttu-id="b08a1-103">클러스터 구성 개체에 클러스터 id를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b08a1-103">Adds a cluster identity to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b08a1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b08a1-104">SYNTAX</span></span>

### <span data-ttu-id="b08a1-105">CertificateFilePath (기본값)</span><span class="sxs-lookup"><span data-stu-id="b08a1-105">CertificateFilePath (Default)</span></span>
```
Add-AzureRmHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b08a1-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="b08a1-106">CertificateFileContents</span></span>
```
Add-AzureRmHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b08a1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b08a1-107">DESCRIPTION</span></span>
<span data-ttu-id="b08a1-108">**AzureRmHDInsightClusterIdentity** cmdlet은 New-AzureRmHDInsightClusterConfig cmdlet에서 만든 Azure HDInsight 구성 개체에 클러스터 id를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b08a1-108">The **Add-AzureRmHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="b08a1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b08a1-109">EXAMPLES</span></span>

### <span data-ttu-id="b08a1-110">예제 1: 클러스터 구성 개체에 클러스터 Id 정보 추가</span><span class="sxs-lookup"><span data-stu-id="b08a1-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value 
PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Cluster Identity values
PS C:\> $tenantId = (Get-AzureRmContext).Tenant.TenantId
PS C:\> $objectId = "<Azure AD Service Principal Object ID>"
PS C:\> $certificateFilePath = "<Path to Azure AD Service Principal Certificate>"
PS C:\> $certificatePassword = "<Password for Azure AD Service Principal Certificate>"

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightClusterIdentity `
                -AadTenantId $tenantId `
                -ObjectId $objectId `
                -CertificateFilePath $certificateFilePath `
                -CertificatePassword $certificatePassword `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageAccountContainer
```

<span data-ttu-id="b08a1-111">이 명령은 클러스터 Id 정보를 클러스터에 추가 하 여 클러스터에서 Azure Data Lake Store에 액세스할 수 있도록 합니다 (--001).</span><span class="sxs-lookup"><span data-stu-id="b08a1-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="b08a1-112">변수</span><span class="sxs-lookup"><span data-stu-id="b08a1-112">PARAMETERS</span></span>

### <span data-ttu-id="b08a1-113">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="b08a1-113">-AadTenantId</span></span>
<span data-ttu-id="b08a1-114">Azure Data Lake Store에 액세스할 때 사용 되는 Azure AD 테 넌 트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b08a1-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="b08a1-115">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="b08a1-115">-CertificateFileContents</span></span>
<span data-ttu-id="b08a1-116">Azure Data Lake Store에 액세스할 때 사용 될 인증서의 파일 내용을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b08a1-116">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="b08a1-117">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="b08a1-117">-CertificateFilePath</span></span>
<span data-ttu-id="b08a1-118">서비스 사용자로 인증 하는 데 사용 되는 인증서의 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b08a1-118">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="b08a1-119">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b08a1-119">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="b08a1-120">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="b08a1-120">-CertificatePassword</span></span>
<span data-ttu-id="b08a1-121">서비스 사용자로 인증 하는 데 사용 되는 인증서의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b08a1-121">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="b08a1-122">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b08a1-122">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="b08a1-123">-구성</span><span class="sxs-lookup"><span data-stu-id="b08a1-123">-Config</span></span>
<span data-ttu-id="b08a1-124">이 cmdlet이 수정 하는 HDInsight 클러스터 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b08a1-124">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="b08a1-125">이 개체는 New-AzureRmHDInsightClusterConfig cmdlet에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b08a1-125">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="b08a1-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b08a1-126">-ObjectId</span></span>
<span data-ttu-id="b08a1-127">클러스터를 나타내는 Azure AD 서비스 주체의 Azure AD 개체 ID (GUID)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b08a1-127">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="b08a1-128">클러스터는 Azure Data Lake Store에 액세스할 때이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b08a1-128">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="b08a1-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b08a1-129">-DefaultProfile</span></span>
<span data-ttu-id="b08a1-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b08a1-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b08a1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b08a1-131">CommonParameters</span></span>
<span data-ttu-id="b08a1-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b08a1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b08a1-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b08a1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b08a1-134">입력</span><span class="sxs-lookup"><span data-stu-id="b08a1-134">INPUTS</span></span>

### <span data-ttu-id="b08a1-135">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="b08a1-135">AzureHDInsightConfig</span></span>
<span data-ttu-id="b08a1-136">' Config ' 매개 변수는 파이프라인에서 ' AzureHDInsightConfig ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b08a1-136">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

### <span data-ttu-id="b08a1-137">Shap</span><span class="sxs-lookup"><span data-stu-id="b08a1-137">Guid</span></span>
<span data-ttu-id="b08a1-138">' ObjectId ' 매개 변수는 파이프라인에서 ' Guid ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b08a1-138">Parameter 'ObjectId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="b08a1-139">출력</span><span class="sxs-lookup"><span data-stu-id="b08a1-139">OUTPUTS</span></span>

### <span data-ttu-id="b08a1-140">AzureHDInsightConfig의. m m.</span><span class="sxs-lookup"><span data-stu-id="b08a1-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="b08a1-141">상속자</span><span class="sxs-lookup"><span data-stu-id="b08a1-141">NOTES</span></span>

## <span data-ttu-id="b08a1-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b08a1-142">RELATED LINKS</span></span>

[<span data-ttu-id="b08a1-143">새로운 AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="b08a1-143">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


