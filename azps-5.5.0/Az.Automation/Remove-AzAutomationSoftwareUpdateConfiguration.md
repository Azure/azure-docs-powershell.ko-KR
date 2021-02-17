---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: bd5e51b8951d2b246036b45ddddf3d1bbe4b8e4e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205448"
---
# <span data-ttu-id="da091-101">Remove-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="da091-101">Remove-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="da091-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da091-102">SYNOPSIS</span></span>
<span data-ttu-id="da091-103">Azure Automation 소프트웨어 업데이트 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="da091-103">Removes an azure automation software update configuration.</span></span>

## <span data-ttu-id="da091-104">구문</span><span class="sxs-lookup"><span data-stu-id="da091-104">SYNTAX</span></span>

### <span data-ttu-id="da091-105">BySucName(기본값)</span><span class="sxs-lookup"><span data-stu-id="da091-105">BySucName (Default)</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da091-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="da091-106">BySuc</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da091-107">설명</span><span class="sxs-lookup"><span data-stu-id="da091-107">DESCRIPTION</span></span>
<span data-ttu-id="da091-108">이 cmdlet은 Azure Automation 소프트웨어 업데이트 구성을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="da091-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="da091-109">예제</span><span class="sxs-lookup"><span data-stu-id="da091-109">EXAMPLES</span></span>

### <span data-ttu-id="da091-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="da091-110">Example 1</span></span>
<span data-ttu-id="da091-111">이 예제에서는 자동화 계정에서 'MyUpdateConfiguration'을 제거하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="da091-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="da091-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da091-112">PARAMETERS</span></span>

### <span data-ttu-id="da091-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="da091-113">-AutomationAccountName</span></span>
<span data-ttu-id="da091-114">자동화 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da091-114">The automation account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da091-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da091-115">-DefaultProfile</span></span>
<span data-ttu-id="da091-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="da091-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da091-117">-Name</span><span class="sxs-lookup"><span data-stu-id="da091-117">-Name</span></span>
<span data-ttu-id="da091-118">제거할 소프트웨어 업데이트 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da091-118">Name of the software update configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: BySucName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da091-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da091-119">-PassThru</span></span>
<span data-ttu-id="da091-120">PassThru는 작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="da091-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="da091-121">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da091-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="da091-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da091-122">-ResourceGroupName</span></span>
<span data-ttu-id="da091-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da091-123">The resource group name.</span></span>

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

### <span data-ttu-id="da091-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="da091-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="da091-125">제거할 소프트웨어 업데이트 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="da091-125">The software update configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration
Parameter Sets: BySuc
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da091-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da091-126">-Confirm</span></span>
<span data-ttu-id="da091-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="da091-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da091-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da091-128">-WhatIf</span></span>
<span data-ttu-id="da091-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="da091-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da091-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da091-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da091-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da091-131">CommonParameters</span></span>
<span data-ttu-id="da091-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="da091-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da091-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="da091-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da091-134">입력</span><span class="sxs-lookup"><span data-stu-id="da091-134">INPUTS</span></span>

### <span data-ttu-id="da091-135">System.String</span><span class="sxs-lookup"><span data-stu-id="da091-135">System.String</span></span>

### <span data-ttu-id="da091-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="da091-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="da091-137">출력</span><span class="sxs-lookup"><span data-stu-id="da091-137">OUTPUTS</span></span>

### <span data-ttu-id="da091-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="da091-138">System.Void</span></span>

### <span data-ttu-id="da091-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="da091-139">System.Boolean</span></span>

## <span data-ttu-id="da091-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="da091-140">NOTES</span></span>

## <span data-ttu-id="da091-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da091-141">RELATED LINKS</span></span>
