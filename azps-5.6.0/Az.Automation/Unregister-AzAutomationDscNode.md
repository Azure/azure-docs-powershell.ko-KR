---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: https://docs.microsoft.com/powershell/module/az.automation/unregister-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
ms.openlocfilehash: 5c8d58024f14e2dbd1be929ddb6f156b479d2487
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990495"
---
# <span data-ttu-id="0f2a5-101">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0f2a5-101">Unregister-AzAutomationDscNode</span></span>

## <span data-ttu-id="0f2a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f2a5-102">SYNOPSIS</span></span>
<span data-ttu-id="0f2a5-103">Automation 계정으로 관리에서 DSC 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0f2a5-103">Removes a DSC node from management by an Automation account.</span></span>

## <span data-ttu-id="0f2a5-104">구문</span><span class="sxs-lookup"><span data-stu-id="0f2a5-104">SYNTAX</span></span>

```
Unregister-AzAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0f2a5-105">설명</span><span class="sxs-lookup"><span data-stu-id="0f2a5-105">DESCRIPTION</span></span>
<span data-ttu-id="0f2a5-106">**Unregister-AzAutomationDscNode** cmdlet은 Azure Automation 계정의 관리에서 APS 원하는 상태 구성(DSC) 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0f2a5-106">The **Unregister-AzAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="0f2a5-107">예제</span><span class="sxs-lookup"><span data-stu-id="0f2a5-107">EXAMPLES</span></span>

### <span data-ttu-id="0f2a5-108">예제 1: Automation 계정으로 관리에서 Azure DSC 노드 제거</span><span class="sxs-lookup"><span data-stu-id="0f2a5-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="0f2a5-109">이 명령은 Contoso17이라는 Automation 계정의 관리에서 지정된 GUID가 있는 DSC 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0f2a5-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="0f2a5-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0f2a5-110">PARAMETERS</span></span>

### <span data-ttu-id="0f2a5-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0f2a5-111">-AutomationAccountName</span></span>
<span data-ttu-id="0f2a5-112">이 cmdlet에서 DSC 노드를 제거하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f2a5-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="0f2a5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f2a5-113">-DefaultProfile</span></span>
<span data-ttu-id="0f2a5-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0f2a5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f2a5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0f2a5-115">-Force</span></span>
<span data-ttu-id="0f2a5-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="0f2a5-116">ps_force</span></span>

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

### <span data-ttu-id="0f2a5-117">-Id</span><span class="sxs-lookup"><span data-stu-id="0f2a5-117">-Id</span></span>
<span data-ttu-id="0f2a5-118">이 cmdlet이 제거한 DSC 노드의 고유 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f2a5-118">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0f2a5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f2a5-119">-ResourceGroupName</span></span>
<span data-ttu-id="0f2a5-120">이 cmdlet에서 DSC 노드 등록을 등록하지 않은 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f2a5-120">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="0f2a5-121">-확인</span><span class="sxs-lookup"><span data-stu-id="0f2a5-121">-Confirm</span></span>
<span data-ttu-id="0f2a5-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f2a5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f2a5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f2a5-123">-WhatIf</span></span>
<span data-ttu-id="0f2a5-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0f2a5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f2a5-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0f2a5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f2a5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f2a5-126">CommonParameters</span></span>
<span data-ttu-id="0f2a5-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0f2a5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f2a5-128">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0f2a5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f2a5-129">입력</span><span class="sxs-lookup"><span data-stu-id="0f2a5-129">INPUTS</span></span>

### <span data-ttu-id="0f2a5-130">System.Guid</span><span class="sxs-lookup"><span data-stu-id="0f2a5-130">System.Guid</span></span>

### <span data-ttu-id="0f2a5-131">System.String</span><span class="sxs-lookup"><span data-stu-id="0f2a5-131">System.String</span></span>

## <span data-ttu-id="0f2a5-132">출력</span><span class="sxs-lookup"><span data-stu-id="0f2a5-132">OUTPUTS</span></span>

### <span data-ttu-id="0f2a5-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="0f2a5-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="0f2a5-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0f2a5-134">NOTES</span></span>

## <span data-ttu-id="0f2a5-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f2a5-135">RELATED LINKS</span></span>

[<span data-ttu-id="0f2a5-136">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0f2a5-136">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="0f2a5-137">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0f2a5-137">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="0f2a5-138">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0f2a5-138">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)


