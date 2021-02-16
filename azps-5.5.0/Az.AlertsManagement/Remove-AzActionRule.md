---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/remove-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
ms.openlocfilehash: 4462434bcda1045afcc8478bbd9c4b7a1718d478
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199785"
---
# <span data-ttu-id="99764-101">Remove-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="99764-101">Remove-AzActionRule</span></span>

## <span data-ttu-id="99764-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99764-102">SYNOPSIS</span></span>
<span data-ttu-id="99764-103">작업 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="99764-103">Deletes a action rule</span></span>

## <span data-ttu-id="99764-104">구문</span><span class="sxs-lookup"><span data-stu-id="99764-104">SYNTAX</span></span>

### <span data-ttu-id="99764-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="99764-105">ByName (Default)</span></span>
```
Remove-AzActionRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99764-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="99764-106">ByResourceId</span></span>
```
Remove-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99764-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="99764-107">ByInputObject</span></span>
```
Remove-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99764-108">설명</span><span class="sxs-lookup"><span data-stu-id="99764-108">DESCRIPTION</span></span>
<span data-ttu-id="99764-109">**Remove-AzActionRule** cmdlet은 작업 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="99764-109">**Remove-AzActionRule** cmdlet deletes a action rule.</span></span>

## <span data-ttu-id="99764-110">예제</span><span class="sxs-lookup"><span data-stu-id="99764-110">EXAMPLES</span></span>

### <span data-ttu-id="99764-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="99764-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzActionRule -ResourceGroupName "test-rg" -Name "ActionRuleName"
```

<span data-ttu-id="99764-112">이 cmdlet은 리소스 그룹 test-rg에서 ActionRuleName 이름이 있는 작업 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="99764-112">This cmdlet deletes the action rule with name ActionRuleName in resource group test-rg</span></span>

## <span data-ttu-id="99764-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99764-113">PARAMETERS</span></span>

### <span data-ttu-id="99764-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99764-114">-DefaultProfile</span></span>
<span data-ttu-id="99764-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="99764-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99764-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99764-116">-InputObject</span></span>
<span data-ttu-id="99764-117">작업 규칙 리소스</span><span class="sxs-lookup"><span data-stu-id="99764-117">The action rule resource</span></span>

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

### <span data-ttu-id="99764-118">-Name</span><span class="sxs-lookup"><span data-stu-id="99764-118">-Name</span></span>
<span data-ttu-id="99764-119">작업 규칙의 이름</span><span class="sxs-lookup"><span data-stu-id="99764-119">Name of action rule</span></span>

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

### <span data-ttu-id="99764-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99764-120">-PassThru</span></span>
<span data-ttu-id="99764-121">PassThru는 작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="99764-121">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="99764-122">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99764-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="99764-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99764-123">-ResourceGroupName</span></span>
<span data-ttu-id="99764-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="99764-124">Resource Group name</span></span>

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

### <span data-ttu-id="99764-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99764-125">-ResourceId</span></span>
<span data-ttu-id="99764-126">리소스 ID로 작업 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="99764-126">Get Action rule by resource id.</span></span>

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

### <span data-ttu-id="99764-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99764-127">-Confirm</span></span>
<span data-ttu-id="99764-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="99764-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99764-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99764-129">-WhatIf</span></span>
<span data-ttu-id="99764-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="99764-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99764-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99764-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99764-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99764-132">CommonParameters</span></span>
<span data-ttu-id="99764-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="99764-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99764-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="99764-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99764-135">입력</span><span class="sxs-lookup"><span data-stu-id="99764-135">INPUTS</span></span>

### <span data-ttu-id="99764-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="99764-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="99764-137">출력</span><span class="sxs-lookup"><span data-stu-id="99764-137">OUTPUTS</span></span>

### <span data-ttu-id="99764-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="99764-138">System.Boolean</span></span>

## <span data-ttu-id="99764-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="99764-139">NOTES</span></span>

## <span data-ttu-id="99764-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99764-140">RELATED LINKS</span></span>