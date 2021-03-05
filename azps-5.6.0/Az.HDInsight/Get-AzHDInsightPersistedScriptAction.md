---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 136099b4fb37952825afbf82ba99a11695b901a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009104"
---
# <span data-ttu-id="4b15b-101">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="4b15b-101">Get-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="4b15b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b15b-102">SYNOPSIS</span></span>
<span data-ttu-id="4b15b-103">클러스터에 대한 지속 스크립트 작업을 얻게 하여 시간 순서로 나열하거나 지정된 지속형 스크립트 작업에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4b15b-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="4b15b-104">구문</span><span class="sxs-lookup"><span data-stu-id="4b15b-104">SYNTAX</span></span>

```
Get-AzHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b15b-105">설명</span><span class="sxs-lookup"><span data-stu-id="4b15b-105">DESCRIPTION</span></span>
<span data-ttu-id="4b15b-106">**Get-AzHDInsightPersistedScriptAction** cmdlet은 Azure HDInsight 클러스터에 대한 영구 스크립트 작업을 얻게 하여 시간 순서대로 나열하거나 지정된 영구 스크립트 작업에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4b15b-106">The **Get-AzHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="4b15b-107">예제</span><span class="sxs-lookup"><span data-stu-id="4b15b-107">EXAMPLES</span></span>

### <span data-ttu-id="4b15b-108">예제 1: 클러스터에서 지속된 스크립트 작업 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4b15b-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="4b15b-109">이 명령은 your-hadoop-001이라는 클러스터에서 영구 스크립트 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4b15b-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="4b15b-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4b15b-110">PARAMETERS</span></span>

### <span data-ttu-id="4b15b-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4b15b-111">-ClusterName</span></span>
<span data-ttu-id="4b15b-112">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b15b-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="4b15b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b15b-113">-DefaultProfile</span></span>
<span data-ttu-id="4b15b-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4b15b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b15b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4b15b-115">-Name</span></span>
<span data-ttu-id="4b15b-116">영구 스크립트 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b15b-116">Specifies the name of the persisted script action.</span></span>

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

### <span data-ttu-id="4b15b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b15b-117">-ResourceGroupName</span></span>
<span data-ttu-id="4b15b-118">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b15b-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4b15b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b15b-119">CommonParameters</span></span>
<span data-ttu-id="4b15b-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4b15b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b15b-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b15b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b15b-122">입력</span><span class="sxs-lookup"><span data-stu-id="4b15b-122">INPUTS</span></span>

### <span data-ttu-id="4b15b-123">없음</span><span class="sxs-lookup"><span data-stu-id="4b15b-123">None</span></span>

## <span data-ttu-id="4b15b-124">출력</span><span class="sxs-lookup"><span data-stu-id="4b15b-124">OUTPUTS</span></span>

### <span data-ttu-id="4b15b-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span><span class="sxs-lookup"><span data-stu-id="4b15b-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span></span>

## <span data-ttu-id="4b15b-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4b15b-126">NOTES</span></span>

## <span data-ttu-id="4b15b-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b15b-127">RELATED LINKS</span></span>

[<span data-ttu-id="4b15b-128">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="4b15b-128">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="4b15b-129">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="4b15b-129">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


