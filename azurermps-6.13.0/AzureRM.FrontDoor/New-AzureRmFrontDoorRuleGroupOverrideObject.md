---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRuleGroupOverrideObject.md
ms.openlocfilehash: 02253a59a7f05bfdecd8147325575605334f13ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524407"
---
# <span data-ttu-id="47a41-101">New-AzureRmFrontDoorRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="47a41-101">New-AzureRmFrontDoorRuleGroupOverrideObject</span></span>

## <span data-ttu-id="47a41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47a41-102">SYNOPSIS</span></span>
<span data-ttu-id="47a41-103">WAF 정책 만들기에 대 한 RuleGroupOverride 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="47a41-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47a41-104">구문과</span><span class="sxs-lookup"><span data-stu-id="47a41-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorRuleGroupOverrideObject -Override <PSRuleGroupOverride> -Action <PSAction>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47a41-105">설명은</span><span class="sxs-lookup"><span data-stu-id="47a41-105">DESCRIPTION</span></span>
<span data-ttu-id="47a41-106">WAF 정책 만들기에 대 한 RuleGroupOverride 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="47a41-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="47a41-107">예제의</span><span class="sxs-lookup"><span data-stu-id="47a41-107">EXAMPLES</span></span>

### <span data-ttu-id="47a41-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="47a41-108">Example 1</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorRuleGroupOverrideObject -Override SqlInjection -Action Block

Action RuleGroupOverride
------ -----------------
 Block      SqlInjection
```

<span data-ttu-id="47a41-109">RuleGroupOverride 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="47a41-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="47a41-110">변수</span><span class="sxs-lookup"><span data-stu-id="47a41-110">PARAMETERS</span></span>

### <span data-ttu-id="47a41-111">-작업</span><span class="sxs-lookup"><span data-stu-id="47a41-111">-Action</span></span>
<span data-ttu-id="47a41-112">작업 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="47a41-112">Type of Actions.</span></span>
<span data-ttu-id="47a41-113">사용할 수 있는 값은 다음과 같습니다. ' 허용 ', ' 차단 ', ' 로그 '</span><span class="sxs-lookup"><span data-stu-id="47a41-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a41-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47a41-114">-DefaultProfile</span></span>
<span data-ttu-id="47a41-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="47a41-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47a41-116">-Override</span><span class="sxs-lookup"><span data-stu-id="47a41-116">-Override</span></span>
<span data-ttu-id="47a41-117">OverrideruleGroup에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="47a41-117">Describes overrideruleGroup.</span></span>
<span data-ttu-id="47a41-118">사용할 수 있는 값은 다음과 같습니다. ' SqlInjection ', ' XSS '</span><span class="sxs-lookup"><span data-stu-id="47a41-118">Possible values include: 'SqlInjection', 'XSS'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRuleGroupOverride
Parameter Sets: (All)
Aliases:
Accepted values: SqlInjection, XSS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a41-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47a41-119">CommonParameters</span></span>
<span data-ttu-id="47a41-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="47a41-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47a41-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47a41-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47a41-122">입력</span><span class="sxs-lookup"><span data-stu-id="47a41-122">INPUTS</span></span>

### <span data-ttu-id="47a41-123">않아야</span><span class="sxs-lookup"><span data-stu-id="47a41-123">None</span></span>

## <span data-ttu-id="47a41-124">출력</span><span class="sxs-lookup"><span data-stu-id="47a41-124">OUTPUTS</span></span>

### <span data-ttu-id="47a41-125">FrontDoor. PSAzureRuleGroupOverride/.</span><span class="sxs-lookup"><span data-stu-id="47a41-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="47a41-126">상속자</span><span class="sxs-lookup"><span data-stu-id="47a41-126">NOTES</span></span>

## <span data-ttu-id="47a41-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="47a41-127">RELATED LINKS</span></span>

[<span data-ttu-id="47a41-128">새로운 AzureRmFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="47a41-128">New-AzureRmFrontDoorManagedRuleObject</span></span>](./New-AzureRmFrontDoorManagedRuleObject.md)
