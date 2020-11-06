---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: c70b4fecc9be5937d24ca4bc84b8aa6554daf482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537751"
---
# <span data-ttu-id="c239f-101">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="c239f-101">Get-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="c239f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c239f-102">SYNOPSIS</span></span>
<span data-ttu-id="c239f-103">클러스터에 대 한 지속형 스크립트 작업을 가져와 시간 순서 대로 나열 하거나 지정 된 지속형 스크립트 작업에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c239f-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c239f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c239f-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c239f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c239f-105">DESCRIPTION</span></span>
<span data-ttu-id="c239f-106">**AzureRmHDInsightPersistedScriptAction** Cmdlet은 Azure HDInsight 클러스터에 대 한 지속형 스크립트 작업을 가져와 시간 순서 대로 나열 하거나 지정 된 지속형 스크립트 작업에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c239f-106">The **Get-AzureRmHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="c239f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c239f-107">EXAMPLES</span></span>

### <span data-ttu-id="c239f-108">예제 1: 클러스터에서 지속형 스크립트 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="c239f-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="c239f-109">이 명령은-hadoop-001 이라는 클러스터에서 유지 된 스크립트 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c239f-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="c239f-110">변수</span><span class="sxs-lookup"><span data-stu-id="c239f-110">PARAMETERS</span></span>

### <span data-ttu-id="c239f-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c239f-111">-ClusterName</span></span>
<span data-ttu-id="c239f-112">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c239f-112">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c239f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c239f-113">-DefaultProfile</span></span>
<span data-ttu-id="c239f-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c239f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c239f-115">-이름</span><span class="sxs-lookup"><span data-stu-id="c239f-115">-Name</span></span>
<span data-ttu-id="c239f-116">지속형 스크립트 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c239f-116">Specifies the name of the persisted script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c239f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c239f-117">-ResourceGroupName</span></span>
<span data-ttu-id="c239f-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c239f-118">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c239f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c239f-119">CommonParameters</span></span>
<span data-ttu-id="c239f-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c239f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c239f-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c239f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c239f-122">입력</span><span class="sxs-lookup"><span data-stu-id="c239f-122">INPUTS</span></span>

### <span data-ttu-id="c239f-123">않아야</span><span class="sxs-lookup"><span data-stu-id="c239f-123">None</span></span>
<span data-ttu-id="c239f-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c239f-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c239f-125">출력</span><span class="sxs-lookup"><span data-stu-id="c239f-125">OUTPUTS</span></span>

### <span data-ttu-id="c239f-126">System.webserver. e 1. a n t. m a. m a. AzureHDInsightRuntimeScriptAction]</span><span class="sxs-lookup"><span data-stu-id="c239f-126">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction]</span></span>

## <span data-ttu-id="c239f-127">상속자</span><span class="sxs-lookup"><span data-stu-id="c239f-127">NOTES</span></span>

## <span data-ttu-id="c239f-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c239f-128">RELATED LINKS</span></span>

[<span data-ttu-id="c239f-129">제거-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="c239f-129">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](./Remove-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="c239f-130">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="c239f-130">Set-AzureRmHDInsightPersistedScriptAction</span></span>](./Set-AzureRmHDInsightPersistedScriptAction.md)


