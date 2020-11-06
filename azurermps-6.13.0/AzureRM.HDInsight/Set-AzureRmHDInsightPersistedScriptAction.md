---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/set-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: 07f501be4ac775a9d80c43173e13fccf3057cc26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527951"
---
# <span data-ttu-id="116b4-101">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="116b4-101">Set-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="116b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="116b4-102">SYNOPSIS</span></span>
<span data-ttu-id="116b4-103">이전에 실행 한 스크립트 작업을 지속형 스크립트 작업으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="116b4-103">Sets a previously executed script action to be a persisted script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="116b4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="116b4-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="116b4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="116b4-105">DESCRIPTION</span></span>
<span data-ttu-id="116b4-106">**AzureRmHDInsightPersistedScriptAction** cmdlet은 이전에 실행 된 스크립트 작업을 지속형 스크립트 작업으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="116b4-106">The **Set-AzureRmHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="116b4-107">지정 된 스크립트 작업은 이전에 성공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="116b4-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="116b4-108">Azure HDInsight 클러스터의 크기를 조정할 때마다 스크립트 작업이 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="116b4-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="116b4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="116b4-109">EXAMPLES</span></span>

### <span data-ttu-id="116b4-110">예제 1: 이전에 성공한 스크립트 작업을 유지 하거나 클러스터 확장에서 실행 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="116b4-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzureRmHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="116b4-111">이 명령은 이전에 성공한 스크립트 작업을 지속형 스크립트 작업으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="116b4-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="116b4-112">변수</span><span class="sxs-lookup"><span data-stu-id="116b4-112">PARAMETERS</span></span>

### <span data-ttu-id="116b4-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="116b4-113">-ClusterName</span></span>
<span data-ttu-id="116b4-114">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="116b4-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="116b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="116b4-115">-DefaultProfile</span></span>
<span data-ttu-id="116b4-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="116b4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="116b4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="116b4-117">-ResourceGroupName</span></span>
<span data-ttu-id="116b4-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="116b4-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="116b4-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="116b4-119">-ScriptExecutionId</span></span>
<span data-ttu-id="116b4-120">유지 하도록 승격할 스크립트 작업의 실행 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="116b4-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="116b4-121">이 스크립트 동작은 승격 되려면 성공이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="116b4-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="116b4-122">Get-AzureRmHDInsightScriptActionHistory를 사용 하 여 스크립트 작업 실행 ID를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="116b4-122">You can find the script action execution ID using Get-AzureRmHDInsightScriptActionHistory.</span></span>

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

### <span data-ttu-id="116b4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="116b4-123">CommonParameters</span></span>
<span data-ttu-id="116b4-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="116b4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="116b4-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="116b4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="116b4-126">입력</span><span class="sxs-lookup"><span data-stu-id="116b4-126">INPUTS</span></span>

### <span data-ttu-id="116b4-127">않아야</span><span class="sxs-lookup"><span data-stu-id="116b4-127">None</span></span>

## <span data-ttu-id="116b4-128">출력</span><span class="sxs-lookup"><span data-stu-id="116b4-128">OUTPUTS</span></span>

### <span data-ttu-id="116b4-129">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="116b4-129">System.Void</span></span>

## <span data-ttu-id="116b4-130">상속자</span><span class="sxs-lookup"><span data-stu-id="116b4-130">NOTES</span></span>

## <span data-ttu-id="116b4-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="116b4-131">RELATED LINKS</span></span>

[<span data-ttu-id="116b4-132">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="116b4-132">Get-AzureRmHDInsightPersistedScriptAction</span></span>](./Get-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="116b4-133">제거-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="116b4-133">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](./Remove-AzureRmHDInsightPersistedScriptAction.md)


