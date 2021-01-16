---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 56056e2933254401645a30e190a3a181b0c4514f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338246"
---
# <span data-ttu-id="b0d8f-101">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="b0d8f-101">Get-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="b0d8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0d8f-102">SYNOPSIS</span></span>
<span data-ttu-id="b0d8f-103">클러스터에 대한 지속형 스크립트 작업을 얻거나 시간 순서로 나열하거나 지정된 지속형 스크립트 동작에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b0d8f-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="b0d8f-104">구문</span><span class="sxs-lookup"><span data-stu-id="b0d8f-104">SYNTAX</span></span>

```
Get-AzHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0d8f-105">설명</span><span class="sxs-lookup"><span data-stu-id="b0d8f-105">DESCRIPTION</span></span>
<span data-ttu-id="b0d8f-106">**Get-AzHDInsightPersistedScriptAction** cmdlet은 Azure HDInsight 클러스터에 대한 지속형 스크립트 작업을 사용하여 시간 순서로 나열하거나 지정된 지속형 스크립트 작업에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b0d8f-106">The **Get-AzHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="b0d8f-107">예제</span><span class="sxs-lookup"><span data-stu-id="b0d8f-107">EXAMPLES</span></span>

### <span data-ttu-id="b0d8f-108">예제 1: 클러스터에서 지속된 스크립트 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="b0d8f-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="b0d8f-109">이 명령은 your-hadoop-001이라는 클러스터에서 지속형 스크립트 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b0d8f-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="b0d8f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0d8f-110">PARAMETERS</span></span>

### <span data-ttu-id="b0d8f-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b0d8f-111">-ClusterName</span></span>
<span data-ttu-id="b0d8f-112">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b0d8f-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="b0d8f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0d8f-113">-DefaultProfile</span></span>
<span data-ttu-id="b0d8f-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b0d8f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0d8f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b0d8f-115">-Name</span></span>
<span data-ttu-id="b0d8f-116">지속된 스크립트 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b0d8f-116">Specifies the name of the persisted script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0d8f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0d8f-117">-ResourceGroupName</span></span>
<span data-ttu-id="b0d8f-118">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b0d8f-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b0d8f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0d8f-119">CommonParameters</span></span>
<span data-ttu-id="b0d8f-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b0d8f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0d8f-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b0d8f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0d8f-122">입력</span><span class="sxs-lookup"><span data-stu-id="b0d8f-122">INPUTS</span></span>

### <span data-ttu-id="b0d8f-123">없음</span><span class="sxs-lookup"><span data-stu-id="b0d8f-123">None</span></span>

## <span data-ttu-id="b0d8f-124">출력</span><span class="sxs-lookup"><span data-stu-id="b0d8f-124">OUTPUTS</span></span>

### <span data-ttu-id="b0d8f-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span><span class="sxs-lookup"><span data-stu-id="b0d8f-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span></span>

## <span data-ttu-id="b0d8f-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b0d8f-126">NOTES</span></span>

## <span data-ttu-id="b0d8f-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0d8f-127">RELATED LINKS</span></span>

[<span data-ttu-id="b0d8f-128">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="b0d8f-128">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="b0d8f-129">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="b0d8f-129">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


