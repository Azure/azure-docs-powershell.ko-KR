---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: d0ca241cc29bedcd3a34f866fa2b7a19fceb0745
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711566"
---
# <span data-ttu-id="a7f36-101">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="a7f36-101">Get-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="a7f36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7f36-102">SYNOPSIS</span></span>
<span data-ttu-id="a7f36-103">클러스터에 대 한 지속형 스크립트 작업을 가져와 시간 순서 대로 나열 하거나 지정 된 지속형 스크립트 작업에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a7f36-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7f36-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a7f36-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7f36-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a7f36-105">DESCRIPTION</span></span>
<span data-ttu-id="a7f36-106">**AzureRmHDInsightPersistedScriptAction** Cmdlet은 Azure HDInsight 클러스터에 대 한 지속형 스크립트 작업을 가져와 시간 순서 대로 나열 하거나 지정 된 지속형 스크립트 작업에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a7f36-106">The **Get-AzureRmHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="a7f36-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a7f36-107">EXAMPLES</span></span>

### <span data-ttu-id="a7f36-108">예제 1: 클러스터에서 지속형 스크립트 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="a7f36-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="a7f36-109">이 명령은-hadoop-001 이라는 클러스터에서 유지 된 스크립트 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a7f36-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="a7f36-110">변수</span><span class="sxs-lookup"><span data-stu-id="a7f36-110">PARAMETERS</span></span>

### <span data-ttu-id="a7f36-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a7f36-111">-ClusterName</span></span>
<span data-ttu-id="a7f36-112">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7f36-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="a7f36-113">-이름</span><span class="sxs-lookup"><span data-stu-id="a7f36-113">-Name</span></span>
<span data-ttu-id="a7f36-114">지속형 스크립트 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7f36-114">Specifies the name of the persisted script action.</span></span>

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

### <span data-ttu-id="a7f36-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7f36-115">-ResourceGroupName</span></span>
<span data-ttu-id="a7f36-116">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7f36-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a7f36-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7f36-117">-DefaultProfile</span></span>
<span data-ttu-id="a7f36-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a7f36-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7f36-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7f36-119">CommonParameters</span></span>
<span data-ttu-id="a7f36-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7f36-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7f36-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7f36-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7f36-122">입력</span><span class="sxs-lookup"><span data-stu-id="a7f36-122">INPUTS</span></span>

## <span data-ttu-id="a7f36-123">출력</span><span class="sxs-lookup"><span data-stu-id="a7f36-123">OUTPUTS</span></span>

### <span data-ttu-id="a7f36-124">System.webserver. e 1. a n t. m a. m a. AzureHDInsightRuntimeScriptAction]</span><span class="sxs-lookup"><span data-stu-id="a7f36-124">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction]</span></span>

## <span data-ttu-id="a7f36-125">상속자</span><span class="sxs-lookup"><span data-stu-id="a7f36-125">NOTES</span></span>

## <span data-ttu-id="a7f36-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7f36-126">RELATED LINKS</span></span>

[<span data-ttu-id="a7f36-127">제거-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="a7f36-127">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](./Remove-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="a7f36-128">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="a7f36-128">Set-AzureRmHDInsightPersistedScriptAction</span></span>](./Set-AzureRmHDInsightPersistedScriptAction.md)


