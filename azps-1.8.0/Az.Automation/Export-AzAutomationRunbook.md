---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
ms.openlocfilehash: 6d0af3f0d991d8d6b1f73c3277f9f86ac8dd0dae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701645"
---
# <span data-ttu-id="2285f-101">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2285f-101">Export-AzAutomationRunbook</span></span>

## <span data-ttu-id="2285f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2285f-102">SYNOPSIS</span></span>
<span data-ttu-id="2285f-103">자동화 runbook을 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="2285f-103">Exports an Automation runbook.</span></span>

## <span data-ttu-id="2285f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2285f-104">SYNTAX</span></span>

```
Export-AzAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2285f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2285f-105">DESCRIPTION</span></span>
<span data-ttu-id="2285f-106">**AzAutomationRunbook** cmdlet은 wps_2 또는 wps_2 워크플로 runbook에 대 한 wps_2 script (ps1) 파일 또는 그래픽 runbook (graphrunbook) 파일로 Azure Automation runbook을 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="2285f-106">The **Export-AzAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="2285f-107">Runbook의 이름은 내보낸 파일의 이름이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2285f-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="2285f-108">예제의</span><span class="sxs-lookup"><span data-stu-id="2285f-108">EXAMPLES</span></span>

### <span data-ttu-id="2285f-109">예제 1: runbook 내보내기</span><span class="sxs-lookup"><span data-stu-id="2285f-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="2285f-110">이 명령은 자동화 runbook의 게시 된 버전을 사용자 데스크톱으로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="2285f-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="2285f-111">변수</span><span class="sxs-lookup"><span data-stu-id="2285f-111">PARAMETERS</span></span>

### <span data-ttu-id="2285f-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2285f-112">-AutomationAccountName</span></span>
<span data-ttu-id="2285f-113">이 cmdlet이 runbook을 내보내는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2285f-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="2285f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2285f-114">-DefaultProfile</span></span>
<span data-ttu-id="2285f-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2285f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2285f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2285f-116">-Force</span></span>
<span data-ttu-id="2285f-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="2285f-117">ps_force</span></span>

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

### <span data-ttu-id="2285f-118">-이름</span><span class="sxs-lookup"><span data-stu-id="2285f-118">-Name</span></span>
<span data-ttu-id="2285f-119">이 cmdlet이 내보내는 runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2285f-119">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="2285f-120">Runbook의 이름은 내보내기 파일의 이름이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2285f-120">The name of the runbook becomes the name of the export file.</span></span>

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

### <span data-ttu-id="2285f-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="2285f-121">-OutputFolder</span></span>
<span data-ttu-id="2285f-122">이 cmdlet이 내보내기 파일을 만드는 폴더의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2285f-122">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

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

### <span data-ttu-id="2285f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2285f-123">-ResourceGroupName</span></span>
<span data-ttu-id="2285f-124">이 cmdlet이 runbook을 내보내는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2285f-124">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="2285f-125">-슬롯</span><span class="sxs-lookup"><span data-stu-id="2285f-125">-Slot</span></span>
<span data-ttu-id="2285f-126">이 cmdlet이 runbook의 초안 또는 게시 된 콘텐츠를 내보내도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2285f-126">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="2285f-127">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2285f-127">Valid values are:</span></span> 
- <span data-ttu-id="2285f-128">게시자</span><span class="sxs-lookup"><span data-stu-id="2285f-128">Published</span></span> 
- <span data-ttu-id="2285f-129">함</span><span class="sxs-lookup"><span data-stu-id="2285f-129">Draft</span></span>

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

### <span data-ttu-id="2285f-130">-확인</span><span class="sxs-lookup"><span data-stu-id="2285f-130">-Confirm</span></span>
<span data-ttu-id="2285f-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2285f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2285f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2285f-132">-WhatIf</span></span>
<span data-ttu-id="2285f-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2285f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2285f-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2285f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2285f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2285f-135">CommonParameters</span></span>
<span data-ttu-id="2285f-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2285f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2285f-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2285f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2285f-138">입력</span><span class="sxs-lookup"><span data-stu-id="2285f-138">INPUTS</span></span>

### <span data-ttu-id="2285f-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2285f-139">System.String</span></span>

## <span data-ttu-id="2285f-140">출력</span><span class="sxs-lookup"><span data-stu-id="2285f-140">OUTPUTS</span></span>

### <span data-ttu-id="2285f-141">DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="2285f-141">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="2285f-142">상속자</span><span class="sxs-lookup"><span data-stu-id="2285f-142">NOTES</span></span>

## <span data-ttu-id="2285f-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2285f-143">RELATED LINKS</span></span>

[<span data-ttu-id="2285f-144">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2285f-144">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="2285f-145">가져오기-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2285f-145">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="2285f-146">새로운 AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2285f-146">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="2285f-147">새로운 AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2285f-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="2285f-148">게시-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2285f-148">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="2285f-149">제거-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2285f-149">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="2285f-150">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2285f-150">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="2285f-151">시작-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2285f-151">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


