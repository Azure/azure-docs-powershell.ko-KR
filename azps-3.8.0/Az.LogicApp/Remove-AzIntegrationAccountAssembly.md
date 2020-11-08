---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 4dceb934f5cf746908c289c7662de0dc3dae09a5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034855"
---
# <span data-ttu-id="cd037-101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cd037-101">Remove-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="cd037-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd037-102">SYNOPSIS</span></span>
<span data-ttu-id="cd037-103">통합 계정 어셈블리를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd037-103">Removes an integration account assembly.</span></span>

## <span data-ttu-id="cd037-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cd037-104">SYNTAX</span></span>

### <span data-ttu-id="cd037-105">ByIntegrationAccount (기본값)</span><span class="sxs-lookup"><span data-stu-id="cd037-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd037-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cd037-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd037-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cd037-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd037-108">설명은</span><span class="sxs-lookup"><span data-stu-id="cd037-108">DESCRIPTION</span></span>
<span data-ttu-id="cd037-109">**AzIntegrationAccountAssembly** cmdlet은 통합 계정에서 어셈블리를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd037-109">The **Remove-AzIntegrationAccountAssembly** cmdlet removes an assembly from an integration account.</span></span>

## <span data-ttu-id="cd037-110">예제의</span><span class="sxs-lookup"><span data-stu-id="cd037-110">EXAMPLES</span></span>

### <span data-ttu-id="cd037-111">예제 1: 매개 변수로 어셈블리 제거</span><span class="sxs-lookup"><span data-stu-id="cd037-111">Example 1: Remove an assembly by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"
```

<span data-ttu-id="cd037-112">통합 계정 "sampleIntegrationAccount"에 있는 "sampleAssembly" 라는 어셈블리를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd037-112">Removes the assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="cd037-113">변수</span><span class="sxs-lookup"><span data-stu-id="cd037-113">PARAMETERS</span></span>

### <span data-ttu-id="cd037-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd037-114">-DefaultProfile</span></span>
<span data-ttu-id="cd037-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cd037-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd037-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd037-116">-InputObject</span></span>
<span data-ttu-id="cd037-117">통합 계정 어셈블리</span><span class="sxs-lookup"><span data-stu-id="cd037-117">An integration account assembly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd037-118">-이름</span><span class="sxs-lookup"><span data-stu-id="cd037-118">-Name</span></span>
<span data-ttu-id="cd037-119">통합 계정 어셈블리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd037-119">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd037-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="cd037-120">-ParentName</span></span>
<span data-ttu-id="cd037-121">통합 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd037-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd037-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd037-122">-PassThru</span></span>
<span data-ttu-id="cd037-123">명령이 성공적으로 실행 되었는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd037-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="cd037-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd037-124">-ResourceGroupName</span></span>
<span data-ttu-id="cd037-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd037-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd037-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd037-126">-ResourceId</span></span>
<span data-ttu-id="cd037-127">통합 계정 어셈블리 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="cd037-127">The integration account assembly resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd037-128">-확인</span><span class="sxs-lookup"><span data-stu-id="cd037-128">-Confirm</span></span>
<span data-ttu-id="cd037-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd037-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd037-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd037-130">-WhatIf</span></span>
<span data-ttu-id="cd037-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cd037-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd037-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd037-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd037-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd037-133">CommonParameters</span></span>
<span data-ttu-id="cd037-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd037-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd037-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd037-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd037-136">입력</span><span class="sxs-lookup"><span data-stu-id="cd037-136">INPUTS</span></span>

### <span data-ttu-id="cd037-137">LogicApp. PSIntegrationAccountAssembly/.</span><span class="sxs-lookup"><span data-stu-id="cd037-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="cd037-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cd037-138">System.String</span></span>

## <span data-ttu-id="cd037-139">출력</span><span class="sxs-lookup"><span data-stu-id="cd037-139">OUTPUTS</span></span>

### <span data-ttu-id="cd037-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="cd037-140">System.Boolean</span></span>

## <span data-ttu-id="cd037-141">상속자</span><span class="sxs-lookup"><span data-stu-id="cd037-141">NOTES</span></span>

## <span data-ttu-id="cd037-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd037-142">RELATED LINKS</span></span>
