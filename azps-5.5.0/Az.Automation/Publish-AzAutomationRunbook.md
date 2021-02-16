---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/publish-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
ms.openlocfilehash: feca8adfbfe24ce006c2fc5f52618f43591fa0b4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177972"
---
# <span data-ttu-id="29747-101">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="29747-101">Publish-AzAutomationRunbook</span></span>

## <span data-ttu-id="29747-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29747-102">SYNOPSIS</span></span>
<span data-ttu-id="29747-103">Runbook을 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="29747-103">Publishes a runbook.</span></span>

## <span data-ttu-id="29747-104">구문</span><span class="sxs-lookup"><span data-stu-id="29747-104">SYNTAX</span></span>

```
Publish-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29747-105">설명</span><span class="sxs-lookup"><span data-stu-id="29747-105">DESCRIPTION</span></span>
<span data-ttu-id="29747-106">**Publish-AzAutomationRunbook** cmdlet은 Azure Automation의 프로덕션 환경에서 사용할 Runbook을 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="29747-106">The **Publish-AzAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="29747-107">예제</span><span class="sxs-lookup"><span data-stu-id="29747-107">EXAMPLES</span></span>

### <span data-ttu-id="29747-108">예제 1: Runbook 게시</span><span class="sxs-lookup"><span data-stu-id="29747-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="29747-109">이 명령은 Contoso17이라는 Azure Automation 계정에 Runbk01이라는 Runbook을 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="29747-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="29747-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29747-110">PARAMETERS</span></span>

### <span data-ttu-id="29747-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="29747-111">-AutomationAccountName</span></span>
<span data-ttu-id="29747-112">이 cmdlet이 Runbook을 게시하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29747-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="29747-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29747-113">-DefaultProfile</span></span>
<span data-ttu-id="29747-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="29747-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29747-115">-Name</span><span class="sxs-lookup"><span data-stu-id="29747-115">-Name</span></span>
<span data-ttu-id="29747-116">이 cmdlet이 게시하는 Runbook의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29747-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29747-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29747-117">-ResourceGroupName</span></span>
<span data-ttu-id="29747-118">이 cmdlet이 Runbook을 게시하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29747-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="29747-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29747-119">CommonParameters</span></span>
<span data-ttu-id="29747-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="29747-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29747-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="29747-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29747-122">입력</span><span class="sxs-lookup"><span data-stu-id="29747-122">INPUTS</span></span>

### <span data-ttu-id="29747-123">System.String</span><span class="sxs-lookup"><span data-stu-id="29747-123">System.String</span></span>

## <span data-ttu-id="29747-124">출력</span><span class="sxs-lookup"><span data-stu-id="29747-124">OUTPUTS</span></span>

### <span data-ttu-id="29747-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="29747-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="29747-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="29747-126">NOTES</span></span>

## <span data-ttu-id="29747-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29747-127">RELATED LINKS</span></span>

[<span data-ttu-id="29747-128">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="29747-128">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="29747-129">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="29747-129">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="29747-130">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="29747-130">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="29747-131">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="29747-131">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="29747-132">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="29747-132">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="29747-133">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="29747-133">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="29747-134">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="29747-134">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="29747-135">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="29747-135">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


