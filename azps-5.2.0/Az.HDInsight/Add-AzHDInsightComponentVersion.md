---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 774848C9-47A1-4C43-B6FA-B3C0C3C76470
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightcomponentversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightComponentVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightComponentVersion.md
ms.openlocfilehash: 6755bb08174a34fe91c5e11373719607f87ad711
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356931"
---
# <span data-ttu-id="c0249-101">Add-AzHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="c0249-101">Add-AzHDInsightComponentVersion</span></span>

## <span data-ttu-id="c0249-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0249-102">SYNOPSIS</span></span>
<span data-ttu-id="c0249-103">클러스터에서 실행되는 서비스에 대한 버전을 클러스터 구성 개체에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c0249-103">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

## <span data-ttu-id="c0249-104">구문</span><span class="sxs-lookup"><span data-stu-id="c0249-104">SYNTAX</span></span>

```
Add-AzHDInsightComponentVersion [-Config] <AzureHDInsightConfig> [-ComponentName] <String>
 [-ComponentVersion] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0249-105">설명</span><span class="sxs-lookup"><span data-stu-id="c0249-105">DESCRIPTION</span></span>
<span data-ttu-id="c0249-106">Add-AzHDInsightComponentVersion cmdlet은 클러스터에서 실행되는 서비스에 대한 버전을 New-AzHDInsightClusterConfig cmdlet에서 만든 Azure HDInsight 구성 개체에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c0249-106">The Add-AzHDInsightComponentVersion cmdlet adds a version for a service running in a cluster to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="c0249-107">예제</span><span class="sxs-lookup"><span data-stu-id="c0249-107">EXAMPLES</span></span>

### <span data-ttu-id="c0249-108">예제 1: 클러스터 구성 개체에 Spark에 대한 버전을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c0249-108">Example 1: Add a version for Spark to the cluster configuration object.</span></span>
```
PS C:\> # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer `
                -SshCredential $sshCredentials `
                -Version "3.5"
```

<span data-ttu-id="c0249-109">이 명령은 'your-spark-001'이라는 HDInsight 클러스터에 Spark 버전을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c0249-109">This command adds the version of Spark to the HDInsight cluster named 'your-spark-001'.</span></span>

## <span data-ttu-id="c0249-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0249-110">PARAMETERS</span></span>

### <span data-ttu-id="c0249-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="c0249-111">-ComponentName</span></span>
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

### <span data-ttu-id="c0249-112">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="c0249-112">-ComponentVersion</span></span>
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

### <span data-ttu-id="c0249-113">-Config</span><span class="sxs-lookup"><span data-stu-id="c0249-113">-Config</span></span>
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

### <span data-ttu-id="c0249-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0249-114">-DefaultProfile</span></span>
<span data-ttu-id="c0249-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c0249-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0249-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0249-116">-Confirm</span></span>
<span data-ttu-id="c0249-117">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0249-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0249-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0249-118">-WhatIf</span></span>
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

### <span data-ttu-id="c0249-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0249-119">CommonParameters</span></span>
<span data-ttu-id="c0249-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c0249-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0249-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c0249-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0249-122">입력</span><span class="sxs-lookup"><span data-stu-id="c0249-122">INPUTS</span></span>

### <span data-ttu-id="c0249-123">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="c0249-123">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="c0249-124">출력</span><span class="sxs-lookup"><span data-stu-id="c0249-124">OUTPUTS</span></span>

### <span data-ttu-id="c0249-125">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="c0249-125">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="c0249-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c0249-126">NOTES</span></span>

## <span data-ttu-id="c0249-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0249-127">RELATED LINKS</span></span>
