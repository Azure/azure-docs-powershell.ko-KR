---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/powershell/module/az.automation/publish-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
ms.openlocfilehash: fa10c44186de06de758e4f7878bb7c8da61c4d6c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004800"
---
# <span data-ttu-id="0f72f-101">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0f72f-101">Publish-AzAutomationRunbook</span></span>

## <span data-ttu-id="0f72f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f72f-102">SYNOPSIS</span></span>
<span data-ttu-id="0f72f-103">Runbook을 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="0f72f-103">Publishes a runbook.</span></span>

## <span data-ttu-id="0f72f-104">구문</span><span class="sxs-lookup"><span data-stu-id="0f72f-104">SYNTAX</span></span>

```
Publish-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f72f-105">설명</span><span class="sxs-lookup"><span data-stu-id="0f72f-105">DESCRIPTION</span></span>
<span data-ttu-id="0f72f-106">**Publish-AzAutomationRunbook** cmdlet은 Azure Automation의 프로덕션 환경에서 사용할 Runbook을 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="0f72f-106">The **Publish-AzAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="0f72f-107">예제</span><span class="sxs-lookup"><span data-stu-id="0f72f-107">EXAMPLES</span></span>

### <span data-ttu-id="0f72f-108">예제 1: Runbook 게시</span><span class="sxs-lookup"><span data-stu-id="0f72f-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0f72f-109">이 명령은 Contoso17이라는 Azure Automation 계정에 Runbk01이라는 Runbook을 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="0f72f-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="0f72f-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0f72f-110">PARAMETERS</span></span>

### <span data-ttu-id="0f72f-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0f72f-111">-AutomationAccountName</span></span>
<span data-ttu-id="0f72f-112">이 cmdlet에서 Runbook을 게시하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f72f-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="0f72f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f72f-113">-DefaultProfile</span></span>
<span data-ttu-id="0f72f-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0f72f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f72f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0f72f-115">-Name</span></span>
<span data-ttu-id="0f72f-116">이 cmdlet이 게시하는 Runbook의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f72f-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="0f72f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f72f-117">-ResourceGroupName</span></span>
<span data-ttu-id="0f72f-118">이 cmdlet에서 Runbook을 게시하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f72f-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="0f72f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f72f-119">CommonParameters</span></span>
<span data-ttu-id="0f72f-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0f72f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f72f-121">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0f72f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f72f-122">입력</span><span class="sxs-lookup"><span data-stu-id="0f72f-122">INPUTS</span></span>

### <span data-ttu-id="0f72f-123">System.String</span><span class="sxs-lookup"><span data-stu-id="0f72f-123">System.String</span></span>

## <span data-ttu-id="0f72f-124">출력</span><span class="sxs-lookup"><span data-stu-id="0f72f-124">OUTPUTS</span></span>

### <span data-ttu-id="0f72f-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="0f72f-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="0f72f-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0f72f-126">NOTES</span></span>

## <span data-ttu-id="0f72f-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f72f-127">RELATED LINKS</span></span>

[<span data-ttu-id="0f72f-128">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0f72f-128">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="0f72f-129">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0f72f-129">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="0f72f-130">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0f72f-130">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="0f72f-131">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0f72f-131">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="0f72f-132">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0f72f-132">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="0f72f-133">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0f72f-133">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="0f72f-134">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0f72f-134">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="0f72f-135">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0f72f-135">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


