---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/restart-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
ms.openlocfilehash: 4e0b5fda29696fb45515c3b478b9dc29ff67263e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489592"
---
# <span data-ttu-id="f623d-101">Restart-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="f623d-101">Restart-AzHDInsightHost</span></span>

## <span data-ttu-id="f623d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f623d-102">SYNOPSIS</span></span>
<span data-ttu-id="f623d-103">HDInsight 클러스터의 특정 호스트를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="f623d-103">Restarts the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="f623d-104">구문</span><span class="sxs-lookup"><span data-stu-id="f623d-104">SYNTAX</span></span>

### <span data-ttu-id="f623d-105">SetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f623d-105">SetByNameParameterSet (Default)</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String> [-Name] <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f623d-106">SetByAzureHDInsightHostInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="f623d-106">SetByAzureHDInsightHostInfoParameterSet</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AzureHDInsightHostInfo] <AzureHDInsightHostInfo[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f623d-107">설명</span><span class="sxs-lookup"><span data-stu-id="f623d-107">DESCRIPTION</span></span>
<span data-ttu-id="f623d-108">이 **Restart-AzHDInsightHost** cmdlet은 HDInsight 클러스터의 특정 호스트를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="f623d-108">This **Restart-AzHDInsightHost** cmdlet restart the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="f623d-109">예제</span><span class="sxs-lookup"><span data-stu-id="f623d-109">EXAMPLES</span></span>

### <span data-ttu-id="f623d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f623d-110">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Restart-AzHDInsightHost -ClusterName $clusterName -Name wn0, wn1
```

<span data-ttu-id="f623d-111">이 명령은 클러스터의 두 호스트인 worknode1, worknode2를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="f623d-111">This command restarts two hosts of the cluster: worknode1, worknode2.</span></span>

### <span data-ttu-id="f623d-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="f623d-112">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $worknode1= Get-AzHDInsightHost -ClusterName $clusterName | Where-Object {$_.Name -like "wn1*"}
PS C:\> $worknode1 | Restart-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="f623d-113">이 명령은 'Get-AzHDInsightHost' cmdlet과 협력하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f623d-113">This command shows how to cooperate with the cmdlet 'Get-AzHDInsightHost'.</span></span>

## <span data-ttu-id="f623d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f623d-114">PARAMETERS</span></span>

### <span data-ttu-id="f623d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f623d-115">-AsJob</span></span>
<span data-ttu-id="f623d-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f623d-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f623d-117">-AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="f623d-117">-AzureHDInsightHostInfo</span></span>
<span data-ttu-id="f623d-118">호스트의 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f623d-118">Gets or sets the name of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]
Parameter Sets: SetByAzureHDInsightHostInfoParameterSet
Aliases: Host

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f623d-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f623d-119">-ClusterName</span></span>
<span data-ttu-id="f623d-120">클러스터의 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f623d-120">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="f623d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f623d-121">-DefaultProfile</span></span>
<span data-ttu-id="f623d-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f623d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f623d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f623d-123">-Name</span></span>
<span data-ttu-id="f623d-124">호스트의 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f623d-124">Gets or sets the name of the host.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByNameParameterSet
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f623d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f623d-125">-PassThru</span></span>
<span data-ttu-id="f623d-126">{{ PassThru 설명 채우기 }}</span><span class="sxs-lookup"><span data-stu-id="f623d-126">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f623d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f623d-127">-ResourceGroupName</span></span>
<span data-ttu-id="f623d-128">리소스 그룹의 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f623d-128">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f623d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f623d-129">-Confirm</span></span>
<span data-ttu-id="f623d-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f623d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f623d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f623d-131">-WhatIf</span></span>
<span data-ttu-id="f623d-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f623d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f623d-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f623d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f623d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f623d-134">CommonParameters</span></span>
<span data-ttu-id="f623d-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f623d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f623d-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f623d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f623d-137">입력</span><span class="sxs-lookup"><span data-stu-id="f623d-137">INPUTS</span></span>

### <span data-ttu-id="f623d-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f623d-138">System.String[]</span></span>

### <span data-ttu-id="f623d-139">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]</span><span class="sxs-lookup"><span data-stu-id="f623d-139">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]</span></span>

## <span data-ttu-id="f623d-140">출력</span><span class="sxs-lookup"><span data-stu-id="f623d-140">OUTPUTS</span></span>

### <span data-ttu-id="f623d-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f623d-141">System.Boolean</span></span>

## <span data-ttu-id="f623d-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f623d-142">NOTES</span></span>

## <span data-ttu-id="f623d-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f623d-143">RELATED LINKS</span></span>
