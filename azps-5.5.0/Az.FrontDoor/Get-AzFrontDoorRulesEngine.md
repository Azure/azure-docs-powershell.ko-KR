---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
ms.openlocfilehash: c0742344db01e40a01a0aeee3b61b93b92cc3f07
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209517"
---
# <span data-ttu-id="4a3c6-101">Get-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="4a3c6-101">Get-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="4a3c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a3c6-102">SYNOPSIS</span></span>
<span data-ttu-id="4a3c6-103">규칙 엔진 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-103">Get Rules Engine configurations.</span></span>

## <span data-ttu-id="4a3c6-104">구문</span><span class="sxs-lookup"><span data-stu-id="4a3c6-104">SYNTAX</span></span>

```
Get-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a3c6-105">설명</span><span class="sxs-lookup"><span data-stu-id="4a3c6-105">DESCRIPTION</span></span>
<span data-ttu-id="4a3c6-106">**Get-AzFrontDoorRulesEngine** cmdlet은 특정 규칙 엔진 구성을 얻거나 Front Door와 연결된 모든 규칙 엔진 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-106">The **Get-AzFrontDoorRulesEngine** cmdlet gets a specific rules engine configuration or gets all rules engine configurations associated with a Front Door.</span></span> 

## <span data-ttu-id="4a3c6-107">예제</span><span class="sxs-lookup"><span data-stu-id="4a3c6-107">EXAMPLES</span></span>

### <span data-ttu-id="4a3c6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4a3c6-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name rulesengine3

Name         RulesEngineRules
----         ----------------
rulesEngine3 {rules1}
```

<span data-ttu-id="4a3c6-109">특정 규칙 엔진 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-109">Get specific rules engine configuration.</span></span>

### <span data-ttu-id="4a3c6-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="4a3c6-110">Example 2</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName

Name         RulesEngineRules
----         ----------------
rulesEngine1 {Rule1}
rulesEngine2 {Rule1}
rulesEngine3 {rules1}
```

<span data-ttu-id="4a3c6-111">프런트 도어에서 모든 규칙 엔진 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-111">Get all rules engine configurations in a front door.</span></span>

### <span data-ttu-id="4a3c6-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="4a3c6-112">Example 3</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistent
Get-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistent' in Front Door 'frontDoorName' is not found.
At line:1 char:1
+ Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontD ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Get-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.GetFrontDoorRulesEngine
```

<span data-ttu-id="4a3c6-113">규칙 엔진이 없는 경우 예상되는 출력입니다.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-113">Expected output when getting a nonexistent rules engine.</span></span> 

## <span data-ttu-id="4a3c6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a3c6-114">PARAMETERS</span></span>

### <span data-ttu-id="4a3c6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a3c6-115">-DefaultProfile</span></span>
<span data-ttu-id="4a3c6-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a3c6-117">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="4a3c6-117">-FrontDoorName</span></span>
<span data-ttu-id="4a3c6-118">Front Door 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-118">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a3c6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4a3c6-119">-Name</span></span>
<span data-ttu-id="4a3c6-120">규칙 엔진 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-120">Rules engine name.</span></span>

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

### <span data-ttu-id="4a3c6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a3c6-121">-ResourceGroupName</span></span>
<span data-ttu-id="4a3c6-122">Front Door를 만들 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-122">The resource group name that the Front Door will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a3c6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a3c6-123">CommonParameters</span></span>
<span data-ttu-id="4a3c6-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a3c6-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4a3c6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a3c6-126">입력</span><span class="sxs-lookup"><span data-stu-id="4a3c6-126">INPUTS</span></span>

### <span data-ttu-id="4a3c6-127">없음</span><span class="sxs-lookup"><span data-stu-id="4a3c6-127">None</span></span>

## <span data-ttu-id="4a3c6-128">출력</span><span class="sxs-lookup"><span data-stu-id="4a3c6-128">OUTPUTS</span></span>

### <span data-ttu-id="4a3c6-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="4a3c6-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="4a3c6-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4a3c6-130">NOTES</span></span>

## <span data-ttu-id="4a3c6-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a3c6-131">RELATED LINKS</span></span>
