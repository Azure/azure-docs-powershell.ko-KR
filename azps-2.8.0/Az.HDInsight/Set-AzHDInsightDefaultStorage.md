---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightdefaultstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
ms.openlocfilehash: 6815e697376f51d70782885485541debb209ecf7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689789"
---
# <span data-ttu-id="40580-101">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="40580-101">Set-AzHDInsightDefaultStorage</span></span>

## <span data-ttu-id="40580-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40580-102">SYNOPSIS</span></span>
<span data-ttu-id="40580-103">클러스터 구성 개체에서 기본 저장소 계정 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40580-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

## <span data-ttu-id="40580-104">구문과</span><span class="sxs-lookup"><span data-stu-id="40580-104">SYNTAX</span></span>

```
Set-AzHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40580-105">설명은</span><span class="sxs-lookup"><span data-stu-id="40580-105">DESCRIPTION</span></span>
<span data-ttu-id="40580-106">**AzHDInsightDefaultStorage** cmdlet은 New-AzHDInsightClusterConfig cmdlet에서 만든 Azure HDInsight 클러스터 구성 개체의 기본 저장소 계정 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40580-106">The **Set-AzHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="40580-107">예제의</span><span class="sxs-lookup"><span data-stu-id="40580-107">EXAMPLES</span></span>

### <span data-ttu-id="40580-108">예제 1: 클러스터 구성 개체에 대 한 기본 저장소 계정 설정</span><span class="sxs-lookup"><span data-stu-id="40580-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
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
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
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

<span data-ttu-id="40580-109">이 명령은 클러스터 구성 개체에 대 한 기본 저장소 계정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40580-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="40580-110">변수</span><span class="sxs-lookup"><span data-stu-id="40580-110">PARAMETERS</span></span>

### <span data-ttu-id="40580-111">-구성</span><span class="sxs-lookup"><span data-stu-id="40580-111">-Config</span></span>
<span data-ttu-id="40580-112">이 cmdlet이 수정 하는 HDInsight 클러스터 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40580-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="40580-113">이 개체는 **AzHDInsightClusterConfig** cmdlet에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="40580-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="40580-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40580-114">-DefaultProfile</span></span>
<span data-ttu-id="40580-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="40580-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40580-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="40580-116">-StorageAccountKey</span></span>
<span data-ttu-id="40580-117">HDInsight 클러스터에서 사용할 기본 Azure 저장소 계정에 대 한 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40580-117">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="40580-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="40580-118">-StorageAccountName</span></span>
<span data-ttu-id="40580-119">HDInsight 클러스터에 사용 되는 기본 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40580-119">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="40580-120">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="40580-120">-StorageAccountType</span></span>
<span data-ttu-id="40580-121">기본 저장소 계정의 유형을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40580-121">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="40580-122">기본값은 AzureStorage입니다.</span><span class="sxs-lookup"><span data-stu-id="40580-122">Defaults to AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40580-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40580-123">CommonParameters</span></span>
<span data-ttu-id="40580-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="40580-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40580-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40580-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40580-126">입력</span><span class="sxs-lookup"><span data-stu-id="40580-126">INPUTS</span></span>

### <span data-ttu-id="40580-127">AzureHDInsightConfig의. m m.</span><span class="sxs-lookup"><span data-stu-id="40580-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="40580-128">출력</span><span class="sxs-lookup"><span data-stu-id="40580-128">OUTPUTS</span></span>

### <span data-ttu-id="40580-129">AzureHDInsightConfig의. m m.</span><span class="sxs-lookup"><span data-stu-id="40580-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="40580-130">상속자</span><span class="sxs-lookup"><span data-stu-id="40580-130">NOTES</span></span>

## <span data-ttu-id="40580-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40580-131">RELATED LINKS</span></span>
