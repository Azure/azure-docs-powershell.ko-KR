---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationdscnodereportcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
ms.openlocfilehash: dd29a092ec0ca3b24614b363147d4c50bf14dcbe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199676"
---
# <span data-ttu-id="38606-101">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="38606-101">Export-AzAutomationDscNodeReportContent</span></span>

## <span data-ttu-id="38606-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38606-102">SYNOPSIS</span></span>
<span data-ttu-id="38606-103">DSC 노드에서 Automation으로 전송된 DSC 보고서의 원시 콘텐츠를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38606-103">Exports the raw content of a DSC report sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="38606-104">구문</span><span class="sxs-lookup"><span data-stu-id="38606-104">SYNTAX</span></span>

```
Export-AzAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38606-105">설명</span><span class="sxs-lookup"><span data-stu-id="38606-105">DESCRIPTION</span></span>
<span data-ttu-id="38606-106">**Export-AzAutomationDscNodeReportContent** cmdlet은 APS DSC(Desired State Configuration) 보고서의 원시 콘텐츠를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38606-106">The **Export-AzAutomationDscNodeReportContent** cmdlet exports the raw contents of an APS Desired State Configuration (DSC) report.</span></span>
<span data-ttu-id="38606-107">DSC 노드는 Azure Automation에 DSC 보고서를 전송합니다.</span><span class="sxs-lookup"><span data-stu-id="38606-107">A DSC node sends a DSC report to Azure Automation.</span></span>

## <span data-ttu-id="38606-108">예제</span><span class="sxs-lookup"><span data-stu-id="38606-108">EXAMPLES</span></span>

### <span data-ttu-id="38606-109">예제 1: DSC 노드에서 보고서 내보내기</span><span class="sxs-lookup"><span data-stu-id="38606-109">Example 1: Export a report from a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="38606-110">이 명령 집합은 Computer14라는 DSC 노드에서 데스크톱으로 최신 보고서를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38606-110">This set of commands exports the latest report from the DSC node named Computer14 to the desktop.</span></span>

## <span data-ttu-id="38606-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38606-111">PARAMETERS</span></span>

### <span data-ttu-id="38606-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="38606-112">-AutomationAccountName</span></span>
<span data-ttu-id="38606-113">Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="38606-113">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="38606-114">이 cmdlet은 이 매개 변수가 지정하는 Automation 계정에 속하는 DSC 노드에 대한 보고서 콘텐츠를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38606-114">This cmdlet exports report content for a DSC node that belongs to the Automation account that this parameter specifies.</span></span>

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

### <span data-ttu-id="38606-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38606-115">-DefaultProfile</span></span>
<span data-ttu-id="38606-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="38606-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38606-117">-Force</span><span class="sxs-lookup"><span data-stu-id="38606-117">-Force</span></span>
<span data-ttu-id="38606-118">이 cmdlet이 기존 로컬 파일을 이름이 같은 새 파일로 대체하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="38606-118">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="38606-119">-NodeId</span><span class="sxs-lookup"><span data-stu-id="38606-119">-NodeId</span></span>
<span data-ttu-id="38606-120">이 cmdlet이 보고서 콘텐츠를 내보낼 DSC 노드의 고유 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="38606-120">Specifies the unique ID of the DSC node for which this cmdlet exports report contents.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38606-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="38606-121">-OutputFolder</span></span>
<span data-ttu-id="38606-122">이 cmdlet이 보고서 콘텐츠를 내보내는 출력 폴더를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="38606-122">Specifies the output folder where this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="38606-123">-ReportId</span><span class="sxs-lookup"><span data-stu-id="38606-123">-ReportId</span></span>
<span data-ttu-id="38606-124">이 cmdlet이 내보낼 DSC 노드 보고서의 고유 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="38606-124">Specifies the unique ID of the DSC node report that this cmdlet exports.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38606-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38606-125">-ResourceGroupName</span></span>
<span data-ttu-id="38606-126">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="38606-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="38606-127">이 cmdlet은 이 cmdlet에서 지정하는 리소스 그룹에 속하는 DSC 노드에 대한 보고서의 콘텐츠를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38606-127">This cmdlet exports the contents of a report for the DSC node that belongs to the resource group that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="38606-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38606-128">-Confirm</span></span>
<span data-ttu-id="38606-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="38606-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38606-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38606-130">-WhatIf</span></span>
<span data-ttu-id="38606-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="38606-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38606-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="38606-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38606-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38606-133">CommonParameters</span></span>
<span data-ttu-id="38606-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="38606-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38606-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="38606-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38606-136">입력</span><span class="sxs-lookup"><span data-stu-id="38606-136">INPUTS</span></span>

### <span data-ttu-id="38606-137">System.Guid</span><span class="sxs-lookup"><span data-stu-id="38606-137">System.Guid</span></span>

### <span data-ttu-id="38606-138">System.String</span><span class="sxs-lookup"><span data-stu-id="38606-138">System.String</span></span>

## <span data-ttu-id="38606-139">출력</span><span class="sxs-lookup"><span data-stu-id="38606-139">OUTPUTS</span></span>

### <span data-ttu-id="38606-140">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="38606-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="38606-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="38606-141">NOTES</span></span>

## <span data-ttu-id="38606-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="38606-142">RELATED LINKS</span></span>

[<span data-ttu-id="38606-143">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="38606-143">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)

[<span data-ttu-id="38606-144">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="38606-144">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="38606-145">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="38606-145">Get-AzAutomationDscNodeReport</span></span>](./Get-AzAutomationDscNodeReport.md)


