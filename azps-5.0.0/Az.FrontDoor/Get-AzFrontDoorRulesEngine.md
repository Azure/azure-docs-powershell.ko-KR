---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
ms.openlocfilehash: c0742344db01e40a01a0aeee3b61b93b92cc3f07
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219057"
---
# <span data-ttu-id="97a12-101">Get-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="97a12-101">Get-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="97a12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97a12-102">SYNOPSIS</span></span>
<span data-ttu-id="97a12-103">규칙 엔진 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="97a12-103">Get Rules Engine configurations.</span></span>

## <span data-ttu-id="97a12-104">구문과</span><span class="sxs-lookup"><span data-stu-id="97a12-104">SYNTAX</span></span>

```
Get-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97a12-105">설명은</span><span class="sxs-lookup"><span data-stu-id="97a12-105">DESCRIPTION</span></span>
<span data-ttu-id="97a12-106">**AzFrontDoorRulesEngine** cmdlet은 특정 규칙 엔진 구성을 가져오거나, 앞 문과 연결 된 모든 규칙 엔진 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="97a12-106">The **Get-AzFrontDoorRulesEngine** cmdlet gets a specific rules engine configuration or gets all rules engine configurations associated with a Front Door.</span></span> 

## <span data-ttu-id="97a12-107">예제의</span><span class="sxs-lookup"><span data-stu-id="97a12-107">EXAMPLES</span></span>

### <span data-ttu-id="97a12-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="97a12-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name rulesengine3

Name         RulesEngineRules
----         ----------------
rulesEngine3 {rules1}
```

<span data-ttu-id="97a12-109">특정 규칙 엔진 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="97a12-109">Get specific rules engine configuration.</span></span>

### <span data-ttu-id="97a12-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="97a12-110">Example 2</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName

Name         RulesEngineRules
----         ----------------
rulesEngine1 {Rule1}
rulesEngine2 {Rule1}
rulesEngine3 {rules1}
```

<span data-ttu-id="97a12-111">앞 도어의 모든 규칙 엔진 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="97a12-111">Get all rules engine configurations in a front door.</span></span>

### <span data-ttu-id="97a12-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="97a12-112">Example 3</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistent
Get-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistent' in Front Door 'frontDoorName' is not found.
At line:1 char:1
+ Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontD ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Get-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.GetFrontDoorRulesEngine
```

<span data-ttu-id="97a12-113">존재 하지 않는 규칙 엔진을 가져올 때 출력이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="97a12-113">Expected output when getting a nonexistent rules engine.</span></span> 

## <span data-ttu-id="97a12-114">변수</span><span class="sxs-lookup"><span data-stu-id="97a12-114">PARAMETERS</span></span>

### <span data-ttu-id="97a12-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97a12-115">-DefaultProfile</span></span>
<span data-ttu-id="97a12-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="97a12-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97a12-117">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="97a12-117">-FrontDoorName</span></span>
<span data-ttu-id="97a12-118">전방 문 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97a12-118">Front Door name.</span></span>

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

### <span data-ttu-id="97a12-119">-이름</span><span class="sxs-lookup"><span data-stu-id="97a12-119">-Name</span></span>
<span data-ttu-id="97a12-120">규칙 엔진 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97a12-120">Rules engine name.</span></span>

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

### <span data-ttu-id="97a12-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97a12-121">-ResourceGroupName</span></span>
<span data-ttu-id="97a12-122">앞 문이 생성 될 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97a12-122">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="97a12-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a12-123">CommonParameters</span></span>
<span data-ttu-id="97a12-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="97a12-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a12-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="97a12-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a12-126">입력</span><span class="sxs-lookup"><span data-stu-id="97a12-126">INPUTS</span></span>

### <span data-ttu-id="97a12-127">않아야</span><span class="sxs-lookup"><span data-stu-id="97a12-127">None</span></span>

## <span data-ttu-id="97a12-128">출력</span><span class="sxs-lookup"><span data-stu-id="97a12-128">OUTPUTS</span></span>

### <span data-ttu-id="97a12-129">FrontDoor. a m/. Ps규칙 엔진</span><span class="sxs-lookup"><span data-stu-id="97a12-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="97a12-130">상속자</span><span class="sxs-lookup"><span data-stu-id="97a12-130">NOTES</span></span>

## <span data-ttu-id="97a12-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="97a12-131">RELATED LINKS</span></span>
