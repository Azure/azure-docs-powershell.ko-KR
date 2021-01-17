---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: bff21d969a88282f3ba3c1d79d1f717c3c169265
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322853"
---
# <span data-ttu-id="2e439-101">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="2e439-101">Set-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="2e439-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e439-102">SYNOPSIS</span></span>
<span data-ttu-id="2e439-103">이전에 실행한 스크립트 작업을 지속형 스크립트 동작으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e439-103">Sets a previously executed script action to be a persisted script action.</span></span>

## <span data-ttu-id="2e439-104">구문</span><span class="sxs-lookup"><span data-stu-id="2e439-104">SYNTAX</span></span>

```
Set-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e439-105">설명</span><span class="sxs-lookup"><span data-stu-id="2e439-105">DESCRIPTION</span></span>
<span data-ttu-id="2e439-106">**Set-AzHDInsightPersistedScriptAction** cmdlet은 이전에 실행한 스크립트 작업을 지속형 스크립트 동작으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e439-106">The **Set-AzHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="2e439-107">지정된 스크립트 동작은 이전에 성공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e439-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="2e439-108">스크립트 작업은 Azure HDInsight 클러스터가 확장될 때마다 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e439-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="2e439-109">예제</span><span class="sxs-lookup"><span data-stu-id="2e439-109">EXAMPLES</span></span>

### <span data-ttu-id="2e439-110">예제 1: 이전에 성공한 스크립트 작업을 유지하거나 클러스터 확장 시 실행</span><span class="sxs-lookup"><span data-stu-id="2e439-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="2e439-111">이 명령은 이전에 성공한 스크립트 작업을 지속된 스크립트 동작으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e439-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="2e439-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e439-112">PARAMETERS</span></span>

### <span data-ttu-id="2e439-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2e439-113">-ClusterName</span></span>
<span data-ttu-id="2e439-114">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e439-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="2e439-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e439-115">-DefaultProfile</span></span>
<span data-ttu-id="2e439-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2e439-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e439-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e439-117">-ResourceGroupName</span></span>
<span data-ttu-id="2e439-118">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e439-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2e439-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="2e439-119">-ScriptExecutionId</span></span>
<span data-ttu-id="2e439-120">지속형으로 승격할 스크립트 작업의 실행 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e439-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="2e439-121">승격하려면 이 스크립트 작업이 성공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e439-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="2e439-122">Get-AzHDInsightScriptActionHistory를 사용하여 스크립트 작업 실행 ID를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e439-122">You can find the script action execution ID using Get-AzHDInsightScriptActionHistory.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e439-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e439-123">CommonParameters</span></span>
<span data-ttu-id="2e439-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2e439-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e439-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2e439-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e439-126">입력</span><span class="sxs-lookup"><span data-stu-id="2e439-126">INPUTS</span></span>

### <span data-ttu-id="2e439-127">없음</span><span class="sxs-lookup"><span data-stu-id="2e439-127">None</span></span>

## <span data-ttu-id="2e439-128">출력</span><span class="sxs-lookup"><span data-stu-id="2e439-128">OUTPUTS</span></span>

### <span data-ttu-id="2e439-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="2e439-129">System.Void</span></span>

## <span data-ttu-id="2e439-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2e439-130">NOTES</span></span>

## <span data-ttu-id="2e439-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2e439-131">RELATED LINKS</span></span>

[<span data-ttu-id="2e439-132">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="2e439-132">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="2e439-133">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="2e439-133">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)


