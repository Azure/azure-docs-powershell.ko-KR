---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C2AF43D-18BF-4036-A355-FC27E406B18A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
ms.openlocfilehash: 43850e035a59674b06502db1486de0d90fe6e4ba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879818"
---
# <span data-ttu-id="3f102-101">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="3f102-101">Add-AzHDInsightStorage</span></span>

## <span data-ttu-id="3f102-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f102-102">SYNOPSIS</span></span>
<span data-ttu-id="3f102-103">클러스터 구성 개체에 Azure Storage 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f102-103">Adds an Azure Storage key to a cluster configuration object.</span></span>

## <span data-ttu-id="3f102-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3f102-104">SYNTAX</span></span>

```
Add-AzHDInsightStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f102-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3f102-105">DESCRIPTION</span></span>
<span data-ttu-id="3f102-106">**AzHDInsightStorage** cmdlet은 New-AzHDInsightClusterConfig cmdlet에서 만든 azure HDInsight 구성 개체에 azure Storage 계정 항목을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f102-106">The **Add-AzHDInsightStorage** cmdlet adds an Azure Storage account entry to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="3f102-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3f102-107">EXAMPLES</span></span>

### <span data-ttu-id="3f102-108">예제 1: 클러스터 구성 개체에 Azure storage 키 추가</span><span class="sxs-lookup"><span data-stu-id="3f102-108">Example 1: Add an Azure storage key to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
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

# Second storage account info
PS C:\> $secondStorageAccountResourceGroupName = "Group"
PS C:\> $secondStorageAccountName = "yourstorageacct002"
PS C:\> $secondStorageAccountKey = Get-AzStorageAccountKey `
PS C:\> -ResourceGroupName $secondStorageAccountResourceGroupName `
            -Name $secondStorageAccountName | %{ $_.Key1 }

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

<span data-ttu-id="3f102-109">이 명령은-hadoop-001 이라는 HDInsight 구성에 blob 저장소 계정 항목을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f102-109">This command adds an blob storage account entry to the HDInsight configuration named your-hadoop-001.</span></span>

## <span data-ttu-id="3f102-110">변수</span><span class="sxs-lookup"><span data-stu-id="3f102-110">PARAMETERS</span></span>

### <span data-ttu-id="3f102-111">-구성</span><span class="sxs-lookup"><span data-stu-id="3f102-111">-Config</span></span>
<span data-ttu-id="3f102-112">이 cmdlet이 수정 하는 HDInsight 클러스터 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f102-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="3f102-113">이 개체는 **AzHDInsightClusterConfig** cmdlet에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3f102-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="3f102-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f102-114">-DefaultProfile</span></span>
<span data-ttu-id="3f102-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3f102-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f102-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="3f102-116">-StorageAccountKey</span></span>
<span data-ttu-id="3f102-117">새 클러스터에 추가할 저장소 계정에 대 한 저장소 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f102-117">Specifies the storage account key for the storage account to be added to the new cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f102-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3f102-118">-StorageAccountName</span></span>
<span data-ttu-id="3f102-119">클러스터에 추가할 저장소 계정의 저장소 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f102-119">Specifies the storage account name for the storage account to be added to the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f102-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f102-120">CommonParameters</span></span>
<span data-ttu-id="3f102-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f102-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f102-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f102-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f102-123">입력</span><span class="sxs-lookup"><span data-stu-id="3f102-123">INPUTS</span></span>

### <span data-ttu-id="3f102-124">AzureHDInsightConfig의. m m.</span><span class="sxs-lookup"><span data-stu-id="3f102-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="3f102-125">출력</span><span class="sxs-lookup"><span data-stu-id="3f102-125">OUTPUTS</span></span>

### <span data-ttu-id="3f102-126">AzureHDInsightConfig의. m m.</span><span class="sxs-lookup"><span data-stu-id="3f102-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="3f102-127">상속자</span><span class="sxs-lookup"><span data-stu-id="3f102-127">NOTES</span></span>

## <span data-ttu-id="3f102-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f102-128">RELATED LINKS</span></span>

[<span data-ttu-id="3f102-129">새로운 AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="3f102-129">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


