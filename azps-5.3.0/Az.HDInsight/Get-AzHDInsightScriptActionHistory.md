---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightscriptactionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
ms.openlocfilehash: 0424578473aedb60071e3389e7aaff2b84848f8c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489604"
---
# <span data-ttu-id="68db8-101">Get-AzHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="68db8-101">Get-AzHDInsightScriptActionHistory</span></span>

## <span data-ttu-id="68db8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68db8-102">SYNOPSIS</span></span>
<span data-ttu-id="68db8-103">클러스터에 대한 스크립트 작업 기록을 얻거나 역순으로 나열하거나 이전에 실행한 스크립트 동작의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="68db8-103">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="68db8-104">구문</span><span class="sxs-lookup"><span data-stu-id="68db8-104">SYNTAX</span></span>

```
Get-AzHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68db8-105">설명</span><span class="sxs-lookup"><span data-stu-id="68db8-105">DESCRIPTION</span></span>
<span data-ttu-id="68db8-106">**Get-AzHDInsightScriptActionHistory** cmdlet은 Azure HDInsight 클러스터에 대한 스크립트 작업 기록을 사용하여 역순으로 나열하거나 이전에 실행한 스크립트 동작의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="68db8-106">The **Get-AzHDInsightScriptActionHistory** cmdlet gets the script action history for an Azure HDInsight cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="68db8-107">예제</span><span class="sxs-lookup"><span data-stu-id="68db8-107">EXAMPLES</span></span>

### <span data-ttu-id="68db8-108">예제 1: 클러스터에 대한 스크립트 작업 실행 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="68db8-108">Example 1: Get the history of script actions executions for a cluster</span></span>
```
PS C:\>Get-AzHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

<span data-ttu-id="68db8-109">이 명령은 hadoop-001 클러스터에 대한 스크립트 작업의 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="68db8-109">This command gets the history of script actions for the cluster your-hadoop-001.</span></span>

## <span data-ttu-id="68db8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68db8-110">PARAMETERS</span></span>

### <span data-ttu-id="68db8-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="68db8-111">-ClusterName</span></span>
<span data-ttu-id="68db8-112">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="68db8-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="68db8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68db8-113">-DefaultProfile</span></span>
<span data-ttu-id="68db8-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="68db8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68db8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68db8-115">-ResourceGroupName</span></span>
<span data-ttu-id="68db8-116">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="68db8-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="68db8-117">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="68db8-117">-ScriptExecutionId</span></span>
<span data-ttu-id="68db8-118">실행된 스크립트 작업의 실행 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="68db8-118">Specifies the execution ID of the executed script action.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68db8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68db8-119">CommonParameters</span></span>
<span data-ttu-id="68db8-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="68db8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68db8-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="68db8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68db8-122">입력</span><span class="sxs-lookup"><span data-stu-id="68db8-122">INPUTS</span></span>

### <span data-ttu-id="68db8-123">없음</span><span class="sxs-lookup"><span data-stu-id="68db8-123">None</span></span>

## <span data-ttu-id="68db8-124">출력</span><span class="sxs-lookup"><span data-stu-id="68db8-124">OUTPUTS</span></span>

### <span data-ttu-id="68db8-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail</span><span class="sxs-lookup"><span data-stu-id="68db8-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail</span></span>

## <span data-ttu-id="68db8-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="68db8-126">NOTES</span></span>

## <span data-ttu-id="68db8-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68db8-127">RELATED LINKS</span></span>
