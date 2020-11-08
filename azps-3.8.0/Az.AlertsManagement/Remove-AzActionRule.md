---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/remove-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
ms.openlocfilehash: 1cdea9a2d5deb9fbe93da0a090070f7ed1b07653
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034659"
---
# <span data-ttu-id="b6cf7-101">Remove-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="b6cf7-101">Remove-AzActionRule</span></span>

## <span data-ttu-id="b6cf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6cf7-102">SYNOPSIS</span></span>
<span data-ttu-id="b6cf7-103">작업 규칙을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cf7-103">Deletes a action rule</span></span>

## <span data-ttu-id="b6cf7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b6cf7-104">SYNTAX</span></span>

### <span data-ttu-id="b6cf7-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="b6cf7-105">ByName (Default)</span></span>
```
Remove-AzActionRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6cf7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b6cf7-106">ByResourceId</span></span>
```
Remove-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6cf7-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b6cf7-107">ByInputObject</span></span>
```
Remove-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6cf7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b6cf7-108">DESCRIPTION</span></span>
<span data-ttu-id="b6cf7-109">**AzActionRule** cmdlet은 작업 규칙을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cf7-109">**Remove-AzActionRule** cmdlet deletes a action rule.</span></span>

## <span data-ttu-id="b6cf7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b6cf7-110">EXAMPLES</span></span>

### <span data-ttu-id="b6cf7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b6cf7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzActionRule -ResourceGroupName "test-rg" -Name "ActionRuleName"
```

<span data-ttu-id="b6cf7-112">이 cmdlet은 리소스 그룹 테스트에서 이름이 ActionRuleName 인 작업 규칙을 삭제 합니다-rg</span><span class="sxs-lookup"><span data-stu-id="b6cf7-112">This cmdlet deletes the action rule with name ActionRuleName in resource group test-rg</span></span>

## <span data-ttu-id="b6cf7-113">변수</span><span class="sxs-lookup"><span data-stu-id="b6cf7-113">PARAMETERS</span></span>

### <span data-ttu-id="b6cf7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6cf7-114">-DefaultProfile</span></span>
<span data-ttu-id="b6cf7-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b6cf7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6cf7-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6cf7-116">-InputObject</span></span>
<span data-ttu-id="b6cf7-117">작업 규칙 리소스</span><span class="sxs-lookup"><span data-stu-id="b6cf7-117">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cf7-118">-이름</span><span class="sxs-lookup"><span data-stu-id="b6cf7-118">-Name</span></span>
<span data-ttu-id="b6cf7-119">작업 규칙 이름</span><span class="sxs-lookup"><span data-stu-id="b6cf7-119">Name of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cf7-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6cf7-120">-PassThru</span></span>
<span data-ttu-id="b6cf7-121">PassThru 작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cf7-121">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="b6cf7-122">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6cf7-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cf7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6cf7-123">-ResourceGroupName</span></span>
<span data-ttu-id="b6cf7-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b6cf7-124">Resource Group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cf7-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6cf7-125">-ResourceId</span></span>
<span data-ttu-id="b6cf7-126">Resoure id를 기준으로 작업 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b6cf7-126">Get Action rule by resoure id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cf7-127">-확인</span><span class="sxs-lookup"><span data-stu-id="b6cf7-127">-Confirm</span></span>
<span data-ttu-id="b6cf7-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cf7-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cf7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6cf7-129">-WhatIf</span></span>
<span data-ttu-id="b6cf7-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b6cf7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6cf7-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6cf7-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cf7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6cf7-132">CommonParameters</span></span>
<span data-ttu-id="b6cf7-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cf7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6cf7-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b6cf7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6cf7-135">입력</span><span class="sxs-lookup"><span data-stu-id="b6cf7-135">INPUTS</span></span>

### <span data-ttu-id="b6cf7-136">AlertsManagement 모델. a PSActionRule</span><span class="sxs-lookup"><span data-stu-id="b6cf7-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="b6cf7-137">출력</span><span class="sxs-lookup"><span data-stu-id="b6cf7-137">OUTPUTS</span></span>

### <span data-ttu-id="b6cf7-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="b6cf7-138">System.Boolean</span></span>

## <span data-ttu-id="b6cf7-139">상속자</span><span class="sxs-lookup"><span data-stu-id="b6cf7-139">NOTES</span></span>

## <span data-ttu-id="b6cf7-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6cf7-140">RELATED LINKS</span></span>
