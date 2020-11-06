---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightScriptActionHistory.md
ms.openlocfilehash: 5e3ee9de0adf511407013ef346a2867cb43fb11c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537220"
---
# <span data-ttu-id="a8f60-101">Get-AzureRmHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="a8f60-101">Get-AzureRmHDInsightScriptActionHistory</span></span>

## <span data-ttu-id="a8f60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8f60-102">SYNOPSIS</span></span>
<span data-ttu-id="a8f60-103">클러스터에 대 한 스크립트 작업 기록을 가져오고이를 역순으로 나열 하거나 이전에 실행 된 스크립트 작업의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a8f60-103">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8f60-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a8f60-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8f60-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a8f60-105">DESCRIPTION</span></span>
<span data-ttu-id="a8f60-106">**AzureRmHDInsightScriptActionHistory** Cmdlet은 Azure HDInsight 클러스터에 대 한 스크립트 작업 기록을 가져와 그 순서의 역순으로 나열 하거나 이전에 실행 된 스크립트 작업의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a8f60-106">The **Get-AzureRmHDInsightScriptActionHistory** cmdlet gets the script action history for an Azure HDInsight cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="a8f60-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a8f60-107">EXAMPLES</span></span>

### <span data-ttu-id="a8f60-108">예제 1: 클러스터에 대 한 스크립트 작업 실행 기록 가져오기</span><span class="sxs-lookup"><span data-stu-id="a8f60-108">Example 1: Get the history of script actions executions for a cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

<span data-ttu-id="a8f60-109">이 명령은 hadoop-001 클러스터에 대 한 스크립트 작업 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a8f60-109">This command gets the history of script actions for the cluster your-hadoop-001.</span></span>

## <span data-ttu-id="a8f60-110">변수</span><span class="sxs-lookup"><span data-stu-id="a8f60-110">PARAMETERS</span></span>

### <span data-ttu-id="a8f60-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a8f60-111">-ClusterName</span></span>
<span data-ttu-id="a8f60-112">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8f60-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="a8f60-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8f60-113">-ResourceGroupName</span></span>
<span data-ttu-id="a8f60-114">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8f60-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a8f60-115">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="a8f60-115">-ScriptExecutionId</span></span>
<span data-ttu-id="a8f60-116">실행 된 스크립트 작업의 실행 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8f60-116">Specifies the execution ID of the executed script action.</span></span>

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

### <span data-ttu-id="a8f60-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8f60-117">-DefaultProfile</span></span>
<span data-ttu-id="a8f60-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a8f60-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8f60-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8f60-119">CommonParameters</span></span>
<span data-ttu-id="a8f60-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8f60-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8f60-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8f60-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8f60-122">입력</span><span class="sxs-lookup"><span data-stu-id="a8f60-122">INPUTS</span></span>

## <span data-ttu-id="a8f60-123">출력</span><span class="sxs-lookup"><span data-stu-id="a8f60-123">OUTPUTS</span></span>

### <span data-ttu-id="a8f60-124">System.webserver. e 1. a n t. m a. m a. AzureHDInsightRuntimeScriptActionDetail]</span><span class="sxs-lookup"><span data-stu-id="a8f60-124">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail]</span></span>

## <span data-ttu-id="a8f60-125">상속자</span><span class="sxs-lookup"><span data-stu-id="a8f60-125">NOTES</span></span>

## <span data-ttu-id="a8f60-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a8f60-126">RELATED LINKS</span></span>

