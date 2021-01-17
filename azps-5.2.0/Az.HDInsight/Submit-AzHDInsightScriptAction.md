---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/submit-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
ms.openlocfilehash: dfae83e6bd540a83475f02ed95382bebff2ec7a5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328257"
---
# <span data-ttu-id="bc007-101">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="bc007-101">Submit-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="bc007-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc007-102">SYNOPSIS</span></span>
<span data-ttu-id="bc007-103">Azure HDInsight 클러스터에 새 스크립트 작업을 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="bc007-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="bc007-104">구문</span><span class="sxs-lookup"><span data-stu-id="bc007-104">SYNTAX</span></span>

```
Submit-AzHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc007-105">설명</span><span class="sxs-lookup"><span data-stu-id="bc007-105">DESCRIPTION</span></span>
<span data-ttu-id="bc007-106">**Submit-AzHDInsightScriptAction** cmdlet은 Azure HDInsight 클러스터에 새 스크립트 작업을 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="bc007-106">The **Submit-AzHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="bc007-107">처음에 스크립트 작업이 성공하는 한 클러스터가 확장될 때마다 *PersistOnSuccess를* 사용하여 스크립트 작업을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="bc007-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="bc007-108">예제</span><span class="sxs-lookup"><span data-stu-id="bc007-108">EXAMPLES</span></span>

### <span data-ttu-id="bc007-109">예제 1: 실행 중인 HDInsight 클러스터에 새 스크립트 작업 제출</span><span class="sxs-lookup"><span data-stu-id="bc007-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="bc007-110">이 명령은 실행 중인 HDInsight 클러스터에 스크립트 작업을 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="bc007-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="bc007-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc007-111">PARAMETERS</span></span>

### <span data-ttu-id="bc007-112">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="bc007-112">-ApplicationName</span></span>
<span data-ttu-id="bc007-113">스크립트 동작에 대한 애플리케이션 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc007-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="bc007-114">*ApplicationName을* 지정하면 *PersistOnSuccess를* False로 설정해야 합니다. 노드는 에지 노드만 포함해야 합니다. 스크립트 작업 수는 1과 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc007-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc007-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="bc007-115">-ClusterName</span></span>
<span data-ttu-id="bc007-116">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc007-116">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc007-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc007-117">-DefaultProfile</span></span>
<span data-ttu-id="bc007-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bc007-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc007-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bc007-119">-Name</span></span>
<span data-ttu-id="bc007-120">스크립트 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc007-120">Specifies the name of the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc007-121">-NodeTypes</span><span class="sxs-lookup"><span data-stu-id="bc007-121">-NodeTypes</span></span>
<span data-ttu-id="bc007-122">스크립트 작업을 실행할 노드 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc007-122">Specifies the node types on which to run the script action.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc007-123">-Parameters</span><span class="sxs-lookup"><span data-stu-id="bc007-123">-Parameters</span></span>
<span data-ttu-id="bc007-124">스크립트 동작에 대한 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc007-124">Specifies the parameters for the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc007-125">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="bc007-125">-PersistOnSuccess</span></span>
<span data-ttu-id="bc007-126">클러스터가 확장할 때마다 스크립트 작업이 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc007-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="bc007-127">스크립트 작업이 처음에 실패하면 이 스위치 매개 변수는 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc007-127">This switch parameter is ignored if the script action initially fails.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc007-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc007-128">-ResourceGroupName</span></span>
<span data-ttu-id="bc007-129">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc007-129">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="bc007-130">-Uri</span><span class="sxs-lookup"><span data-stu-id="bc007-130">-Uri</span></span>
<span data-ttu-id="bc007-131">스크립트 작업(PowerShell 또는 Bash 스크립트)에 대한 공용 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc007-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc007-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc007-132">CommonParameters</span></span>
<span data-ttu-id="bc007-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bc007-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc007-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bc007-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc007-135">입력</span><span class="sxs-lookup"><span data-stu-id="bc007-135">INPUTS</span></span>

### <span data-ttu-id="bc007-136">System.String</span><span class="sxs-lookup"><span data-stu-id="bc007-136">System.String</span></span>

### <span data-ttu-id="bc007-137">System.Uri</span><span class="sxs-lookup"><span data-stu-id="bc007-137">System.Uri</span></span>

### <span data-ttu-id="bc007-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span><span class="sxs-lookup"><span data-stu-id="bc007-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span></span>

## <span data-ttu-id="bc007-139">출력</span><span class="sxs-lookup"><span data-stu-id="bc007-139">OUTPUTS</span></span>

### <span data-ttu-id="bc007-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span><span class="sxs-lookup"><span data-stu-id="bc007-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="bc007-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bc007-141">NOTES</span></span>

## <span data-ttu-id="bc007-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bc007-142">RELATED LINKS</span></span>

[<span data-ttu-id="bc007-143">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="bc007-143">Add-AzHDInsightScriptAction</span></span>](./Add-AzHDInsightScriptAction.md)


