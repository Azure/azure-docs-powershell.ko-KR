---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightgatewaycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
ms.openlocfilehash: 5f5c8c193a352738f64d595188247bf0564bea43
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056337"
---
# <span data-ttu-id="55e15-101">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="55e15-101">Set-AzHDInsightGatewayCredential</span></span>

## <span data-ttu-id="55e15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55e15-102">SYNOPSIS</span></span>
<span data-ttu-id="55e15-103">Azure HDInsight 클러스터의 게이트웨이 HTTP 자격 증명을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e15-103">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="55e15-104">구문과</span><span class="sxs-lookup"><span data-stu-id="55e15-104">SYNTAX</span></span>

### <span data-ttu-id="55e15-105">SetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="55e15-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightGatewayCredential -Name <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55e15-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55e15-106">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -InputObject <AzureHDInsightCluster> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55e15-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55e15-107">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55e15-108">설명은</span><span class="sxs-lookup"><span data-stu-id="55e15-108">DESCRIPTION</span></span>
<span data-ttu-id="55e15-109">**AzHDInsightGatewayCredential** Cmdlet은 Azure HDInsight 클러스터의 게이트웨이 자격 증명을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e15-109">The **Set-AzHDInsightGatewayCredential** cmdlet sets gateway credential of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="55e15-110">예제의</span><span class="sxs-lookup"><span data-stu-id="55e15-110">EXAMPLES</span></span>

### <span data-ttu-id="55e15-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="55e15-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Set-AzHDInsightGatewayCredential `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="55e15-112">이 명령은 name 매개 변수 집합으로-hadoop-001 이라는 클러스터의 게이트웨이 자격 증명을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e15-112">This command sets gateway credential of the cluster named your-hadoop-001 by name parameter set.</span></span>

### <span data-ttu-id="55e15-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="55e15-113">Example 2</span></span>
```powershell
PS C:\> Set-AzHDInsightGatewayCredential `
            -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.HDInsight/clusters/your-hadoop-001" `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="55e15-114">이 명령은-hadoop-001에서 ResourceId 매개 변수 집합으로 명명 된 클러스터의 게이트웨이 자격 증명을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e15-114">This command sets gateway credential of the cluster named your-hadoop-001 by ResourceId parameter set.</span></span>

### <span data-ttu-id="55e15-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="55e15-115">Example 3</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Get-AzHDInsightCluster -ClusterName $clusterName | Set-AzHDInsightGatewayCredential `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="55e15-116">이 명령은-hadoop-001에서 InputObject 매개 변수 집합으로 명명 된 클러스터의 게이트웨이 자격 증명을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e15-116">This command sets gateway credential of the cluster named your-hadoop-001 by InputObject parameter set.</span></span>

## <span data-ttu-id="55e15-117">변수</span><span class="sxs-lookup"><span data-stu-id="55e15-117">PARAMETERS</span></span>

### <span data-ttu-id="55e15-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55e15-118">-AsJob</span></span>
<span data-ttu-id="55e15-119">백그라운드에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e15-119">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="55e15-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55e15-120">-DefaultProfile</span></span>
<span data-ttu-id="55e15-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="55e15-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55e15-122">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="55e15-122">-HttpCredential</span></span>
<span data-ttu-id="55e15-123">클러스터의 사용자에 대 한 로그인을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e15-123">Gets or sets the login for the cluster's user.</span></span>

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

### <span data-ttu-id="55e15-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55e15-124">-InputObject</span></span>
<span data-ttu-id="55e15-125">입력 개체를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e15-125">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="55e15-126">-이름</span><span class="sxs-lookup"><span data-stu-id="55e15-126">-Name</span></span>
<span data-ttu-id="55e15-127">클러스터의 이름을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e15-127">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e15-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55e15-128">-ResourceGroupName</span></span>
<span data-ttu-id="55e15-129">리소스 그룹의 이름을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e15-129">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e15-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55e15-130">-ResourceId</span></span>
<span data-ttu-id="55e15-131">리소스 id를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e15-131">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="55e15-132">-확인</span><span class="sxs-lookup"><span data-stu-id="55e15-132">-Confirm</span></span>
<span data-ttu-id="55e15-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e15-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55e15-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55e15-134">-WhatIf</span></span>
<span data-ttu-id="55e15-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="55e15-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55e15-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="55e15-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55e15-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55e15-137">CommonParameters</span></span>
<span data-ttu-id="55e15-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e15-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55e15-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="55e15-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55e15-140">입력</span><span class="sxs-lookup"><span data-stu-id="55e15-140">INPUTS</span></span>

### <span data-ttu-id="55e15-141">않아야</span><span class="sxs-lookup"><span data-stu-id="55e15-141">None</span></span>

## <span data-ttu-id="55e15-142">출력</span><span class="sxs-lookup"><span data-stu-id="55e15-142">OUTPUTS</span></span>

### <span data-ttu-id="55e15-143">AzureHDInsightGatewaySettings를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e15-143">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightGatewaySettings</span></span>

## <span data-ttu-id="55e15-144">상속자</span><span class="sxs-lookup"><span data-stu-id="55e15-144">NOTES</span></span>

## <span data-ttu-id="55e15-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="55e15-145">RELATED LINKS</span></span>
