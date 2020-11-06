---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/submit-azurermhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
ms.openlocfilehash: 884741f6543dee05ed8236385071ad345321413e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530295"
---
# <span data-ttu-id="0dc41-101">Submit-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="0dc41-101">Submit-AzureRmHDInsightScriptAction</span></span>

## <span data-ttu-id="0dc41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0dc41-102">SYNOPSIS</span></span>
<span data-ttu-id="0dc41-103">Azure HDInsight 클러스터에 새 스크립트 작업을 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dc41-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0dc41-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0dc41-104">SYNTAX</span></span>

```
Submit-AzureRmHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0dc41-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0dc41-105">DESCRIPTION</span></span>
<span data-ttu-id="0dc41-106">**AzureRmHDInsightScriptAction** Cmdlet은 Azure HDInsight 클러스터에 새 스크립트 작업을 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dc41-106">The **Submit-AzureRmHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="0dc41-107">스크립트 작업이 처음에 성공 하는 한, 클러스터의 크기를 조정할 때마다 스크립트 작업이 실행 되도록 *Persistonsuccess* 를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dc41-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="0dc41-108">예제의</span><span class="sxs-lookup"><span data-stu-id="0dc41-108">EXAMPLES</span></span>

### <span data-ttu-id="0dc41-109">예제 1: 실행 중인 HDInsight 클러스터에 새 스크립트 작업 제출</span><span class="sxs-lookup"><span data-stu-id="0dc41-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzureRmHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="0dc41-110">이 명령은 스크립트 동작을 실행 중인 HDInsight 클러스터에 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dc41-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="0dc41-111">변수</span><span class="sxs-lookup"><span data-stu-id="0dc41-111">PARAMETERS</span></span>

### <span data-ttu-id="0dc41-112">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="0dc41-112">-ApplicationName</span></span>
<span data-ttu-id="0dc41-113">스크립트 작업의 응용 프로그램 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dc41-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="0dc41-114">*ApplicationName* 이 지정 되 면 *Persistonsuccess* 가 False로 설정 되 고 노드는 edgenode만 포함 해야 하며 스크립트 동작 수는 1 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dc41-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

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

### <span data-ttu-id="0dc41-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0dc41-115">-ClusterName</span></span>
<span data-ttu-id="0dc41-116">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dc41-116">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="0dc41-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dc41-117">-DefaultProfile</span></span>
<span data-ttu-id="0dc41-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0dc41-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc41-119">-이름</span><span class="sxs-lookup"><span data-stu-id="0dc41-119">-Name</span></span>
<span data-ttu-id="0dc41-120">스크립트 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dc41-120">Specifies the name of the script action.</span></span>

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

### <span data-ttu-id="0dc41-121">-NodeTypes</span><span class="sxs-lookup"><span data-stu-id="0dc41-121">-NodeTypes</span></span>
<span data-ttu-id="0dc41-122">스크립트 작업을 실행할 노드 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dc41-122">Specifies the node types on which to run the script action.</span></span>

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

### <span data-ttu-id="0dc41-123">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="0dc41-123">-Parameters</span></span>
<span data-ttu-id="0dc41-124">스크립트 작업에 대 한 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dc41-124">Specifies the parameters for the script action.</span></span>

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

### <span data-ttu-id="0dc41-125">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="0dc41-125">-PersistOnSuccess</span></span>
<span data-ttu-id="0dc41-126">클러스터의 크기를 조정할 때마다 스크립트 동작이 실행 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0dc41-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="0dc41-127">스크립트 작업이 처음에 실패 하는 경우이 스위치 매개 변수는 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0dc41-127">This switch parameter is ignored if the script action initially fails.</span></span>

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

### <span data-ttu-id="0dc41-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dc41-128">-ResourceGroupName</span></span>
<span data-ttu-id="0dc41-129">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dc41-129">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0dc41-130">-Uri</span><span class="sxs-lookup"><span data-stu-id="0dc41-130">-Uri</span></span>
<span data-ttu-id="0dc41-131">스크립트 작업 (PowerShell 또는 Bash 스크립트)에 대 한 공용 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dc41-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

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

### <span data-ttu-id="0dc41-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dc41-132">CommonParameters</span></span>
<span data-ttu-id="0dc41-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dc41-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dc41-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dc41-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dc41-135">입력</span><span class="sxs-lookup"><span data-stu-id="0dc41-135">INPUTS</span></span>

### <span data-ttu-id="0dc41-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0dc41-136">System.String</span></span>

### <span data-ttu-id="0dc41-137">시스템 Uri</span><span class="sxs-lookup"><span data-stu-id="0dc41-137">System.Uri</span></span>

### <span data-ttu-id="0dc41-138">RuntimeScriptActionClusterNodeType [] (으)로의 명령</span><span class="sxs-lookup"><span data-stu-id="0dc41-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span></span>

## <span data-ttu-id="0dc41-139">출력</span><span class="sxs-lookup"><span data-stu-id="0dc41-139">OUTPUTS</span></span>

### <span data-ttu-id="0dc41-140">AzureHDInsightRuntimeScriptActionOperationResource를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dc41-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="0dc41-141">상속자</span><span class="sxs-lookup"><span data-stu-id="0dc41-141">NOTES</span></span>

## <span data-ttu-id="0dc41-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0dc41-142">RELATED LINKS</span></span>

[<span data-ttu-id="0dc41-143">추가-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="0dc41-143">Add-AzureRmHDInsightScriptAction</span></span>](./Add-AzureRmHDInsightScriptAction.md)


