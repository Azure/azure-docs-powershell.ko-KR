---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/set-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 573bb9534107a4df020e21269b5bdb2ec12db125
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984606"
---
# <span data-ttu-id="ae84a-101">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="ae84a-101">Set-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="ae84a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae84a-102">SYNOPSIS</span></span>
<span data-ttu-id="ae84a-103">이전에 실행한 스크립트 작업을 영구 스크립트 작업으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ae84a-103">Sets a previously executed script action to be a persisted script action.</span></span>

## <span data-ttu-id="ae84a-104">구문</span><span class="sxs-lookup"><span data-stu-id="ae84a-104">SYNTAX</span></span>

```
Set-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae84a-105">설명</span><span class="sxs-lookup"><span data-stu-id="ae84a-105">DESCRIPTION</span></span>
<span data-ttu-id="ae84a-106">**Set-AzHDInsightPersistedScriptAction** cmdlet은 이전에 실행한 스크립트 작업을 영구 스크립트 작업으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ae84a-106">The **Set-AzHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="ae84a-107">지정된 스크립트 작업은 이전에 성공했기만 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae84a-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="ae84a-108">스크립트 작업은 Azure HDInsight 클러스터가 확장될 때마다 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae84a-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="ae84a-109">예제</span><span class="sxs-lookup"><span data-stu-id="ae84a-109">EXAMPLES</span></span>

### <span data-ttu-id="ae84a-110">예제 1: 이전에 성공한 스크립트 작업을 유지하거나 클러스터 확장에서 실행</span><span class="sxs-lookup"><span data-stu-id="ae84a-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="ae84a-111">이 명령은 이전에 성공한 스크립트 작업을 영구 스크립트 작업으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ae84a-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="ae84a-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ae84a-112">PARAMETERS</span></span>

### <span data-ttu-id="ae84a-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ae84a-113">-ClusterName</span></span>
<span data-ttu-id="ae84a-114">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ae84a-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="ae84a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae84a-115">-DefaultProfile</span></span>
<span data-ttu-id="ae84a-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ae84a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae84a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae84a-117">-ResourceGroupName</span></span>
<span data-ttu-id="ae84a-118">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ae84a-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ae84a-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="ae84a-119">-ScriptExecutionId</span></span>
<span data-ttu-id="ae84a-120">지속성으로 승격할 스크립트 작업의 실행 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ae84a-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="ae84a-121">승격하려면 이 스크립트 작업이 성공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae84a-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="ae84a-122">Get-AzHDInsightScriptActionHistory를 사용하여 스크립트 작업 실행 ID를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae84a-122">You can find the script action execution ID using Get-AzHDInsightScriptActionHistory.</span></span>

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

### <span data-ttu-id="ae84a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae84a-123">CommonParameters</span></span>
<span data-ttu-id="ae84a-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ae84a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae84a-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae84a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae84a-126">입력</span><span class="sxs-lookup"><span data-stu-id="ae84a-126">INPUTS</span></span>

### <span data-ttu-id="ae84a-127">없음</span><span class="sxs-lookup"><span data-stu-id="ae84a-127">None</span></span>

## <span data-ttu-id="ae84a-128">출력</span><span class="sxs-lookup"><span data-stu-id="ae84a-128">OUTPUTS</span></span>

### <span data-ttu-id="ae84a-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="ae84a-129">System.Void</span></span>

## <span data-ttu-id="ae84a-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ae84a-130">NOTES</span></span>

## <span data-ttu-id="ae84a-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae84a-131">RELATED LINKS</span></span>

[<span data-ttu-id="ae84a-132">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="ae84a-132">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="ae84a-133">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="ae84a-133">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)


