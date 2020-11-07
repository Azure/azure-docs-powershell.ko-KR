---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
ms.openlocfilehash: fc4696a26c10ace497c6ff64a7ac4c1ac49279c7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701480"
---
# <span data-ttu-id="9f65a-101">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="9f65a-101">Unregister-AzAutomationDscNode</span></span>

## <span data-ttu-id="9f65a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f65a-102">SYNOPSIS</span></span>
<span data-ttu-id="9f65a-103">자동화 계정으로 관리에서 DSC 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f65a-103">Removes a DSC node from management by an Automation account.</span></span>

## <span data-ttu-id="9f65a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9f65a-104">SYNTAX</span></span>

```
Unregister-AzAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9f65a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9f65a-105">DESCRIPTION</span></span>
<span data-ttu-id="9f65a-106">**AzAutomationDscNode** Cmdlet은 Azure Automation 계정에의 한 관리에서 Ap (원하는 상태 구성) 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f65a-106">The **Unregister-AzAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="9f65a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9f65a-107">EXAMPLES</span></span>

### <span data-ttu-id="9f65a-108">예제 1: Automation 계정 관리에서 Azure DSC 노드 제거</span><span class="sxs-lookup"><span data-stu-id="9f65a-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="9f65a-109">이 명령은 Contoso17 이라는 자동화 계정으로 지정 된 GUID가 있는 DSC 노드를 관리에서 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f65a-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="9f65a-110">변수</span><span class="sxs-lookup"><span data-stu-id="9f65a-110">PARAMETERS</span></span>

### <span data-ttu-id="9f65a-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9f65a-111">-AutomationAccountName</span></span>
<span data-ttu-id="9f65a-112">이 cmdlet이 DSC 노드를 제거 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f65a-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="9f65a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f65a-113">-DefaultProfile</span></span>
<span data-ttu-id="9f65a-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9f65a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f65a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9f65a-115">-Force</span></span>
<span data-ttu-id="9f65a-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="9f65a-116">ps_force</span></span>

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

### <span data-ttu-id="9f65a-117">-Id</span><span class="sxs-lookup"><span data-stu-id="9f65a-117">-Id</span></span>
<span data-ttu-id="9f65a-118">이 cmdlet이 제거 하는 DSC 노드의 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f65a-118">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9f65a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f65a-119">-ResourceGroupName</span></span>
<span data-ttu-id="9f65a-120">이 cmdlet이 DSC 노드의 등록을 취소 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f65a-120">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="9f65a-121">-확인</span><span class="sxs-lookup"><span data-stu-id="9f65a-121">-Confirm</span></span>
<span data-ttu-id="9f65a-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f65a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f65a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f65a-123">-WhatIf</span></span>
<span data-ttu-id="9f65a-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9f65a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f65a-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9f65a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f65a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f65a-126">CommonParameters</span></span>
<span data-ttu-id="9f65a-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f65a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f65a-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f65a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f65a-129">입력</span><span class="sxs-lookup"><span data-stu-id="9f65a-129">INPUTS</span></span>

### <span data-ttu-id="9f65a-130">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="9f65a-130">System.Guid</span></span>

### <span data-ttu-id="9f65a-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9f65a-131">System.String</span></span>

## <span data-ttu-id="9f65a-132">출력</span><span class="sxs-lookup"><span data-stu-id="9f65a-132">OUTPUTS</span></span>

### <span data-ttu-id="9f65a-133">Microsoft Azure.-DscNode</span><span class="sxs-lookup"><span data-stu-id="9f65a-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="9f65a-134">상속자</span><span class="sxs-lookup"><span data-stu-id="9f65a-134">NOTES</span></span>

## <span data-ttu-id="9f65a-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9f65a-135">RELATED LINKS</span></span>

[<span data-ttu-id="9f65a-136">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="9f65a-136">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="9f65a-137">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="9f65a-137">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="9f65a-138">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="9f65a-138">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)


