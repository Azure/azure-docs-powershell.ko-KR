---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoormanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorManagedRuleObject.md
ms.openlocfilehash: 236cb9ff263f97ae52ea5d3226f4defec00c662a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702930"
---
# <span data-ttu-id="03bfe-101">New-AzureRmFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="03bfe-101">New-AzureRmFrontDoorManagedRuleObject</span></span>

## <span data-ttu-id="03bfe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03bfe-102">SYNOPSIS</span></span>
<span data-ttu-id="03bfe-103">WAF 정책 만들기에 대 한 ManagedRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="03bfe-103">Create ManagedRule Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03bfe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="03bfe-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorManagedRuleObject -Priority <Int32> [-Version <String>]
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="03bfe-105">설명은</span><span class="sxs-lookup"><span data-stu-id="03bfe-105">DESCRIPTION</span></span>
<span data-ttu-id="03bfe-106">WAF 정책 만들기에 대 한 ManagedRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="03bfe-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="03bfe-107">예제의</span><span class="sxs-lookup"><span data-stu-id="03bfe-107">EXAMPLES</span></span>

### <span data-ttu-id="03bfe-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="03bfe-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoor
ManagedRuleObject -Priority 1 -Version 0 -RuleGroupOverride $override1

RuleGroupOverrides                                                   Priority Version
------------------                                                   -------- -------
{Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride}        1 0
```

<span data-ttu-id="03bfe-109">ManagedRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="03bfe-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="03bfe-110">변수</span><span class="sxs-lookup"><span data-stu-id="03bfe-110">PARAMETERS</span></span>

### <span data-ttu-id="03bfe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03bfe-111">-DefaultProfile</span></span>
<span data-ttu-id="03bfe-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="03bfe-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03bfe-113">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="03bfe-113">-Priority</span></span>
<span data-ttu-id="03bfe-114">규칙의 우선 순위에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="03bfe-114">Describes priority of the rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bfe-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="03bfe-115">-RuleGroupOverride</span></span>
<span data-ttu-id="03bfe-116">Azure 관리 공급자 재정의 구성 목록</span><span class="sxs-lookup"><span data-stu-id="03bfe-116">List of azure managed provider override configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bfe-117">-버전</span><span class="sxs-lookup"><span data-stu-id="03bfe-117">-Version</span></span>
<span data-ttu-id="03bfe-118">버전 규칙 집합</span><span class="sxs-lookup"><span data-stu-id="03bfe-118">Version of the ruleset</span></span>

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

### <span data-ttu-id="03bfe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03bfe-119">CommonParameters</span></span>
<span data-ttu-id="03bfe-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="03bfe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03bfe-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03bfe-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03bfe-122">입력</span><span class="sxs-lookup"><span data-stu-id="03bfe-122">INPUTS</span></span>

### <span data-ttu-id="03bfe-123">않아야</span><span class="sxs-lookup"><span data-stu-id="03bfe-123">None</span></span>

## <span data-ttu-id="03bfe-124">출력</span><span class="sxs-lookup"><span data-stu-id="03bfe-124">OUTPUTS</span></span>

### <span data-ttu-id="03bfe-125">FrontDoor를 통해 PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="03bfe-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="03bfe-126">상속자</span><span class="sxs-lookup"><span data-stu-id="03bfe-126">NOTES</span></span>

## <span data-ttu-id="03bfe-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03bfe-127">RELATED LINKS</span></span>

<span data-ttu-id="03bfe-128">[새로운 AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
 [새로운 AzureRmFrontDoorRuleGroupOverrideObject](./Set-AzureRmFrontDoorRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="03bfe-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorRuleGroupOverrideObject](./Set-AzureRmFrontDoorRuleGroupOverrideObject.md)</span></span>
