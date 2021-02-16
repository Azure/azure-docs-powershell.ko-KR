---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
ms.openlocfilehash: 03a57c35063a401aa5f730e11538532bdbbbc58c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205581"
---
# <span data-ttu-id="0147b-101">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0147b-101">Export-AzAutomationRunbook</span></span>

## <span data-ttu-id="0147b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0147b-102">SYNOPSIS</span></span>
<span data-ttu-id="0147b-103">Automation Runbook을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0147b-103">Exports an Automation runbook.</span></span>

## <span data-ttu-id="0147b-104">구문</span><span class="sxs-lookup"><span data-stu-id="0147b-104">SYNTAX</span></span>

```
Export-AzAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0147b-105">설명</span><span class="sxs-lookup"><span data-stu-id="0147b-105">DESCRIPTION</span></span>
<span data-ttu-id="0147b-106">**Export-AzAutomationRunbook** cmdlet은 Azure Automation Runbook을 wps_2 스크립트(.ps1) 파일, wps_2 또는 wps_2 Workflow Runbook의 경우 또는 그래픽 Runbook의 경우 그래픽 Runbook(.graphrunbook) 파일로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0147b-106">The **Export-AzAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="0147b-107">Runbook의 이름은 내보낼 파일의 이름이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0147b-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="0147b-108">예제</span><span class="sxs-lookup"><span data-stu-id="0147b-108">EXAMPLES</span></span>

### <span data-ttu-id="0147b-109">예제 1: Runbook 내보내기</span><span class="sxs-lookup"><span data-stu-id="0147b-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="0147b-110">이 명령은 게시된 버전의 Automation Runbook을 사용자 데스크톱으로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0147b-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="0147b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0147b-111">PARAMETERS</span></span>

### <span data-ttu-id="0147b-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0147b-112">-AutomationAccountName</span></span>
<span data-ttu-id="0147b-113">이 cmdlet이 Runbook을 내보낼 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0147b-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="0147b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0147b-114">-DefaultProfile</span></span>
<span data-ttu-id="0147b-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0147b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0147b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="0147b-116">-Force</span></span>
<span data-ttu-id="0147b-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="0147b-117">ps_force</span></span>

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

### <span data-ttu-id="0147b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="0147b-118">-Name</span></span>
<span data-ttu-id="0147b-119">이 cmdlet이 내보낼 Runbook의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0147b-119">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="0147b-120">Runbook의 이름은 내보내기 파일의 이름이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0147b-120">The name of the runbook becomes the name of the export file.</span></span>

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

### <span data-ttu-id="0147b-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="0147b-121">-OutputFolder</span></span>
<span data-ttu-id="0147b-122">이 cmdlet이 내보내기 파일을 만드는 폴더의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0147b-122">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

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

### <span data-ttu-id="0147b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0147b-123">-ResourceGroupName</span></span>
<span data-ttu-id="0147b-124">이 cmdlet이 Runbook을 내보낼 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0147b-124">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="0147b-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="0147b-125">-Slot</span></span>
<span data-ttu-id="0147b-126">이 cmdlet이 Runbook의 초안 또는 게시된 콘텐츠를 내보낼지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0147b-126">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="0147b-127">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="0147b-127">Valid values are:</span></span> 
- <span data-ttu-id="0147b-128">게시</span><span class="sxs-lookup"><span data-stu-id="0147b-128">Published</span></span> 
- <span data-ttu-id="0147b-129">초안</span><span class="sxs-lookup"><span data-stu-id="0147b-129">Draft</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0147b-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0147b-130">-Confirm</span></span>
<span data-ttu-id="0147b-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0147b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0147b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0147b-132">-WhatIf</span></span>
<span data-ttu-id="0147b-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0147b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0147b-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0147b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0147b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0147b-135">CommonParameters</span></span>
<span data-ttu-id="0147b-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0147b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0147b-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0147b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0147b-138">입력</span><span class="sxs-lookup"><span data-stu-id="0147b-138">INPUTS</span></span>

### <span data-ttu-id="0147b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="0147b-139">System.String</span></span>

## <span data-ttu-id="0147b-140">출력</span><span class="sxs-lookup"><span data-stu-id="0147b-140">OUTPUTS</span></span>

### <span data-ttu-id="0147b-141">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="0147b-141">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="0147b-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0147b-142">NOTES</span></span>

## <span data-ttu-id="0147b-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0147b-143">RELATED LINKS</span></span>

[<span data-ttu-id="0147b-144">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0147b-144">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="0147b-145">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0147b-145">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="0147b-146">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0147b-146">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="0147b-147">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0147b-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="0147b-148">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0147b-148">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="0147b-149">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0147b-149">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="0147b-150">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0147b-150">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="0147b-151">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0147b-151">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


