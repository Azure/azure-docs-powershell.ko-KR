---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/remove-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: a7c5c9c2008839d4e90dd5f393fbe4acea0f78a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965888"
---
# <span data-ttu-id="8e934-101">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="8e934-101">Remove-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="8e934-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e934-102">SYNOPSIS</span></span>
<span data-ttu-id="8e934-103">HDInsight 클러스터에서 영구 스크립트 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8e934-103">Removes an persisted script action from an HDInsight cluster.</span></span>

## <span data-ttu-id="8e934-104">구문</span><span class="sxs-lookup"><span data-stu-id="8e934-104">SYNTAX</span></span>

```
Remove-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e934-105">설명</span><span class="sxs-lookup"><span data-stu-id="8e934-105">DESCRIPTION</span></span>
<span data-ttu-id="8e934-106">**Remove-AzHDInsightPersistedScriptAction** cmdlet은 지정된 Azure HDInsight 클러스터의 영구 스크립트 작업 목록에서 영구 스크립트 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8e934-106">The **Remove-AzHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="8e934-107">클러스터가 확장되면 제거된 스크립트가 더 이상 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e934-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="8e934-108">예제</span><span class="sxs-lookup"><span data-stu-id="8e934-108">EXAMPLES</span></span>

### <span data-ttu-id="8e934-109">예제 1: 클러스터의 영구 스크립트 작업 목록에서 스크립트 작업 제거</span><span class="sxs-lookup"><span data-stu-id="8e934-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="8e934-110">이 명령은 지정된 클러스터의 영구 스크립트 작업 목록에서 Scriptaction이라는 스크립트 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8e934-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="8e934-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8e934-111">PARAMETERS</span></span>

### <span data-ttu-id="8e934-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8e934-112">-ClusterName</span></span>
<span data-ttu-id="8e934-113">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8e934-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="8e934-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e934-114">-DefaultProfile</span></span>
<span data-ttu-id="8e934-115">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8e934-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e934-116">-Name</span><span class="sxs-lookup"><span data-stu-id="8e934-116">-Name</span></span>
<span data-ttu-id="8e934-117">제거할 영구 스크립트 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8e934-117">Specifies the name of the persisted script action to be removed.</span></span>

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

### <span data-ttu-id="8e934-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e934-118">-ResourceGroupName</span></span>
<span data-ttu-id="8e934-119">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8e934-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8e934-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e934-120">CommonParameters</span></span>
<span data-ttu-id="8e934-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8e934-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e934-122">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e934-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e934-123">입력</span><span class="sxs-lookup"><span data-stu-id="8e934-123">INPUTS</span></span>

### <span data-ttu-id="8e934-124">없음</span><span class="sxs-lookup"><span data-stu-id="8e934-124">None</span></span>

## <span data-ttu-id="8e934-125">출력</span><span class="sxs-lookup"><span data-stu-id="8e934-125">OUTPUTS</span></span>

### <span data-ttu-id="8e934-126">System.Void</span><span class="sxs-lookup"><span data-stu-id="8e934-126">System.Void</span></span>

## <span data-ttu-id="8e934-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8e934-127">NOTES</span></span>

## <span data-ttu-id="8e934-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e934-128">RELATED LINKS</span></span>

[<span data-ttu-id="8e934-129">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="8e934-129">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="8e934-130">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="8e934-130">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


