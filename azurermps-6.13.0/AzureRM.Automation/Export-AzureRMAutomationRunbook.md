---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/export-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRMAutomationRunbook.md
ms.openlocfilehash: f982c68c49d6a8a92bb06bf150e352626730f67d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529648"
---
# <span data-ttu-id="5b8e6-101">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5b8e6-101">Export-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="5b8e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b8e6-102">SYNOPSIS</span></span>
<span data-ttu-id="5b8e6-103">자동화 runbook을 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="5b8e6-103">Exports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b8e6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5b8e6-104">SYNTAX</span></span>

```
Export-AzureRmAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b8e6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5b8e6-105">DESCRIPTION</span></span>
<span data-ttu-id="5b8e6-106">**AzureRmAutomationRunbook** cmdlet은 wps_2 또는 wps_2 워크플로 runbook에 대 한 wps_2 script (ps1) 파일 또는 그래픽 runbook (graphrunbook) 파일로 Azure Automation runbook을 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="5b8e6-106">The **Export-AzureRmAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="5b8e6-107">Runbook의 이름은 내보낸 파일의 이름이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b8e6-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="5b8e6-108">예제의</span><span class="sxs-lookup"><span data-stu-id="5b8e6-108">EXAMPLES</span></span>

### <span data-ttu-id="5b8e6-109">예제 1: runbook 내보내기</span><span class="sxs-lookup"><span data-stu-id="5b8e6-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzureRmAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="5b8e6-110">이 명령은 자동화 runbook의 게시 된 버전을 사용자 데스크톱으로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="5b8e6-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="5b8e6-111">변수</span><span class="sxs-lookup"><span data-stu-id="5b8e6-111">PARAMETERS</span></span>

### <span data-ttu-id="5b8e6-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5b8e6-112">-AutomationAccountName</span></span>
<span data-ttu-id="5b8e6-113">이 cmdlet이 runbook을 내보내는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8e6-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="5b8e6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b8e6-114">-DefaultProfile</span></span>
<span data-ttu-id="5b8e6-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5b8e6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b8e6-116">-Force</span><span class="sxs-lookup"><span data-stu-id="5b8e6-116">-Force</span></span>
<span data-ttu-id="5b8e6-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="5b8e6-117">ps_force</span></span>

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

### <span data-ttu-id="5b8e6-118">-이름</span><span class="sxs-lookup"><span data-stu-id="5b8e6-118">-Name</span></span>
<span data-ttu-id="5b8e6-119">이 cmdlet이 내보내는 runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8e6-119">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="5b8e6-120">Runbook의 이름은 내보내기 파일의 이름이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b8e6-120">The name of the runbook becomes the name of the export file.</span></span>

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

### <span data-ttu-id="5b8e6-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="5b8e6-121">-OutputFolder</span></span>
<span data-ttu-id="5b8e6-122">이 cmdlet이 내보내기 파일을 만드는 폴더의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8e6-122">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

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

### <span data-ttu-id="5b8e6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b8e6-123">-ResourceGroupName</span></span>
<span data-ttu-id="5b8e6-124">이 cmdlet이 runbook을 내보내는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8e6-124">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="5b8e6-125">-슬롯</span><span class="sxs-lookup"><span data-stu-id="5b8e6-125">-Slot</span></span>
<span data-ttu-id="5b8e6-126">이 cmdlet이 runbook의 초안 또는 게시 된 콘텐츠를 내보내도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8e6-126">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="5b8e6-127">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5b8e6-127">Valid values are:</span></span> 
- <span data-ttu-id="5b8e6-128">게시자</span><span class="sxs-lookup"><span data-stu-id="5b8e6-128">Published</span></span> 
- <span data-ttu-id="5b8e6-129">함</span><span class="sxs-lookup"><span data-stu-id="5b8e6-129">Draft</span></span>

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

### <span data-ttu-id="5b8e6-130">-확인</span><span class="sxs-lookup"><span data-stu-id="5b8e6-130">-Confirm</span></span>
<span data-ttu-id="5b8e6-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8e6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b8e6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b8e6-132">-WhatIf</span></span>
<span data-ttu-id="5b8e6-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5b8e6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b8e6-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b8e6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b8e6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b8e6-135">CommonParameters</span></span>
<span data-ttu-id="5b8e6-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b8e6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b8e6-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b8e6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b8e6-138">입력</span><span class="sxs-lookup"><span data-stu-id="5b8e6-138">INPUTS</span></span>

### <span data-ttu-id="5b8e6-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5b8e6-139">System.String</span></span>

## <span data-ttu-id="5b8e6-140">출력</span><span class="sxs-lookup"><span data-stu-id="5b8e6-140">OUTPUTS</span></span>

### <span data-ttu-id="5b8e6-141">DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="5b8e6-141">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="5b8e6-142">상속자</span><span class="sxs-lookup"><span data-stu-id="5b8e6-142">NOTES</span></span>

## <span data-ttu-id="5b8e6-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b8e6-143">RELATED LINKS</span></span>

[<span data-ttu-id="5b8e6-144">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5b8e6-144">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5b8e6-145">가져오기-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5b8e6-145">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5b8e6-146">새로운 AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5b8e6-146">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5b8e6-147">새로운 AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5b8e6-147">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5b8e6-148">게시-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5b8e6-148">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5b8e6-149">제거-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5b8e6-149">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5b8e6-150">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5b8e6-150">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5b8e6-151">시작-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5b8e6-151">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)

