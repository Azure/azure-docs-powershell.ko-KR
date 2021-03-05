---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
ms.openlocfilehash: 00d6908e244a54fb2dbd501f0d944fc9cfdbdff4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014272"
---
# <span data-ttu-id="cf887-101">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cf887-101">Get-AzAutomationRunbook</span></span>

## <span data-ttu-id="cf887-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf887-102">SYNOPSIS</span></span>
<span data-ttu-id="cf887-103">Runbook을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cf887-103">Gets a runbook.</span></span>

## <span data-ttu-id="cf887-104">구문</span><span class="sxs-lookup"><span data-stu-id="cf887-104">SYNTAX</span></span>

### <span data-ttu-id="cf887-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="cf887-105">ByAll (Default)</span></span>
```
Get-AzAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf887-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="cf887-106">ByRunbookName</span></span>
```
Get-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf887-107">설명</span><span class="sxs-lookup"><span data-stu-id="cf887-107">DESCRIPTION</span></span>
<span data-ttu-id="cf887-108">**Get-AzAutomationRunbook** cmdlet은 Azure Automation Runbook을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cf887-108">The **Get-AzAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="cf887-109">특정 Runbook을 얻지 못하도록 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf887-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="cf887-110">예제</span><span class="sxs-lookup"><span data-stu-id="cf887-110">EXAMPLES</span></span>

### <span data-ttu-id="cf887-111">예제 1: 모든 Runbook 다운로드</span><span class="sxs-lookup"><span data-stu-id="cf887-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="cf887-112">이 명령은 Contoso17이라는 Azure Automation 계정의 모든 Runbook을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cf887-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="cf887-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cf887-113">PARAMETERS</span></span>

### <span data-ttu-id="cf887-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cf887-114">-AutomationAccountName</span></span>
<span data-ttu-id="cf887-115">이 cmdlet에서 Runbook을 얻을 수 있는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf887-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="cf887-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf887-116">-DefaultProfile</span></span>
<span data-ttu-id="cf887-117">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="cf887-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf887-118">-Name</span><span class="sxs-lookup"><span data-stu-id="cf887-118">-Name</span></span>
<span data-ttu-id="cf887-119">이 cmdlet이 얻을 Runbook의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf887-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="cf887-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf887-120">-ResourceGroupName</span></span>
<span data-ttu-id="cf887-121">이 cmdlet에서 Runbook을 얻을 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf887-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="cf887-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf887-122">CommonParameters</span></span>
<span data-ttu-id="cf887-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cf887-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf887-124">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cf887-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf887-125">입력</span><span class="sxs-lookup"><span data-stu-id="cf887-125">INPUTS</span></span>

### <span data-ttu-id="cf887-126">System.String</span><span class="sxs-lookup"><span data-stu-id="cf887-126">System.String</span></span>

## <span data-ttu-id="cf887-127">출력</span><span class="sxs-lookup"><span data-stu-id="cf887-127">OUTPUTS</span></span>

### <span data-ttu-id="cf887-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="cf887-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="cf887-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cf887-129">NOTES</span></span>

## <span data-ttu-id="cf887-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cf887-130">RELATED LINKS</span></span>

[<span data-ttu-id="cf887-131">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cf887-131">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="cf887-132">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cf887-132">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="cf887-133">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cf887-133">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="cf887-134">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cf887-134">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="cf887-135">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cf887-135">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="cf887-136">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cf887-136">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="cf887-137">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cf887-137">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="cf887-138">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cf887-138">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


