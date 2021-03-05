---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: ee65492adc8c2756a2d19871e4c673668d471c84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989739"
---
# <span data-ttu-id="542e8-101">Set-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="542e8-101">Set-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="542e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="542e8-102">SYNOPSIS</span></span>
<span data-ttu-id="542e8-103">지정된 인텔리전스 팩을 활성화하거나 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="542e8-103">Enables or disables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="542e8-104">구문</span><span class="sxs-lookup"><span data-stu-id="542e8-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="542e8-105">설명</span><span class="sxs-lookup"><span data-stu-id="542e8-105">DESCRIPTION</span></span>
<span data-ttu-id="542e8-106">**Set-AzOperationalInsightsIntelligencePack** cmdlet을 사용하면 활성화가  설정되어 있는 경우 지정된 인텔리전스 팩을 $True 설정하고 활성화가 설정되어 있는 경우 사용하지 않도록 $False. </span><span class="sxs-lookup"><span data-stu-id="542e8-106">The **Set-AzOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="542e8-107">예제</span><span class="sxs-lookup"><span data-stu-id="542e8-107">EXAMPLES</span></span>

### <span data-ttu-id="542e8-108">예제 1: 인텔리전스 팩 설정</span><span class="sxs-lookup"><span data-stu-id="542e8-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="542e8-109">이 명령은 지정된 인텔리전스 팩을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="542e8-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="542e8-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="542e8-110">PARAMETERS</span></span>

### <span data-ttu-id="542e8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="542e8-111">-DefaultProfile</span></span>
<span data-ttu-id="542e8-112">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="542e8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="542e8-113">-사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="542e8-113">-Enabled</span></span>
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

### <span data-ttu-id="542e8-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="542e8-114">-IntelligencePackName</span></span>
<span data-ttu-id="542e8-115">인텔리전스 팩 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="542e8-115">Specifies the Intelligence Pack name.</span></span>

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

### <span data-ttu-id="542e8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="542e8-116">-ResourceGroupName</span></span>
<span data-ttu-id="542e8-117">리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="542e8-117">Specifies the resource group name</span></span>

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

### <span data-ttu-id="542e8-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="542e8-118">-WorkspaceName</span></span>
<span data-ttu-id="542e8-119">작업 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="542e8-119">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="542e8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="542e8-120">CommonParameters</span></span>
<span data-ttu-id="542e8-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="542e8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="542e8-122">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="542e8-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="542e8-123">입력</span><span class="sxs-lookup"><span data-stu-id="542e8-123">INPUTS</span></span>

### <span data-ttu-id="542e8-124">System.String</span><span class="sxs-lookup"><span data-stu-id="542e8-124">System.String</span></span>

### <span data-ttu-id="542e8-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="542e8-125">System.Boolean</span></span>

## <span data-ttu-id="542e8-126">출력</span><span class="sxs-lookup"><span data-stu-id="542e8-126">OUTPUTS</span></span>

### <span data-ttu-id="542e8-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="542e8-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="542e8-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="542e8-128">NOTES</span></span>

## <span data-ttu-id="542e8-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="542e8-129">RELATED LINKS</span></span>

[<span data-ttu-id="542e8-130">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="542e8-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


