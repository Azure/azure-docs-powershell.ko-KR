---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightgatewaycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
ms.openlocfilehash: f3997247c9a32fa9066e17dff3a09f2bd65a80d5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207309"
---
# <span data-ttu-id="a6244-101">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="a6244-101">Set-AzHDInsightGatewayCredential</span></span>

## <span data-ttu-id="a6244-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6244-102">SYNOPSIS</span></span>
<span data-ttu-id="a6244-103">Azure HDInsight 클러스터의 게이트웨이 HTTP 자격 증명을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6244-103">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="a6244-104">구문</span><span class="sxs-lookup"><span data-stu-id="a6244-104">SYNTAX</span></span>

### <span data-ttu-id="a6244-105">SetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a6244-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightGatewayCredential [-Name] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a6244-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6244-106">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -InputObject <AzureHDInsightCluster> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a6244-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6244-107">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6244-108">설명</span><span class="sxs-lookup"><span data-stu-id="a6244-108">DESCRIPTION</span></span>
<span data-ttu-id="a6244-109">**Set-AzHDInsightGatewayCredential** cmdlet은 Azure HDInsight 클러스터의 게이트웨이 자격 증명을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6244-109">The **Set-AzHDInsightGatewayCredential** cmdlet sets gateway credential of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="a6244-110">예제</span><span class="sxs-lookup"><span data-stu-id="a6244-110">EXAMPLES</span></span>

### <span data-ttu-id="a6244-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a6244-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Set-AzHDInsightGatewayCredential `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="a6244-112">이 명령은 이름 매개 변수 집합으로 your-hadoop-001이라는 클러스터의 게이트웨이 자격 증명을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6244-112">This command sets gateway credential of the cluster named your-hadoop-001 by name parameter set.</span></span>

### <span data-ttu-id="a6244-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="a6244-113">Example 2</span></span>
```powershell
PS C:\> Set-AzHDInsightGatewayCredential `
            -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.HDInsight/clusters/your-hadoop-001" `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="a6244-114">이 명령은 ResourceId 매개 변수 집합에 의해 hadoop-001이라는 클러스터의 게이트웨이 자격 증명을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6244-114">This command sets gateway credential of the cluster named your-hadoop-001 by ResourceId parameter set.</span></span>

### <span data-ttu-id="a6244-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="a6244-115">Example 3</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Get-AzHDInsightCluster -ClusterName $clusterName | Set-AzHDInsightGatewayCredential `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="a6244-116">이 명령은 InputObject 매개 변수 집합에 의해 your-hadoop-001이라는 클러스터의 게이트웨이 자격 증명을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6244-116">This command sets gateway credential of the cluster named your-hadoop-001 by InputObject parameter set.</span></span>

## <span data-ttu-id="a6244-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6244-117">PARAMETERS</span></span>

### <span data-ttu-id="a6244-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6244-118">-AsJob</span></span>
<span data-ttu-id="a6244-119">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a6244-119">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="a6244-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6244-120">-DefaultProfile</span></span>
<span data-ttu-id="a6244-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a6244-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6244-122">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="a6244-122">-HttpCredential</span></span>
<span data-ttu-id="a6244-123">클러스터의 사용자에 대한 로그인을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6244-123">Gets or sets the login for the cluster's user.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6244-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6244-124">-InputObject</span></span>
<span data-ttu-id="a6244-125">입력 개체를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6244-125">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6244-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a6244-126">-Name</span></span>
<span data-ttu-id="a6244-127">클러스터의 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6244-127">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6244-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6244-128">-ResourceGroupName</span></span>
<span data-ttu-id="a6244-129">리소스 그룹의 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6244-129">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6244-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6244-130">-ResourceId</span></span>
<span data-ttu-id="a6244-131">리소스 ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6244-131">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6244-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6244-132">-Confirm</span></span>
<span data-ttu-id="a6244-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6244-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6244-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6244-134">-WhatIf</span></span>
<span data-ttu-id="a6244-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a6244-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6244-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6244-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6244-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6244-137">CommonParameters</span></span>
<span data-ttu-id="a6244-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a6244-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6244-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a6244-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6244-140">입력</span><span class="sxs-lookup"><span data-stu-id="a6244-140">INPUTS</span></span>

### <span data-ttu-id="a6244-141">없음</span><span class="sxs-lookup"><span data-stu-id="a6244-141">None</span></span>

## <span data-ttu-id="a6244-142">출력</span><span class="sxs-lookup"><span data-stu-id="a6244-142">OUTPUTS</span></span>

### <span data-ttu-id="a6244-143">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightGatewaySettings</span><span class="sxs-lookup"><span data-stu-id="a6244-143">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightGatewaySettings</span></span>

## <span data-ttu-id="a6244-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a6244-144">NOTES</span></span>

## <span data-ttu-id="a6244-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a6244-145">RELATED LINKS</span></span>
