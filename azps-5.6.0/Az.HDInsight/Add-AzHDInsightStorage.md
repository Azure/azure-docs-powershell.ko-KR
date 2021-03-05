---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C2AF43D-18BF-4036-A355-FC27E406B18A
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/add-azhdinsightstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
ms.openlocfilehash: 47e40395d9422610bcf6fbd341141ba6e9eb3a97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990145"
---
# <span data-ttu-id="39603-101">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="39603-101">Add-AzHDInsightStorage</span></span>

## <span data-ttu-id="39603-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39603-102">SYNOPSIS</span></span>
<span data-ttu-id="39603-103">클러스터 구성 개체에 Azure Storage 키를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="39603-103">Adds an Azure Storage key to a cluster configuration object.</span></span>

## <span data-ttu-id="39603-104">구문</span><span class="sxs-lookup"><span data-stu-id="39603-104">SYNTAX</span></span>

```
Add-AzHDInsightStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39603-105">설명</span><span class="sxs-lookup"><span data-stu-id="39603-105">DESCRIPTION</span></span>
<span data-ttu-id="39603-106">**Add-AzHDInsightStorage** cmdlet은 azure HDInsight 구성 개체에 Azure Storage 계정 항목을 New-AzHDInsightClusterConfig cmdlet을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="39603-106">The **Add-AzHDInsightStorage** cmdlet adds an Azure Storage account entry to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="39603-107">예제</span><span class="sxs-lookup"><span data-stu-id="39603-107">EXAMPLES</span></span>

### <span data-ttu-id="39603-108">예제 1: 클러스터 구성 개체에 Azure Storage 키 추가</span><span class="sxs-lookup"><span data-stu-id="39603-108">Example 1: Add an Azure storage key to the cluster configuration object</span></span>
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
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

<span data-ttu-id="39603-109">이 명령은 your-hadoop-001이라는 HDInsight 구성에 Blob Storage 계정 항목을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="39603-109">This command adds an blob storage account entry to the HDInsight configuration named your-hadoop-001.</span></span>

## <span data-ttu-id="39603-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="39603-110">PARAMETERS</span></span>

### <span data-ttu-id="39603-111">-Config</span><span class="sxs-lookup"><span data-stu-id="39603-111">-Config</span></span>
<span data-ttu-id="39603-112">이 cmdlet이 수정하는 HDInsight 클러스터 구성 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39603-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="39603-113">이 개체는 **New-AzHDInsightClusterConfig** cmdlet에 의해 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="39603-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="39603-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39603-114">-DefaultProfile</span></span>
<span data-ttu-id="39603-115">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="39603-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39603-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="39603-116">-StorageAccountKey</span></span>
<span data-ttu-id="39603-117">새 클러스터에 추가할 저장소 계정에 대한 저장소 계정 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39603-117">Specifies the storage account key for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="39603-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="39603-118">-StorageAccountName</span></span>
<span data-ttu-id="39603-119">클러스터에 추가할 저장소 계정의 저장소 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39603-119">Specifies the storage account name for the storage account to be added to the cluster.</span></span>

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

### <span data-ttu-id="39603-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39603-120">CommonParameters</span></span>
<span data-ttu-id="39603-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="39603-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39603-122">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39603-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39603-123">입력</span><span class="sxs-lookup"><span data-stu-id="39603-123">INPUTS</span></span>

### <span data-ttu-id="39603-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="39603-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="39603-125">출력</span><span class="sxs-lookup"><span data-stu-id="39603-125">OUTPUTS</span></span>

### <span data-ttu-id="39603-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="39603-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="39603-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="39603-127">NOTES</span></span>

## <span data-ttu-id="39603-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39603-128">RELATED LINKS</span></span>

[<span data-ttu-id="39603-129">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="39603-129">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


