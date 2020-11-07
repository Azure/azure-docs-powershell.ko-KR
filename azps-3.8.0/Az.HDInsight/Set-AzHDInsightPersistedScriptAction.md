---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: bff21d969a88282f3ba3c1d79d1f717c3c169265
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878509"
---
# <span data-ttu-id="dfac2-101">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="dfac2-101">Set-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="dfac2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfac2-102">SYNOPSIS</span></span>
<span data-ttu-id="dfac2-103">이전에 실행 한 스크립트 작업을 지속형 스크립트 작업으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfac2-103">Sets a previously executed script action to be a persisted script action.</span></span>

## <span data-ttu-id="dfac2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dfac2-104">SYNTAX</span></span>

```
Set-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfac2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dfac2-105">DESCRIPTION</span></span>
<span data-ttu-id="dfac2-106">**AzHDInsightPersistedScriptAction** cmdlet은 이전에 실행 된 스크립트 작업을 지속형 스크립트 작업으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfac2-106">The **Set-AzHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="dfac2-107">지정 된 스크립트 작업은 이전에 성공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfac2-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="dfac2-108">Azure HDInsight 클러스터의 크기를 조정할 때마다 스크립트 작업이 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dfac2-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="dfac2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="dfac2-109">EXAMPLES</span></span>

### <span data-ttu-id="dfac2-110">예제 1: 이전에 성공한 스크립트 작업을 유지 하거나 클러스터 확장에서 실행 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="dfac2-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="dfac2-111">이 명령은 이전에 성공한 스크립트 작업을 지속형 스크립트 작업으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfac2-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="dfac2-112">변수</span><span class="sxs-lookup"><span data-stu-id="dfac2-112">PARAMETERS</span></span>

### <span data-ttu-id="dfac2-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="dfac2-113">-ClusterName</span></span>
<span data-ttu-id="dfac2-114">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfac2-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="dfac2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfac2-115">-DefaultProfile</span></span>
<span data-ttu-id="dfac2-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="dfac2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dfac2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfac2-117">-ResourceGroupName</span></span>
<span data-ttu-id="dfac2-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfac2-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="dfac2-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="dfac2-119">-ScriptExecutionId</span></span>
<span data-ttu-id="dfac2-120">유지 하도록 승격할 스크립트 작업의 실행 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfac2-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="dfac2-121">이 스크립트 동작은 승격 되려면 성공이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfac2-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="dfac2-122">Get-AzHDInsightScriptActionHistory를 사용 하 여 스크립트 작업 실행 ID를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dfac2-122">You can find the script action execution ID using Get-AzHDInsightScriptActionHistory.</span></span>

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

### <span data-ttu-id="dfac2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfac2-123">CommonParameters</span></span>
<span data-ttu-id="dfac2-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfac2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfac2-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfac2-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfac2-126">입력</span><span class="sxs-lookup"><span data-stu-id="dfac2-126">INPUTS</span></span>

### <span data-ttu-id="dfac2-127">않아야</span><span class="sxs-lookup"><span data-stu-id="dfac2-127">None</span></span>

## <span data-ttu-id="dfac2-128">출력</span><span class="sxs-lookup"><span data-stu-id="dfac2-128">OUTPUTS</span></span>

### <span data-ttu-id="dfac2-129">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="dfac2-129">System.Void</span></span>

## <span data-ttu-id="dfac2-130">상속자</span><span class="sxs-lookup"><span data-stu-id="dfac2-130">NOTES</span></span>

## <span data-ttu-id="dfac2-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dfac2-131">RELATED LINKS</span></span>

[<span data-ttu-id="dfac2-132">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="dfac2-132">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="dfac2-133">제거-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="dfac2-133">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)


