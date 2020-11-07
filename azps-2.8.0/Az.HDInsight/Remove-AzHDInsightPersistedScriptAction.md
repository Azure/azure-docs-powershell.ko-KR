---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: cfa99107875940854b9ad9c74061ec717a16c51e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689803"
---
# <span data-ttu-id="64550-101">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="64550-101">Remove-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="64550-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64550-102">SYNOPSIS</span></span>
<span data-ttu-id="64550-103">HDInsight 클러스터에서 지속형 스크립트 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="64550-103">Removes an persisted script action from an HDInsight cluster.</span></span>

## <span data-ttu-id="64550-104">구문과</span><span class="sxs-lookup"><span data-stu-id="64550-104">SYNTAX</span></span>

```
Remove-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64550-105">설명은</span><span class="sxs-lookup"><span data-stu-id="64550-105">DESCRIPTION</span></span>
<span data-ttu-id="64550-106">**AzHDInsightPersistedScriptAction** cmdlet은 지정 된 Azure HDInsight 클러스터의 지속형 스크립트 작업 목록에서 지속형 스크립트 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="64550-106">The **Remove-AzHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="64550-107">클러스터의 크기를 조정 하면 제거 된 스크립트도 더 이상 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64550-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="64550-108">예제의</span><span class="sxs-lookup"><span data-stu-id="64550-108">EXAMPLES</span></span>

### <span data-ttu-id="64550-109">예제 1: 클러스터의 지속형 스크립트 작업 목록에서 스크립트 동작 제거</span><span class="sxs-lookup"><span data-stu-id="64550-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="64550-110">이 명령은 지정 된 클러스터의 지속형 스크립트 작업 목록에서 Scriptaction 이라는 스크립트 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="64550-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="64550-111">변수</span><span class="sxs-lookup"><span data-stu-id="64550-111">PARAMETERS</span></span>

### <span data-ttu-id="64550-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="64550-112">-ClusterName</span></span>
<span data-ttu-id="64550-113">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64550-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="64550-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64550-114">-DefaultProfile</span></span>
<span data-ttu-id="64550-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="64550-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64550-116">-이름</span><span class="sxs-lookup"><span data-stu-id="64550-116">-Name</span></span>
<span data-ttu-id="64550-117">제거할 지속형 스크립트 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64550-117">Specifies the name of the persisted script action to be removed.</span></span>

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

### <span data-ttu-id="64550-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64550-118">-ResourceGroupName</span></span>
<span data-ttu-id="64550-119">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64550-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="64550-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64550-120">CommonParameters</span></span>
<span data-ttu-id="64550-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="64550-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64550-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64550-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64550-123">입력</span><span class="sxs-lookup"><span data-stu-id="64550-123">INPUTS</span></span>

### <span data-ttu-id="64550-124">않아야</span><span class="sxs-lookup"><span data-stu-id="64550-124">None</span></span>

## <span data-ttu-id="64550-125">출력</span><span class="sxs-lookup"><span data-stu-id="64550-125">OUTPUTS</span></span>

### <span data-ttu-id="64550-126">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="64550-126">System.Void</span></span>

## <span data-ttu-id="64550-127">상속자</span><span class="sxs-lookup"><span data-stu-id="64550-127">NOTES</span></span>

## <span data-ttu-id="64550-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="64550-128">RELATED LINKS</span></span>

[<span data-ttu-id="64550-129">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="64550-129">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="64550-130">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="64550-130">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


