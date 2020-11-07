---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2C2AF43D-18BF-4036-A355-FC27E406B18A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightStorage.md
ms.openlocfilehash: 2452ef9784b18550569125c47fd5859c260e754e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702527"
---
# <span data-ttu-id="316cc-101">Add-AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="316cc-101">Add-AzureRmHDInsightStorage</span></span>

## <span data-ttu-id="316cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="316cc-102">SYNOPSIS</span></span>
<span data-ttu-id="316cc-103">클러스터 구성 개체에 Azure Storage 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="316cc-103">Adds an Azure Storage key to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="316cc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="316cc-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="316cc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="316cc-105">DESCRIPTION</span></span>
<span data-ttu-id="316cc-106">**AzureRmHDInsightStorage** cmdlet은 New-AzureRmHDInsightClusterConfig cmdlet에서 만든 azure HDInsight 구성 개체에 azure Storage 계정 항목을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="316cc-106">The **Add-AzureRmHDInsightStorage** cmdlet adds an Azure Storage account entry to the Azure HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="316cc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="316cc-107">EXAMPLES</span></span>

### <span data-ttu-id="316cc-108">예제 1: 클러스터 구성 개체에 Azure storage 키 추가</span><span class="sxs-lookup"><span data-stu-id="316cc-108">Example 1: Add an Azure storage key to the cluster configuration object</span></span>
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

# Second storage account info
PS C:\> $secondStorageAccountResourceGroupName = "Group"
PS C:\> $secondStorageAccountName = "yourstorageacct002"
PS C:\> $secondStorageAccountKey = Get-AzureRmStorageAccountKey `
PS C:\> -ResourceGroupName $secondStorageAccountResourceGroupName `
            -Name $secondStorageAccountName | %{ $_.Key1 }

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

<span data-ttu-id="316cc-109">이 명령은-hadoop-001 이라는 HDInsight 구성에 blob 저장소 계정 항목을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="316cc-109">This command adds an blob storage account entry to the HDInsight configuration named your-hadoop-001.</span></span>

## <span data-ttu-id="316cc-110">변수</span><span class="sxs-lookup"><span data-stu-id="316cc-110">PARAMETERS</span></span>

### <span data-ttu-id="316cc-111">-구성</span><span class="sxs-lookup"><span data-stu-id="316cc-111">-Config</span></span>
<span data-ttu-id="316cc-112">이 cmdlet이 수정 하는 HDInsight 클러스터 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="316cc-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="316cc-113">이 개체는 **AzureRmHDInsightClusterConfig** cmdlet에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="316cc-113">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="316cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="316cc-114">-DefaultProfile</span></span>
<span data-ttu-id="316cc-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="316cc-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="316cc-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="316cc-116">-StorageAccountKey</span></span>
<span data-ttu-id="316cc-117">새 클러스터에 추가할 저장소 계정에 대 한 저장소 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="316cc-117">Specifies the storage account key for the storage account to be added to the new cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="316cc-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="316cc-118">-StorageAccountName</span></span>
<span data-ttu-id="316cc-119">클러스터에 추가할 저장소 계정의 저장소 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="316cc-119">Specifies the storage account name for the storage account to be added to the cluster.</span></span>

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

### <span data-ttu-id="316cc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="316cc-120">CommonParameters</span></span>
<span data-ttu-id="316cc-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="316cc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="316cc-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="316cc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="316cc-123">입력</span><span class="sxs-lookup"><span data-stu-id="316cc-123">INPUTS</span></span>

### <span data-ttu-id="316cc-124">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="316cc-124">AzureHDInsightConfig</span></span>
<span data-ttu-id="316cc-125">' Config ' 매개 변수는 파이프라인에서 ' AzureHDInsightConfig ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="316cc-125">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="316cc-126">출력</span><span class="sxs-lookup"><span data-stu-id="316cc-126">OUTPUTS</span></span>

### <span data-ttu-id="316cc-127">AzureHDInsightConfig의. m m.</span><span class="sxs-lookup"><span data-stu-id="316cc-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="316cc-128">상속자</span><span class="sxs-lookup"><span data-stu-id="316cc-128">NOTES</span></span>

## <span data-ttu-id="316cc-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="316cc-129">RELATED LINKS</span></span>

[<span data-ttu-id="316cc-130">새로운 AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="316cc-130">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


