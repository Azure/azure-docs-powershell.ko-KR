---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: a8d799cec6278149cb4c08faf68584fb7968f85e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179220"
---
# <span data-ttu-id="f5384-101">Set-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="f5384-101">Set-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="f5384-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5384-102">SYNOPSIS</span></span>
<span data-ttu-id="f5384-103">지정된 인텔리전스 팩을 활성화하거나 비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="f5384-103">Enables or disables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="f5384-104">구문</span><span class="sxs-lookup"><span data-stu-id="f5384-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5384-105">설명</span><span class="sxs-lookup"><span data-stu-id="f5384-105">DESCRIPTION</span></span>
<span data-ttu-id="f5384-106">**Set-AzOperationalInsightsIntelligencePack** cmdlet은 *Enabled가* 설정되어 있는 경우 지정된 인텔리전스 팩을 $True 사용하도록 *설정하고, Enabled가* $False.</span><span class="sxs-lookup"><span data-stu-id="f5384-106">The **Set-AzOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="f5384-107">예제</span><span class="sxs-lookup"><span data-stu-id="f5384-107">EXAMPLES</span></span>

### <span data-ttu-id="f5384-108">예제 1: 인텔리전스 팩 설정</span><span class="sxs-lookup"><span data-stu-id="f5384-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="f5384-109">이 명령은 지정된 인텔리전스 팩을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f5384-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="f5384-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5384-110">PARAMETERS</span></span>

### <span data-ttu-id="f5384-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5384-111">-DefaultProfile</span></span>
<span data-ttu-id="f5384-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f5384-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5384-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="f5384-113">-Enabled</span></span>
```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5384-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="f5384-114">-IntelligencePackName</span></span>
<span data-ttu-id="f5384-115">인텔리전스 팩 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f5384-115">Specifies the Intelligence Pack name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5384-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5384-116">-ResourceGroupName</span></span>
<span data-ttu-id="f5384-117">리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f5384-117">Specifies the resource group name</span></span>

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

### <span data-ttu-id="f5384-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f5384-118">-WorkspaceName</span></span>
<span data-ttu-id="f5384-119">작업 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f5384-119">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="f5384-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5384-120">CommonParameters</span></span>
<span data-ttu-id="f5384-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f5384-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5384-122">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f5384-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5384-123">입력</span><span class="sxs-lookup"><span data-stu-id="f5384-123">INPUTS</span></span>

### <span data-ttu-id="f5384-124">System.String</span><span class="sxs-lookup"><span data-stu-id="f5384-124">System.String</span></span>

### <span data-ttu-id="f5384-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f5384-125">System.Boolean</span></span>

## <span data-ttu-id="f5384-126">출력</span><span class="sxs-lookup"><span data-stu-id="f5384-126">OUTPUTS</span></span>

### <span data-ttu-id="f5384-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="f5384-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="f5384-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f5384-128">NOTES</span></span>

## <span data-ttu-id="f5384-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5384-129">RELATED LINKS</span></span>

[<span data-ttu-id="f5384-130">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5384-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


