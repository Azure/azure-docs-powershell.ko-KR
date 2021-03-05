---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
ms.openlocfilehash: 26a84b381e3193f9f95f21135f40489f0cacb754
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004720"
---
# <span data-ttu-id="c3fda-101">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c3fda-101">Set-AzAutomationRunbook</span></span>

## <span data-ttu-id="c3fda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3fda-102">SYNOPSIS</span></span>
<span data-ttu-id="c3fda-103">Runbook을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c3fda-103">Modifies a runbook.</span></span>

## <span data-ttu-id="c3fda-104">구문</span><span class="sxs-lookup"><span data-stu-id="c3fda-104">SYNTAX</span></span>

```
Set-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3fda-105">설명</span><span class="sxs-lookup"><span data-stu-id="c3fda-105">DESCRIPTION</span></span>
<span data-ttu-id="c3fda-106">**Set-AzAutomationRunbook** cmdlet은 APS에서 Azure Automation Runbook의 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c3fda-106">The **Set-AzAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="c3fda-107">예제</span><span class="sxs-lookup"><span data-stu-id="c3fda-107">EXAMPLES</span></span>

### <span data-ttu-id="c3fda-108">예제 1: Runbook에 대해 자세한 로깅 사용</span><span class="sxs-lookup"><span data-stu-id="c3fda-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c3fda-109">이 명령을 사용하면 Contoso17이라는 Azure Automation 계정에서 지정된 Runbook의 작업의 자세한 로깅을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3fda-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="c3fda-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c3fda-110">PARAMETERS</span></span>

### <span data-ttu-id="c3fda-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c3fda-111">-AutomationAccountName</span></span>
<span data-ttu-id="c3fda-112">이 cmdlet이 Runbook을 수정하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c3fda-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="c3fda-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3fda-113">-DefaultProfile</span></span>
<span data-ttu-id="c3fda-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c3fda-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3fda-115">-Description</span><span class="sxs-lookup"><span data-stu-id="c3fda-115">-Description</span></span>
<span data-ttu-id="c3fda-116">Runbook에 대한 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c3fda-116">Specifies a description for the runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3fda-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="c3fda-117">-LogProgress</span></span>
<span data-ttu-id="c3fda-118">Runbook 로그가 진행률인지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c3fda-118">Specifies whether the runbook logs progress.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3fda-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="c3fda-119">-LogVerbose</span></span>
<span data-ttu-id="c3fda-120">로깅에 자세한 정보가 포함되어 있는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c3fda-120">Specifies whether logging includes detailed information.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3fda-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c3fda-121">-Name</span></span>
<span data-ttu-id="c3fda-122">이 cmdlet이 수정하는 Runbook의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c3fda-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c3fda-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3fda-123">-ResourceGroupName</span></span>
<span data-ttu-id="c3fda-124">이 cmdlet이 Runbook을 수정하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c3fda-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="c3fda-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="c3fda-125">-Tag</span></span>
<span data-ttu-id="c3fda-126">Runbook 태그.</span><span class="sxs-lookup"><span data-stu-id="c3fda-126">The runbook tags.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3fda-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3fda-127">CommonParameters</span></span>
<span data-ttu-id="c3fda-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c3fda-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3fda-129">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c3fda-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3fda-130">입력</span><span class="sxs-lookup"><span data-stu-id="c3fda-130">INPUTS</span></span>

### <span data-ttu-id="c3fda-131">System.String</span><span class="sxs-lookup"><span data-stu-id="c3fda-131">System.String</span></span>

### <span data-ttu-id="c3fda-132">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="c3fda-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="c3fda-133">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c3fda-133">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c3fda-134">출력</span><span class="sxs-lookup"><span data-stu-id="c3fda-134">OUTPUTS</span></span>

### <span data-ttu-id="c3fda-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="c3fda-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="c3fda-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c3fda-136">NOTES</span></span>

## <span data-ttu-id="c3fda-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c3fda-137">RELATED LINKS</span></span>

[<span data-ttu-id="c3fda-138">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c3fda-138">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="c3fda-139">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c3fda-139">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="c3fda-140">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c3fda-140">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="c3fda-141">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c3fda-141">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="c3fda-142">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c3fda-142">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="c3fda-143">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c3fda-143">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="c3fda-144">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c3fda-144">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="c3fda-145">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c3fda-145">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


