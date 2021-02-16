---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
ms.openlocfilehash: edae476893de5a64e950902d2de7b31fe53b51ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199652"
---
# <span data-ttu-id="e7730-101">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e7730-101">Get-AzAutomationRunbook</span></span>

## <span data-ttu-id="e7730-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7730-102">SYNOPSIS</span></span>
<span data-ttu-id="e7730-103">Runbook을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e7730-103">Gets a runbook.</span></span>

## <span data-ttu-id="e7730-104">구문</span><span class="sxs-lookup"><span data-stu-id="e7730-104">SYNTAX</span></span>

### <span data-ttu-id="e7730-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="e7730-105">ByAll (Default)</span></span>
```
Get-AzAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7730-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="e7730-106">ByRunbookName</span></span>
```
Get-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7730-107">설명</span><span class="sxs-lookup"><span data-stu-id="e7730-107">DESCRIPTION</span></span>
<span data-ttu-id="e7730-108">**Get-AzAutomationRunbook** cmdlet은 Azure Automation Runbook을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e7730-108">The **Get-AzAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="e7730-109">특정 Runbook을 얻습니다. 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e7730-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="e7730-110">예제</span><span class="sxs-lookup"><span data-stu-id="e7730-110">EXAMPLES</span></span>

### <span data-ttu-id="e7730-111">예제 1: 모든 Runbook 다운로드</span><span class="sxs-lookup"><span data-stu-id="e7730-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e7730-112">이 명령은 Contoso17이라는 Azure Automation 계정의 모든 Runbook을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e7730-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="e7730-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7730-113">PARAMETERS</span></span>

### <span data-ttu-id="e7730-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e7730-114">-AutomationAccountName</span></span>
<span data-ttu-id="e7730-115">이 cmdlet이 Runbook을 얻을 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e7730-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="e7730-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7730-116">-DefaultProfile</span></span>
<span data-ttu-id="e7730-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e7730-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7730-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e7730-118">-Name</span></span>
<span data-ttu-id="e7730-119">이 cmdlet이 얻을 Runbook의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e7730-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7730-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7730-120">-ResourceGroupName</span></span>
<span data-ttu-id="e7730-121">이 cmdlet에서 Runbook을 얻을 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e7730-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="e7730-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7730-122">CommonParameters</span></span>
<span data-ttu-id="e7730-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e7730-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7730-124">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e7730-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7730-125">입력</span><span class="sxs-lookup"><span data-stu-id="e7730-125">INPUTS</span></span>

### <span data-ttu-id="e7730-126">System.String</span><span class="sxs-lookup"><span data-stu-id="e7730-126">System.String</span></span>

## <span data-ttu-id="e7730-127">출력</span><span class="sxs-lookup"><span data-stu-id="e7730-127">OUTPUTS</span></span>

### <span data-ttu-id="e7730-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="e7730-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="e7730-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e7730-129">NOTES</span></span>

## <span data-ttu-id="e7730-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7730-130">RELATED LINKS</span></span>

[<span data-ttu-id="e7730-131">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e7730-131">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="e7730-132">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e7730-132">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="e7730-133">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e7730-133">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="e7730-134">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e7730-134">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="e7730-135">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e7730-135">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="e7730-136">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e7730-136">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="e7730-137">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e7730-137">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="e7730-138">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e7730-138">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


