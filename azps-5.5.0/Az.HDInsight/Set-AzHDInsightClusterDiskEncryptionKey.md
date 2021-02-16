---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5141D84C-3C58-42B9-890F-C3C9049BC1C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclusterdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
ms.openlocfilehash: b3421fa4382912d11a3e3a28b81acffb7be123a2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200193"
---
# <span data-ttu-id="f6031-101">Set-AzHDInsightClusterDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="f6031-101">Set-AzHDInsightClusterDiskEncryptionKey</span></span>

## <span data-ttu-id="f6031-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6031-102">SYNOPSIS</span></span>
<span data-ttu-id="f6031-103">지정된 HDInsight 클러스터의 디스크 암호화 키를 회전합니다.</span><span class="sxs-lookup"><span data-stu-id="f6031-103">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

## <span data-ttu-id="f6031-104">구문</span><span class="sxs-lookup"><span data-stu-id="f6031-104">SYNTAX</span></span>

### <span data-ttu-id="f6031-105">SetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f6031-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceGroupName] <String> [-Name] <String>
 -EncryptionKeyName <String> -EncryptionKeyVersion <String> -EncryptionVaultUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6031-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6031-106">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceId] <String> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6031-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6031-107">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-InputObject] <AzureHDInsightCluster> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6031-108">설명</span><span class="sxs-lookup"><span data-stu-id="f6031-108">DESCRIPTION</span></span>
<span data-ttu-id="f6031-109">지정된 HDInsight 클러스터의 디스크 암호화 키를 회전합니다.</span><span class="sxs-lookup"><span data-stu-id="f6031-109">Rotate the disk encryption key of the specified HDInsight cluster.</span></span> <span data-ttu-id="f6031-110">이 작업의 경우 클러스터는 현재 키와 의도된 새 키 모두에 액세스할 수 있어야 합니다. 그렇지 않으면 회전 키 작업이 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="f6031-110">For this operation, the cluster must have access to both the current key and the intended new key, otherwise the rotate key operation will fail.</span></span>

## <span data-ttu-id="f6031-111">예제</span><span class="sxs-lookup"><span data-stu-id="f6031-111">EXAMPLES</span></span>

### <span data-ttu-id="f6031-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="f6031-112">Example 1</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterResourceGroupName = "Group"
        $clusterName = "your-cmk-cluster"

Set-AzHDInsightClusterDiskEncryptionKey `
        -ResourceGroupName $clusterResourceGroupName `
        -ClusterName $clusterName `
        -EncryptionKeyName new-key `
        -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
        -EncryptionKeyVersion 00000000000000000000000000000000
```

### <span data-ttu-id="f6031-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="f6031-113">Example 2</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterName = "your-cmk-cluster"

$cluster= Get-AzHDInsightCluster -ClusterName $clusterName 
$cluster |  Set-AzHDInsightClusterDiskEncryptionKey `
    -EncryptionKeyName new-key `
    -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
    -EncryptionKeyVersion 00000000000000000000000000000000
```

## <span data-ttu-id="f6031-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6031-114">PARAMETERS</span></span>

### <span data-ttu-id="f6031-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6031-115">-DefaultProfile</span></span>
<span data-ttu-id="f6031-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f6031-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6031-117">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="f6031-117">-EncryptionKeyName</span></span>
<span data-ttu-id="f6031-118">암호화 키 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6031-118">Gets or sets the encryption key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6031-119">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="f6031-119">-EncryptionKeyVersion</span></span>
<span data-ttu-id="f6031-120">암호화 키 버전을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6031-120">Gets or sets the encryption key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6031-121">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="f6031-121">-EncryptionVaultUri</span></span>
<span data-ttu-id="f6031-122">암호화 자격 증명 모음 URI를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6031-122">Gets or sets the encryption vault uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6031-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6031-123">-InputObject</span></span>
<span data-ttu-id="f6031-124">입력 개체를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6031-124">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6031-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f6031-125">-Name</span></span>
<span data-ttu-id="f6031-126">클러스터의 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6031-126">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6031-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6031-127">-ResourceGroupName</span></span>
<span data-ttu-id="f6031-128">리소스 그룹의 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6031-128">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6031-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6031-129">-ResourceId</span></span>
<span data-ttu-id="f6031-130">리소스 ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6031-130">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6031-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6031-131">-Confirm</span></span>
<span data-ttu-id="f6031-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6031-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6031-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6031-133">-WhatIf</span></span>
<span data-ttu-id="f6031-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f6031-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6031-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f6031-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6031-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6031-136">CommonParameters</span></span>
<span data-ttu-id="f6031-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f6031-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6031-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f6031-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6031-139">입력</span><span class="sxs-lookup"><span data-stu-id="f6031-139">INPUTS</span></span>

### <span data-ttu-id="f6031-140">없음</span><span class="sxs-lookup"><span data-stu-id="f6031-140">None</span></span>

## <span data-ttu-id="f6031-141">출력</span><span class="sxs-lookup"><span data-stu-id="f6031-141">OUTPUTS</span></span>

### <span data-ttu-id="f6031-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span><span class="sxs-lookup"><span data-stu-id="f6031-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="f6031-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f6031-143">NOTES</span></span>

## <span data-ttu-id="f6031-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f6031-144">RELATED LINKS</span></span>

[<span data-ttu-id="f6031-145">고객 관리 키 디스크 암호화</span><span class="sxs-lookup"><span data-stu-id="f6031-145">Customer-managed key disk encryption</span></span>](https://docs.microsoft.com/en-us/azure/hdinsight/disk-encryption)
