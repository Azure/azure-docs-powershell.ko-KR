---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 60023C8D-EA37-41DA-97E6-AF89F7F9BADD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationDscNode.md
ms.openlocfilehash: 02a6d7a129dc084b982f1827d678354265ddbc66
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182140"
---
# <span data-ttu-id="f08e0-101">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="f08e0-101">Set-AzAutomationDscNode</span></span>

## <span data-ttu-id="f08e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f08e0-102">SYNOPSIS</span></span>
<span data-ttu-id="f08e0-103">DSC 노드가 매핑되는 노드 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="f08e0-103">Modifies the node configuration that a DSC node is mapped to.</span></span>

## <span data-ttu-id="f08e0-104">구문</span><span class="sxs-lookup"><span data-stu-id="f08e0-104">SYNTAX</span></span>

```
Set-AzAutomationDscNode -Id <Guid> -NodeConfigurationName <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f08e0-105">설명</span><span class="sxs-lookup"><span data-stu-id="f08e0-105">DESCRIPTION</span></span>
<span data-ttu-id="f08e0-106">**Set-AzAutomationDscNode** cmdlet은 APS DSC(필요한 상태 구성) 노드 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="f08e0-106">The **Set-AzAutomationDscNode** cmdlet modifies an APS Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="f08e0-107">Azure Automation은 DSC 노드 구성을 MOF(관리 개체 형식) 구성 문서로 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f08e0-107">Azure Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="f08e0-108">예제</span><span class="sxs-lookup"><span data-stu-id="f08e0-108">EXAMPLES</span></span>

### <span data-ttu-id="f08e0-109">예제 1: 노드 구성 매핑 수정</span><span class="sxs-lookup"><span data-stu-id="f08e0-109">Example 1: Modify node configuration mapping</span></span>
```
PS C:\>Set-AzAutomationDscNode -NodeConfigurationName "Contoso.NodeConfiguration01" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111c8a6067j8
```

<span data-ttu-id="f08e0-110">이 명령은 Contoso.NodeConfiguration01이라는 노드 구성을 지정된 GUID가 있는 노드에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="f08e0-110">This command assigns the node configuration named Contoso.NodeConfiguration01 to the node that has the specified GUID.</span></span>

## <span data-ttu-id="f08e0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f08e0-111">PARAMETERS</span></span>

### <span data-ttu-id="f08e0-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f08e0-112">-AutomationAccountName</span></span>
<span data-ttu-id="f08e0-113">이 cmdlet이 구성을 수정하는 DSC 노드를 포함하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f08e0-113">Specifies the name of the Automation account that contains the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="f08e0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f08e0-114">-DefaultProfile</span></span>
<span data-ttu-id="f08e0-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f08e0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f08e0-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f08e0-116">-Force</span></span>
<span data-ttu-id="f08e0-117">ps_force 확인을 요청하지 않고 실행할 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f08e0-117">ps_force the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f08e0-118">-Id</span><span class="sxs-lookup"><span data-stu-id="f08e0-118">-Id</span></span>
<span data-ttu-id="f08e0-119">이 cmdlet이 구성을 수정하는 DSC 노드의 고유 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f08e0-119">Specifies the unique ID of the DSC node for which this cmdlet modifies the configuration.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f08e0-120">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f08e0-120">-NodeConfigurationName</span></span>
<span data-ttu-id="f08e0-121">이 cmdlet이 노드를 매핑하는 노드 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f08e0-121">Specifies the name of the node configuration to which this cmdlet maps the node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f08e0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f08e0-122">-ResourceGroupName</span></span>
<span data-ttu-id="f08e0-123">이 cmdlet이 DSC 노드 구성을 수정하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f08e0-123">Specifies the name of a resource group in which this cmdlet modifies a DSC node configuration.</span></span>

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

### <span data-ttu-id="f08e0-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f08e0-124">-Confirm</span></span>
<span data-ttu-id="f08e0-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f08e0-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f08e0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f08e0-126">-WhatIf</span></span>
<span data-ttu-id="f08e0-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f08e0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f08e0-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f08e0-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f08e0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f08e0-129">CommonParameters</span></span>
<span data-ttu-id="f08e0-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f08e0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f08e0-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f08e0-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f08e0-132">입력</span><span class="sxs-lookup"><span data-stu-id="f08e0-132">INPUTS</span></span>

### <span data-ttu-id="f08e0-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="f08e0-133">System.Guid</span></span>

### <span data-ttu-id="f08e0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f08e0-134">System.String</span></span>

## <span data-ttu-id="f08e0-135">출력</span><span class="sxs-lookup"><span data-stu-id="f08e0-135">OUTPUTS</span></span>

### <span data-ttu-id="f08e0-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="f08e0-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="f08e0-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f08e0-137">NOTES</span></span>

## <span data-ttu-id="f08e0-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f08e0-138">RELATED LINKS</span></span>

[<span data-ttu-id="f08e0-139">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="f08e0-139">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="f08e0-140">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="f08e0-140">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="f08e0-141">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="f08e0-141">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


