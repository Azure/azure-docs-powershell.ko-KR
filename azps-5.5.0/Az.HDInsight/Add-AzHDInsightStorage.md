---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C2AF43D-18BF-4036-A355-FC27E406B18A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
ms.openlocfilehash: 6db3c5b5d899f9b7a32e6dbb20c280590bea93c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180601"
---
# <span data-ttu-id="ae0c8-101">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="ae0c8-101">Add-AzHDInsightStorage</span></span>

## <span data-ttu-id="ae0c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae0c8-102">SYNOPSIS</span></span>
<span data-ttu-id="ae0c8-103">클러스터 구성 개체에 Azure Storage 키를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ae0c8-103">Adds an Azure Storage key to a cluster configuration object.</span></span>

## <span data-ttu-id="ae0c8-104">구문</span><span class="sxs-lookup"><span data-stu-id="ae0c8-104">SYNTAX</span></span>

```
Add-AzHDInsightStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae0c8-105">설명</span><span class="sxs-lookup"><span data-stu-id="ae0c8-105">DESCRIPTION</span></span>
<span data-ttu-id="ae0c8-106">**Add-AzHDInsightStorage** cmdlet은 Azure Storage 계정 항목을 New-AzHDInsightClusterConfig cmdlet에서 만든 Azure HDInsight 구성 개체에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ae0c8-106">The **Add-AzHDInsightStorage** cmdlet adds an Azure Storage account entry to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="ae0c8-107">예제</span><span class="sxs-lookup"><span data-stu-id="ae0c8-107">EXAMPLES</span></span>

### <span data-ttu-id="ae0c8-108">예제 1: 클러스터 구성 개체에 Azure 저장소 키 추가</span><span class="sxs-lookup"><span data-stu-id="ae0c8-108">Example 1: Add an Azure storage key to the cluster configuration object</span></span>
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

<span data-ttu-id="ae0c8-109">이 명령은 hadoop-001이라는 HDInsight 구성에 Blob Storage 계정 항목을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ae0c8-109">This command adds an blob storage account entry to the HDInsight configuration named your-hadoop-001.</span></span>

## <span data-ttu-id="ae0c8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae0c8-110">PARAMETERS</span></span>

### <span data-ttu-id="ae0c8-111">-Config</span><span class="sxs-lookup"><span data-stu-id="ae0c8-111">-Config</span></span>
<span data-ttu-id="ae0c8-112">이 cmdlet이 수정하는 HDInsight 클러스터 구성 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ae0c8-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="ae0c8-113">이 개체는 **New-AzHDInsightClusterConfig** cmdlet에 의해 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae0c8-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="ae0c8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae0c8-114">-DefaultProfile</span></span>
<span data-ttu-id="ae0c8-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ae0c8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae0c8-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ae0c8-116">-StorageAccountKey</span></span>
<span data-ttu-id="ae0c8-117">새 클러스터에 추가할 저장소 계정에 대한 저장소 계정 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ae0c8-117">Specifies the storage account key for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="ae0c8-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ae0c8-118">-StorageAccountName</span></span>
<span data-ttu-id="ae0c8-119">클러스터에 추가할 저장소 계정의 저장소 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ae0c8-119">Specifies the storage account name for the storage account to be added to the cluster.</span></span>

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

### <span data-ttu-id="ae0c8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae0c8-120">CommonParameters</span></span>
<span data-ttu-id="ae0c8-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ae0c8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae0c8-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ae0c8-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae0c8-123">입력</span><span class="sxs-lookup"><span data-stu-id="ae0c8-123">INPUTS</span></span>

### <span data-ttu-id="ae0c8-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="ae0c8-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="ae0c8-125">출력</span><span class="sxs-lookup"><span data-stu-id="ae0c8-125">OUTPUTS</span></span>

### <span data-ttu-id="ae0c8-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="ae0c8-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="ae0c8-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ae0c8-127">NOTES</span></span>

## <span data-ttu-id="ae0c8-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae0c8-128">RELATED LINKS</span></span>

[<span data-ttu-id="ae0c8-129">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="ae0c8-129">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


