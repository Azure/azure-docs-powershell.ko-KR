---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 774848C9-47A1-4C43-B6FA-B3C0C3C76470
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightcomponentversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightComponentVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightComponentVersion.md
ms.openlocfilehash: 868ab69420cac66e911d772f4362e70ec2c03a1d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048259"
---
# <span data-ttu-id="9b5e6-101">Add-AzHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="9b5e6-101">Add-AzHDInsightComponentVersion</span></span>

## <span data-ttu-id="9b5e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b5e6-102">SYNOPSIS</span></span>
<span data-ttu-id="9b5e6-103">클러스터에서 실행 되는 서비스의 버전을 클러스터 구성 개체에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b5e6-103">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

## <span data-ttu-id="9b5e6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9b5e6-104">SYNTAX</span></span>

```
Add-AzHDInsightComponentVersion [-Config] <AzureHDInsightConfig> [-ComponentName] <String>
 [-ComponentVersion] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b5e6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9b5e6-105">DESCRIPTION</span></span>
<span data-ttu-id="9b5e6-106">Add-AzHDInsightComponentVersion cmdlet은 클러스터에서 실행 되는 서비스의 버전을 New-AzHDInsightClusterConfig cmdlet에서 만든 Azure HDInsight 구성 개체에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b5e6-106">The Add-AzHDInsightComponentVersion cmdlet adds a version for a service running in a cluster to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="9b5e6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9b5e6-107">EXAMPLES</span></span>

### <span data-ttu-id="9b5e6-108">예제 1: Spark에 대 한 버전을 클러스터 구성 개체에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b5e6-108">Example 1: Add a version for Spark to the cluster configuration object.</span></span>
```
PS C:\> # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container001"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-spark-001"
        $clusterCreds = Get-Credential
        $sshClusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        #   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightClusterConfig `
            | Add-AzHDInsightComponentVersion `
                -ComponentName "Spark" `
                -ComponentVersion "2.0" `
            | New-AzHDInsightCluster `
                -ClusterType Spark `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer `
                -SshCredential $sshCredentials `
                -Version "3.5"
```

<span data-ttu-id="9b5e6-109">이 명령은 ' 사용자의 spark-001 ' 이라는 HDInsight 클러스터에 Spark 버전을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b5e6-109">This command adds the version of Spark to the HDInsight cluster named 'your-spark-001'.</span></span>

## <span data-ttu-id="9b5e6-110">변수</span><span class="sxs-lookup"><span data-stu-id="9b5e6-110">PARAMETERS</span></span>

### <span data-ttu-id="9b5e6-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="9b5e6-111">-ComponentName</span></span>
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

### <span data-ttu-id="9b5e6-112">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="9b5e6-112">-ComponentVersion</span></span>
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

### <span data-ttu-id="9b5e6-113">-구성</span><span class="sxs-lookup"><span data-stu-id="9b5e6-113">-Config</span></span>
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

### <span data-ttu-id="9b5e6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b5e6-114">-DefaultProfile</span></span>
<span data-ttu-id="9b5e6-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9b5e6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b5e6-116">-확인</span><span class="sxs-lookup"><span data-stu-id="9b5e6-116">-Confirm</span></span>
<span data-ttu-id="9b5e6-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b5e6-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b5e6-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b5e6-118">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b5e6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b5e6-119">CommonParameters</span></span>
<span data-ttu-id="9b5e6-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b5e6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b5e6-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b5e6-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b5e6-122">입력</span><span class="sxs-lookup"><span data-stu-id="9b5e6-122">INPUTS</span></span>

### <span data-ttu-id="9b5e6-123">AzureHDInsightConfig의. m m.</span><span class="sxs-lookup"><span data-stu-id="9b5e6-123">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="9b5e6-124">출력</span><span class="sxs-lookup"><span data-stu-id="9b5e6-124">OUTPUTS</span></span>

### <span data-ttu-id="9b5e6-125">AzureHDInsightConfig의. m m.</span><span class="sxs-lookup"><span data-stu-id="9b5e6-125">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="9b5e6-126">상속자</span><span class="sxs-lookup"><span data-stu-id="9b5e6-126">NOTES</span></span>

## <span data-ttu-id="9b5e6-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b5e6-127">RELATED LINKS</span></span>
