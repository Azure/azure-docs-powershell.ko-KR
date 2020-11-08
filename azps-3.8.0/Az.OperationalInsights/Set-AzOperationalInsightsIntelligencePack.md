---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: 73dd6e62ba6bac6ec2684822e257bbf5a02d6e31
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "94047284"
---
# <span data-ttu-id="02d17-101">Set-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="02d17-101">Set-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="02d17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02d17-102">SYNOPSIS</span></span>
<span data-ttu-id="02d17-103">지정 된 인텔리전스 팩을 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02d17-103">Enables or disables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="02d17-104">구문과</span><span class="sxs-lookup"><span data-stu-id="02d17-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="02d17-105">설명은</span><span class="sxs-lookup"><span data-stu-id="02d17-105">DESCRIPTION</span></span>
<span data-ttu-id="02d17-106">**AzOperationalInsightsIntelligencePack** Cmdlet은 *enabled* 가 $True로 설정 된 경우 지정 된 인텔리전스 팩을 사용할 수 있게 하 고, *enabled* 가 $False로 설정 된 경우 사용 하지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="02d17-106">The **Set-AzOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="02d17-107">예제의</span><span class="sxs-lookup"><span data-stu-id="02d17-107">EXAMPLES</span></span>

### <span data-ttu-id="02d17-108">예제 1: Intelligence 팩 설정</span><span class="sxs-lookup"><span data-stu-id="02d17-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="02d17-109">이 명령은 지정 된 인텔리전스 팩을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02d17-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="02d17-110">변수</span><span class="sxs-lookup"><span data-stu-id="02d17-110">PARAMETERS</span></span>

### <span data-ttu-id="02d17-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02d17-111">-DefaultProfile</span></span>
<span data-ttu-id="02d17-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="02d17-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02d17-113">-사용</span><span class="sxs-lookup"><span data-stu-id="02d17-113">-Enabled</span></span>
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

### <span data-ttu-id="02d17-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="02d17-114">-IntelligencePackName</span></span>
<span data-ttu-id="02d17-115">인텔리전스 팩 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02d17-115">Specifies the Intelligence Pack name.</span></span>

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

### <span data-ttu-id="02d17-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02d17-116">-ResourceGroupName</span></span>
<span data-ttu-id="02d17-117">리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02d17-117">Specifies the resource group name</span></span>

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

### <span data-ttu-id="02d17-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="02d17-118">-WorkspaceName</span></span>
<span data-ttu-id="02d17-119">작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02d17-119">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="02d17-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02d17-120">CommonParameters</span></span>
<span data-ttu-id="02d17-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="02d17-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02d17-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02d17-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02d17-123">입력</span><span class="sxs-lookup"><span data-stu-id="02d17-123">INPUTS</span></span>

### <span data-ttu-id="02d17-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="02d17-124">System.String</span></span>

### <span data-ttu-id="02d17-125">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="02d17-125">System.Boolean</span></span>

## <span data-ttu-id="02d17-126">출력</span><span class="sxs-lookup"><span data-stu-id="02d17-126">OUTPUTS</span></span>

### <span data-ttu-id="02d17-127">OperationalInsights. PSIntelligencePack/.</span><span class="sxs-lookup"><span data-stu-id="02d17-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="02d17-128">상속자</span><span class="sxs-lookup"><span data-stu-id="02d17-128">NOTES</span></span>

## <span data-ttu-id="02d17-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02d17-129">RELATED LINKS</span></span>

[<span data-ttu-id="02d17-130">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="02d17-130">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


