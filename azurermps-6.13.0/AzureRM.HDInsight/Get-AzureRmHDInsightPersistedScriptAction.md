---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: 6305e9a312eb5ebb34de56bcef8a8894b1bd7dd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530310"
---
# <span data-ttu-id="c65bf-101">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="c65bf-101">Get-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="c65bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c65bf-102">SYNOPSIS</span></span>
<span data-ttu-id="c65bf-103">클러스터에 대 한 지속형 스크립트 작업을 가져와 시간 순서 대로 나열 하거나 지정 된 지속형 스크립트 작업에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c65bf-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c65bf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c65bf-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c65bf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c65bf-105">DESCRIPTION</span></span>
<span data-ttu-id="c65bf-106">**AzureRmHDInsightPersistedScriptAction** Cmdlet은 Azure HDInsight 클러스터에 대 한 지속형 스크립트 작업을 가져와 시간 순서 대로 나열 하거나 지정 된 지속형 스크립트 작업에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c65bf-106">The **Get-AzureRmHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="c65bf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c65bf-107">EXAMPLES</span></span>

### <span data-ttu-id="c65bf-108">예제 1: 클러스터에서 지속형 스크립트 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="c65bf-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="c65bf-109">이 명령은-hadoop-001 이라는 클러스터에서 유지 된 스크립트 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c65bf-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="c65bf-110">변수</span><span class="sxs-lookup"><span data-stu-id="c65bf-110">PARAMETERS</span></span>

### <span data-ttu-id="c65bf-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c65bf-111">-ClusterName</span></span>
<span data-ttu-id="c65bf-112">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c65bf-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="c65bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c65bf-113">-DefaultProfile</span></span>
<span data-ttu-id="c65bf-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c65bf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c65bf-115">-이름</span><span class="sxs-lookup"><span data-stu-id="c65bf-115">-Name</span></span>
<span data-ttu-id="c65bf-116">지속형 스크립트 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c65bf-116">Specifies the name of the persisted script action.</span></span>

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

### <span data-ttu-id="c65bf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c65bf-117">-ResourceGroupName</span></span>
<span data-ttu-id="c65bf-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c65bf-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c65bf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c65bf-119">CommonParameters</span></span>
<span data-ttu-id="c65bf-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c65bf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c65bf-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c65bf-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c65bf-122">입력</span><span class="sxs-lookup"><span data-stu-id="c65bf-122">INPUTS</span></span>

### <span data-ttu-id="c65bf-123">않아야</span><span class="sxs-lookup"><span data-stu-id="c65bf-123">None</span></span>

## <span data-ttu-id="c65bf-124">출력</span><span class="sxs-lookup"><span data-stu-id="c65bf-124">OUTPUTS</span></span>

### <span data-ttu-id="c65bf-125">AzureHDInsightRuntimeScriptAction를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="c65bf-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span></span>

## <span data-ttu-id="c65bf-126">상속자</span><span class="sxs-lookup"><span data-stu-id="c65bf-126">NOTES</span></span>

## <span data-ttu-id="c65bf-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c65bf-127">RELATED LINKS</span></span>

[<span data-ttu-id="c65bf-128">제거-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="c65bf-128">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](./Remove-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="c65bf-129">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="c65bf-129">Set-AzureRmHDInsightPersistedScriptAction</span></span>](./Set-AzureRmHDInsightPersistedScriptAction.md)


