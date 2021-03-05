---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: a56fd0303e6f610468c9f2784396023fd20edef4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965627"
---
# <span data-ttu-id="0259b-101">Get-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="0259b-101">Get-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="0259b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0259b-102">SYNOPSIS</span></span>
<span data-ttu-id="0259b-103">사용 가능한 인텔리전스 팩을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0259b-103">Gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="0259b-104">구문</span><span class="sxs-lookup"><span data-stu-id="0259b-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0259b-105">설명</span><span class="sxs-lookup"><span data-stu-id="0259b-105">DESCRIPTION</span></span>
<span data-ttu-id="0259b-106">**Get-AzOperationalInsightsIntelligencePack** cmdlet은 사용 가능한 인텔리전스 팩을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0259b-106">The **Get-AzOperationalInsightsIntelligencePack** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="0259b-107">예제</span><span class="sxs-lookup"><span data-stu-id="0259b-107">EXAMPLES</span></span>

### <span data-ttu-id="0259b-108">예제 1: 인텔리전스 팩을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0259b-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="0259b-109">이 명령은 사용 가능한 인텔리전스 팩을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0259b-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="0259b-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0259b-110">PARAMETERS</span></span>

### <span data-ttu-id="0259b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0259b-111">-DefaultProfile</span></span>
<span data-ttu-id="0259b-112">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0259b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0259b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0259b-113">-ResourceGroupName</span></span>
<span data-ttu-id="0259b-114">작업 영역이 포함된 Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0259b-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="0259b-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0259b-115">-WorkspaceName</span></span>
<span data-ttu-id="0259b-116">작업 영역 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0259b-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="0259b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0259b-117">CommonParameters</span></span>
<span data-ttu-id="0259b-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0259b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0259b-119">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0259b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0259b-120">입력</span><span class="sxs-lookup"><span data-stu-id="0259b-120">INPUTS</span></span>

### <span data-ttu-id="0259b-121">System.String</span><span class="sxs-lookup"><span data-stu-id="0259b-121">System.String</span></span>

## <span data-ttu-id="0259b-122">출력</span><span class="sxs-lookup"><span data-stu-id="0259b-122">OUTPUTS</span></span>

### <span data-ttu-id="0259b-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="0259b-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="0259b-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0259b-124">NOTES</span></span>

## <span data-ttu-id="0259b-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0259b-125">RELATED LINKS</span></span>

[<span data-ttu-id="0259b-126">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0259b-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


