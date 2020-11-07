---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/set-azurermhdinsightdefaultstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightDefaultStorage.md
ms.openlocfilehash: 43418937c379ba1ac93b5a2c733028e31eef7318
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702860"
---
# <span data-ttu-id="3eb60-101">Set-AzureRmHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="3eb60-101">Set-AzureRmHDInsightDefaultStorage</span></span>

## <span data-ttu-id="3eb60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3eb60-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb60-103">클러스터 구성 개체에서 기본 저장소 계정 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb60-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3eb60-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3eb60-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3eb60-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3eb60-105">DESCRIPTION</span></span>
<span data-ttu-id="3eb60-106">**AzureRmHDInsightDefaultStorage** cmdlet은 New-AzureRmHDInsightClusterConfig cmdlet에서 만든 Azure HDInsight 클러스터 구성 개체의 기본 저장소 계정 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb60-106">The **Set-AzureRmHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="3eb60-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3eb60-107">EXAMPLES</span></span>

### <span data-ttu-id="3eb60-108">예제 1: 클러스터 구성 개체에 대 한 기본 저장소 계정 설정</span><span class="sxs-lookup"><span data-stu-id="3eb60-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\>$storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRMResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Set-AzureRmHDInsightDefaultStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
                -StorageContainer $storageContainer `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location
```

<span data-ttu-id="3eb60-109">이 명령은 클러스터 구성 개체에 대 한 기본 저장소 계정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb60-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="3eb60-110">변수</span><span class="sxs-lookup"><span data-stu-id="3eb60-110">PARAMETERS</span></span>

### <span data-ttu-id="3eb60-111">-구성</span><span class="sxs-lookup"><span data-stu-id="3eb60-111">-Config</span></span>
<span data-ttu-id="3eb60-112">이 cmdlet이 수정 하는 HDInsight 클러스터 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb60-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="3eb60-113">이 개체는 **AzureRmHDInsightClusterConfig** cmdlet에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3eb60-113">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3eb60-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eb60-114">-DefaultProfile</span></span>
<span data-ttu-id="3eb60-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3eb60-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eb60-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="3eb60-116">-StorageAccountKey</span></span>
<span data-ttu-id="3eb60-117">HDInsight 클러스터에서 사용할 기본 Azure 저장소 계정에 대 한 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb60-117">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eb60-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3eb60-118">-StorageAccountName</span></span>
<span data-ttu-id="3eb60-119">HDInsight 클러스터에 사용 되는 기본 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb60-119">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eb60-120">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="3eb60-120">-StorageAccountType</span></span>
<span data-ttu-id="3eb60-121">기본 저장소 계정의 유형을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb60-121">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="3eb60-122">기본값은 AzureStorage입니다.</span><span class="sxs-lookup"><span data-stu-id="3eb60-122">Defaults to AzureStorage</span></span>

```yaml
Type: StorageType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eb60-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb60-123">CommonParameters</span></span>
<span data-ttu-id="3eb60-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb60-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb60-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eb60-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb60-126">입력</span><span class="sxs-lookup"><span data-stu-id="3eb60-126">INPUTS</span></span>

### <span data-ttu-id="3eb60-127">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="3eb60-127">AzureHDInsightConfig</span></span>
<span data-ttu-id="3eb60-128">' Config ' 매개 변수는 파이프라인에서 ' AzureHDInsightConfig ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb60-128">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="3eb60-129">출력</span><span class="sxs-lookup"><span data-stu-id="3eb60-129">OUTPUTS</span></span>

### <span data-ttu-id="3eb60-130">AzureHDInsightConfig의. m m.</span><span class="sxs-lookup"><span data-stu-id="3eb60-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="3eb60-131">상속자</span><span class="sxs-lookup"><span data-stu-id="3eb60-131">NOTES</span></span>

## <span data-ttu-id="3eb60-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3eb60-132">RELATED LINKS</span></span>

