---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: fa4df1d2b2149a0bc9c637ffefd5c60e52fa0059
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93701948"
---
# <span data-ttu-id="ef643-101">Get-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="ef643-101">Get-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="ef643-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef643-102">SYNOPSIS</span></span>
<span data-ttu-id="ef643-103">사용할 수 있는 인텔리전스 팩을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ef643-103">Gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="ef643-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ef643-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef643-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ef643-105">DESCRIPTION</span></span>
<span data-ttu-id="ef643-106">**Get-AzOperationalInsightsIntelligencePack** cmdlet은 사용 가능한 인텔리전스 팩을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ef643-106">The **Get-AzOperationalInsightsIntelligencePack** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="ef643-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ef643-107">EXAMPLES</span></span>

### <span data-ttu-id="ef643-108">예제 1: 인텔리전스 팩 가져오기</span><span class="sxs-lookup"><span data-stu-id="ef643-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="ef643-109">이 명령은 사용 가능한 인텔리전스 팩을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ef643-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="ef643-110">변수</span><span class="sxs-lookup"><span data-stu-id="ef643-110">PARAMETERS</span></span>

### <span data-ttu-id="ef643-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef643-111">-DefaultProfile</span></span>
<span data-ttu-id="ef643-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ef643-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef643-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef643-113">-ResourceGroupName</span></span>
<span data-ttu-id="ef643-114">작업 영역을 포함 하는 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef643-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef643-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ef643-115">-WorkspaceName</span></span>
<span data-ttu-id="ef643-116">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef643-116">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef643-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef643-117">CommonParameters</span></span>
<span data-ttu-id="ef643-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef643-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef643-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef643-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef643-120">입력</span><span class="sxs-lookup"><span data-stu-id="ef643-120">INPUTS</span></span>

### <span data-ttu-id="ef643-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ef643-121">System.String</span></span>

## <span data-ttu-id="ef643-122">출력</span><span class="sxs-lookup"><span data-stu-id="ef643-122">OUTPUTS</span></span>

### <span data-ttu-id="ef643-123">OperationalInsights. PSIntelligencePack/.</span><span class="sxs-lookup"><span data-stu-id="ef643-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="ef643-124">상속자</span><span class="sxs-lookup"><span data-stu-id="ef643-124">NOTES</span></span>

## <span data-ttu-id="ef643-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef643-125">RELATED LINKS</span></span>

[<span data-ttu-id="ef643-126">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ef643-126">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


