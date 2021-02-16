---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 344c6fccd0f6c7db26110a94e2cacc53625df3d9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200201"
---
# <span data-ttu-id="7b142-101">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="7b142-101">Remove-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="7b142-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b142-102">SYNOPSIS</span></span>
<span data-ttu-id="7b142-103">HDInsight 클러스터에서 지속된 스크립트 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7b142-103">Removes an persisted script action from an HDInsight cluster.</span></span>

## <span data-ttu-id="7b142-104">구문</span><span class="sxs-lookup"><span data-stu-id="7b142-104">SYNTAX</span></span>

```
Remove-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b142-105">설명</span><span class="sxs-lookup"><span data-stu-id="7b142-105">DESCRIPTION</span></span>
<span data-ttu-id="7b142-106">**Remove-AzHDInsightPersistedScriptAction** cmdlet은 지정된 Azure HDInsight 클러스터의 지속형 스크립트 작업 목록에서 지속형 스크립트 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7b142-106">The **Remove-AzHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="7b142-107">클러스터가 확장될 때 제거된 스크립트가 더 이상 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7b142-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="7b142-108">예제</span><span class="sxs-lookup"><span data-stu-id="7b142-108">EXAMPLES</span></span>

### <span data-ttu-id="7b142-109">예제 1: 클러스터의 지속된 스크립트 작업 목록에서 스크립트 작업 제거</span><span class="sxs-lookup"><span data-stu-id="7b142-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="7b142-110">이 명령은 지정된 클러스터의 지속된 스크립트 작업 목록에서 Scriptaction이라는 스크립트 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7b142-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="7b142-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b142-111">PARAMETERS</span></span>

### <span data-ttu-id="7b142-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7b142-112">-ClusterName</span></span>
<span data-ttu-id="7b142-113">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b142-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="7b142-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b142-114">-DefaultProfile</span></span>
<span data-ttu-id="7b142-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7b142-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b142-116">-Name</span><span class="sxs-lookup"><span data-stu-id="7b142-116">-Name</span></span>
<span data-ttu-id="7b142-117">제거할 지속된 스크립트 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b142-117">Specifies the name of the persisted script action to be removed.</span></span>

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

### <span data-ttu-id="7b142-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b142-118">-ResourceGroupName</span></span>
<span data-ttu-id="7b142-119">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b142-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7b142-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b142-120">CommonParameters</span></span>
<span data-ttu-id="7b142-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7b142-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b142-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7b142-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b142-123">입력</span><span class="sxs-lookup"><span data-stu-id="7b142-123">INPUTS</span></span>

### <span data-ttu-id="7b142-124">없음</span><span class="sxs-lookup"><span data-stu-id="7b142-124">None</span></span>

## <span data-ttu-id="7b142-125">출력</span><span class="sxs-lookup"><span data-stu-id="7b142-125">OUTPUTS</span></span>

### <span data-ttu-id="7b142-126">System.Void</span><span class="sxs-lookup"><span data-stu-id="7b142-126">System.Void</span></span>

## <span data-ttu-id="7b142-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7b142-127">NOTES</span></span>

## <span data-ttu-id="7b142-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b142-128">RELATED LINKS</span></span>

[<span data-ttu-id="7b142-129">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="7b142-129">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="7b142-130">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="7b142-130">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


