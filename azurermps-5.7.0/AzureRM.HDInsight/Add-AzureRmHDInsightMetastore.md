---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8BD3B8BD-DC87-4A94-9FCA-611D11D5E065
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightmetastore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightMetastore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightMetastore.md
ms.openlocfilehash: bc9b5a05111fff64b41400093d1f9c1ba3c2df8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529824"
---
# <span data-ttu-id="5935b-101">Add-AzureRmHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="5935b-101">Add-AzureRmHDInsightMetastore</span></span>

## <span data-ttu-id="5935b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5935b-102">SYNOPSIS</span></span>
<span data-ttu-id="5935b-103">클러스터 구성 개체에 Hive 또는 Oozie metastore 역할을 하는 SQL 데이터베이스를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5935b-103">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5935b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5935b-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightMetastore [-Config] <AzureHDInsightConfig> [-MetastoreType] <AzureHDInsightMetastoreType>
 [-SqlAzureServerName] <String> [-DatabaseName] <String> [-Credential] <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5935b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5935b-105">DESCRIPTION</span></span>
<span data-ttu-id="5935b-106">**AzureRmHDInsightMetastore** cmdlet은 New-AzureRmHDInsightClusterConfig cmdlet에서 만든 HDInsight 구성 개체에 Hive 또는 Oozie metastore를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5935b-106">The **Add-AzureRmHDInsightMetastore** cmdlet adds a Hive or Oozie metastore to the HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="5935b-107">Metastore는 Hive, Oozie 또는 두 가지 모두에 대 한 메타 데이터를 저장 하는 데 사용할 수 있는 SQL 데이터베이스입니다.</span><span class="sxs-lookup"><span data-stu-id="5935b-107">A metastore is a SQL Database that can used to store metadata for Hive, Oozie, or both.</span></span>

## <span data-ttu-id="5935b-108">예제의</span><span class="sxs-lookup"><span data-stu-id="5935b-108">EXAMPLES</span></span>

### <span data-ttu-id="5935b-109">예제 1: 클러스터 구성 개체에 SQL 데이터베이스 metastore 추가</span><span class="sxs-lookup"><span data-stu-id="5935b-109">Example 1: Add a SQL database metastore to the cluster configuration object</span></span>
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

# Hive metastore info
PS C:\> $hiveSqlServer = "your-sqlserver-001"
PS C:\> $hiveDb = "your-sqldb-001"
PS C:\> $hiveCreds = Get-Credential

# Oozie metastore info
PS C:\> $oozieSqlServer = "your-sqlserver-001"
PS C:\> $oozieDb = "your-sqldb-002"
PS C:\> $oozieCreds = Get-Credential

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig  `
            | Add-AzureRmHDInsightMetastore `
                -SqlAzureServerName "$oozieSqlServer.database.contoso.net" `
                -DatabaseName $oozieDb `
                -Credential $oozieCreds `
                -MetastoreType OozieMetastore `
            | Add-AzureRmHDInsightMetastore `
                -SqlAzureServerName "$hiveSqlServer.database.contoso.net" `
                -DatabaseName $hiveDb `
                -Credential $hiveCreds `
                -MetastoreType HiveMetastore `
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

<span data-ttu-id="5935b-110">이 명령은-hadoop-001 이라는 클러스터에 SQL 데이터베이스 metastore를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5935b-110">This command adds a SQL database metastore to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="5935b-111">변수</span><span class="sxs-lookup"><span data-stu-id="5935b-111">PARAMETERS</span></span>

### <span data-ttu-id="5935b-112">-구성</span><span class="sxs-lookup"><span data-stu-id="5935b-112">-Config</span></span>
<span data-ttu-id="5935b-113">이 cmdlet이 수정 하는 HDInsight 클러스터 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5935b-113">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="5935b-114">이 개체는 **AzureRmHDInsightClusterConfig** cmdlet에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5935b-114">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="5935b-115">-Credential</span><span class="sxs-lookup"><span data-stu-id="5935b-115">-Credential</span></span>
<span data-ttu-id="5935b-116">AzureSQL Server 데이터베이스에 사용할 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5935b-116">Specifies the credentials to use for the AzureSQL Server database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5935b-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5935b-117">-DatabaseName</span></span>
<span data-ttu-id="5935b-118">AzureSQL 서버 인스턴스에서이 metastore에 사용할 데이터베이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5935b-118">Specifies the database on the AzureSQL Server instance to use for this metastore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5935b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5935b-119">-DefaultProfile</span></span>
<span data-ttu-id="5935b-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5935b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5935b-121">-MetastoreType</span><span class="sxs-lookup"><span data-stu-id="5935b-121">-MetastoreType</span></span>
<span data-ttu-id="5935b-122">Metastore 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5935b-122">Specifies the type of metastore.</span></span>
<span data-ttu-id="5935b-123">사용할 수 있는 값은 HiveMetastore 또는 OozieMetastore입니다.</span><span class="sxs-lookup"><span data-stu-id="5935b-123">Possible values are HiveMetastore or OozieMetastore.</span></span>

```yaml
Type: AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases: 
Accepted values: HiveMetastore, OozieMetastore

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5935b-124">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="5935b-124">-SqlAzureServerName</span></span>
<span data-ttu-id="5935b-125">이 metastore에 사용할 AzureSQL Server 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5935b-125">Specifies the AzureSQL Server instance to use for this metastore.</span></span>

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

### <span data-ttu-id="5935b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5935b-126">CommonParameters</span></span>
<span data-ttu-id="5935b-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5935b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5935b-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5935b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5935b-129">입력</span><span class="sxs-lookup"><span data-stu-id="5935b-129">INPUTS</span></span>

### <span data-ttu-id="5935b-130">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="5935b-130">AzureHDInsightConfig</span></span>
<span data-ttu-id="5935b-131">' Config ' 매개 변수는 파이프라인에서 ' AzureHDInsightConfig ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5935b-131">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="5935b-132">출력</span><span class="sxs-lookup"><span data-stu-id="5935b-132">OUTPUTS</span></span>

### <span data-ttu-id="5935b-133">AzureHDInsightConfig의. m m.</span><span class="sxs-lookup"><span data-stu-id="5935b-133">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="5935b-134">상속자</span><span class="sxs-lookup"><span data-stu-id="5935b-134">NOTES</span></span>

## <span data-ttu-id="5935b-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5935b-135">RELATED LINKS</span></span>

[<span data-ttu-id="5935b-136">새로운 AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="5935b-136">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


