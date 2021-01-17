---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 4dceb934f5cf746908c289c7662de0dc3dae09a5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490187"
---
# <span data-ttu-id="cbc6a-101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cbc6a-101">Remove-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="cbc6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbc6a-102">SYNOPSIS</span></span>
<span data-ttu-id="cbc6a-103">통합 계정 어셈블리를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-103">Removes an integration account assembly.</span></span>

## <span data-ttu-id="cbc6a-104">구문</span><span class="sxs-lookup"><span data-stu-id="cbc6a-104">SYNTAX</span></span>

### <span data-ttu-id="cbc6a-105">ByIntegrationAccount(기본값)</span><span class="sxs-lookup"><span data-stu-id="cbc6a-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbc6a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cbc6a-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbc6a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cbc6a-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbc6a-108">설명</span><span class="sxs-lookup"><span data-stu-id="cbc6a-108">DESCRIPTION</span></span>
<span data-ttu-id="cbc6a-109">**Remove-AzIntegrationAccountAssembly** cmdlet은 통합 계정에서 어셈블리를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-109">The **Remove-AzIntegrationAccountAssembly** cmdlet removes an assembly from an integration account.</span></span>

## <span data-ttu-id="cbc6a-110">예제</span><span class="sxs-lookup"><span data-stu-id="cbc6a-110">EXAMPLES</span></span>

### <span data-ttu-id="cbc6a-111">예제 1: 매개 변수로 어셈블리 제거</span><span class="sxs-lookup"><span data-stu-id="cbc6a-111">Example 1: Remove an assembly by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"
```

<span data-ttu-id="cbc6a-112">통합 계정 "sampleIntegrationAccount"에 있는 "sampleAssembly"라는 어셈블리를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-112">Removes the assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="cbc6a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbc6a-113">PARAMETERS</span></span>

### <span data-ttu-id="cbc6a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbc6a-114">-DefaultProfile</span></span>
<span data-ttu-id="cbc6a-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbc6a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbc6a-116">-InputObject</span></span>
<span data-ttu-id="cbc6a-117">통합 계정 어셈블리입니다.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-117">An integration account assembly.</span></span>

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

### <span data-ttu-id="cbc6a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="cbc6a-118">-Name</span></span>
<span data-ttu-id="cbc6a-119">통합 계정 어셈블리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-119">The integration account assembly name.</span></span>

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

### <span data-ttu-id="cbc6a-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="cbc6a-120">-ParentName</span></span>
<span data-ttu-id="cbc6a-121">통합 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-121">The integration account name.</span></span>

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

### <span data-ttu-id="cbc6a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cbc6a-122">-PassThru</span></span>
<span data-ttu-id="cbc6a-123">명령이 성공적이지 않은지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="cbc6a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbc6a-124">-ResourceGroupName</span></span>
<span data-ttu-id="cbc6a-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-125">The resource group name.</span></span>

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

### <span data-ttu-id="cbc6a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbc6a-126">-ResourceId</span></span>
<span data-ttu-id="cbc6a-127">통합 계정 어셈블리 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-127">The integration account assembly resource id.</span></span>

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

### <span data-ttu-id="cbc6a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cbc6a-128">-Confirm</span></span>
<span data-ttu-id="cbc6a-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbc6a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbc6a-130">-WhatIf</span></span>
<span data-ttu-id="cbc6a-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="cbc6a-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cbc6a-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbc6a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbc6a-133">CommonParameters</span></span>
<span data-ttu-id="cbc6a-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbc6a-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cbc6a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbc6a-136">입력</span><span class="sxs-lookup"><span data-stu-id="cbc6a-136">INPUTS</span></span>

### <span data-ttu-id="cbc6a-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cbc6a-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="cbc6a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="cbc6a-138">System.String</span></span>

## <span data-ttu-id="cbc6a-139">출력</span><span class="sxs-lookup"><span data-stu-id="cbc6a-139">OUTPUTS</span></span>

### <span data-ttu-id="cbc6a-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cbc6a-140">System.Boolean</span></span>

## <span data-ttu-id="cbc6a-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cbc6a-141">NOTES</span></span>

## <span data-ttu-id="cbc6a-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cbc6a-142">RELATED LINKS</span></span>
