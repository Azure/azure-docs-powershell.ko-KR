---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/set-azhdinsightdefaultstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
ms.openlocfilehash: 9873ba2e4fa4f54c4aa77822af076bb5426ac198
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001515"
---
# <span data-ttu-id="6f8f8-101">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="6f8f8-101">Set-AzHDInsightDefaultStorage</span></span>

## <span data-ttu-id="6f8f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f8f8-102">SYNOPSIS</span></span>
<span data-ttu-id="6f8f8-103">클러스터 구성 개체에서 기본 Storage 계정 설정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6f8f8-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

## <span data-ttu-id="6f8f8-104">구문</span><span class="sxs-lookup"><span data-stu-id="6f8f8-104">SYNTAX</span></span>

```
Set-AzHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountResourceId] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6f8f8-105">설명</span><span class="sxs-lookup"><span data-stu-id="6f8f8-105">DESCRIPTION</span></span>
<span data-ttu-id="6f8f8-106">**Set-AzHDInsightDefaultStorage** cmdlet은 azure HDInsight 클러스터 구성 개체의 기본 Storage 계정 설정을 New-AzHDInsightClusterConfig cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="6f8f8-106">The **Set-AzHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="6f8f8-107">예제</span><span class="sxs-lookup"><span data-stu-id="6f8f8-107">EXAMPLES</span></span>

### <span data-ttu-id="6f8f8-108">예제 1: 클러스터 구성 개체에 대한 기본 저장소 계정 설정</span><span class="sxs-lookup"><span data-stu-id="6f8f8-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageaccountname"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\>$storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Set-AzHDInsightDefaultStorage `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $key2 `
                -StorageContainer $storageContainer `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location
```

<span data-ttu-id="6f8f8-109">이 명령은 클러스터 구성 개체에 대한 기본 Storage 계정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6f8f8-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="6f8f8-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6f8f8-110">PARAMETERS</span></span>

### <span data-ttu-id="6f8f8-111">-Config</span><span class="sxs-lookup"><span data-stu-id="6f8f8-111">-Config</span></span>
<span data-ttu-id="6f8f8-112">이 cmdlet이 수정하는 HDInsight 클러스터 구성 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6f8f8-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="6f8f8-113">이 개체는 **New-AzHDInsightClusterConfig** cmdlet에 의해 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="6f8f8-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="6f8f8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f8f8-114">-DefaultProfile</span></span>
<span data-ttu-id="6f8f8-115">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6f8f8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f8f8-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="6f8f8-116">-StorageAccountKey</span></span>
<span data-ttu-id="6f8f8-117">HDInsight 클러스터에서 사용할 기본 Azure Storage 계정에 대한 계정 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6f8f8-117">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8f8-118">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="6f8f8-118">-StorageAccountResourceId</span></span>
<span data-ttu-id="6f8f8-119">새 클러스터에 추가할 저장소 계정에 대한 저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f8f8-119">The storage account name for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="6f8f8-120">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="6f8f8-120">-StorageAccountType</span></span>
<span data-ttu-id="6f8f8-121">기본 저장소 계정의 형식을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6f8f8-121">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="6f8f8-122">AzureStorage 기본값</span><span class="sxs-lookup"><span data-stu-id="6f8f8-122">Defaults to AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8f8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f8f8-123">CommonParameters</span></span>
<span data-ttu-id="6f8f8-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6f8f8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f8f8-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f8f8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f8f8-126">입력</span><span class="sxs-lookup"><span data-stu-id="6f8f8-126">INPUTS</span></span>

### <span data-ttu-id="6f8f8-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="6f8f8-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="6f8f8-128">출력</span><span class="sxs-lookup"><span data-stu-id="6f8f8-128">OUTPUTS</span></span>

### <span data-ttu-id="6f8f8-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="6f8f8-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="6f8f8-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6f8f8-130">NOTES</span></span>

## <span data-ttu-id="6f8f8-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f8f8-131">RELATED LINKS</span></span>
