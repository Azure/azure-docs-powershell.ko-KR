---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationdscnodereportcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
ms.openlocfilehash: dd29a092ec0ca3b24614b363147d4c50bf14dcbe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204101"
---
# <span data-ttu-id="67653-101">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="67653-101">Export-AzAutomationDscNodeReportContent</span></span>

## <span data-ttu-id="67653-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67653-102">SYNOPSIS</span></span>
<span data-ttu-id="67653-103">DSC 노드에서 전송 되는 DSC 보고서의 원시 콘텐츠를 자동화로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="67653-103">Exports the raw content of a DSC report sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="67653-104">구문과</span><span class="sxs-lookup"><span data-stu-id="67653-104">SYNTAX</span></span>

```
Export-AzAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67653-105">설명은</span><span class="sxs-lookup"><span data-stu-id="67653-105">DESCRIPTION</span></span>
<span data-ttu-id="67653-106">**Export-AzAutomationDscNodeReportContent** CMDLET은 DSC (원하는 상태 구성) 보고서의 원시 콘텐츠를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="67653-106">The **Export-AzAutomationDscNodeReportContent** cmdlet exports the raw contents of an APS Desired State Configuration (DSC) report.</span></span>
<span data-ttu-id="67653-107">DSC 노드에서는 DSC 보고서를 Azure 자동화로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="67653-107">A DSC node sends a DSC report to Azure Automation.</span></span>

## <span data-ttu-id="67653-108">예제의</span><span class="sxs-lookup"><span data-stu-id="67653-108">EXAMPLES</span></span>

### <span data-ttu-id="67653-109">예제 1: DSC 노드에서 보고서 내보내기</span><span class="sxs-lookup"><span data-stu-id="67653-109">Example 1: Export a report from a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="67653-110">이 명령 집합은 Computer14 이라는 DSC 노드에서 최신 보고서를 데스크톱으로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="67653-110">This set of commands exports the latest report from the DSC node named Computer14 to the desktop.</span></span>

## <span data-ttu-id="67653-111">변수</span><span class="sxs-lookup"><span data-stu-id="67653-111">PARAMETERS</span></span>

### <span data-ttu-id="67653-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="67653-112">-AutomationAccountName</span></span>
<span data-ttu-id="67653-113">Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67653-113">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="67653-114">이 cmdlet은이 매개 변수에서 지정 하는 자동화 계정에 속하는 DSC 노드에 대 한 보고서 콘텐츠를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="67653-114">This cmdlet exports report content for a DSC node that belongs to the Automation account that this parameter specifies.</span></span>

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

### <span data-ttu-id="67653-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67653-115">-DefaultProfile</span></span>
<span data-ttu-id="67653-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="67653-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67653-117">-Force</span><span class="sxs-lookup"><span data-stu-id="67653-117">-Force</span></span>
<span data-ttu-id="67653-118">이 cmdlet이 기존 로컬 파일을 동일한 이름을 가진 새 파일로 대체 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="67653-118">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="67653-119">-NodeId</span><span class="sxs-lookup"><span data-stu-id="67653-119">-NodeId</span></span>
<span data-ttu-id="67653-120">이 cmdlet이 보고서 콘텐츠를 내보내는 DSC 노드의 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67653-120">Specifies the unique ID of the DSC node for which this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="67653-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="67653-121">-OutputFolder</span></span>
<span data-ttu-id="67653-122">이 cmdlet이 보고서 콘텐츠를 내보내는 출력 폴더를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67653-122">Specifies the output folder where this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="67653-123">-ReportId</span><span class="sxs-lookup"><span data-stu-id="67653-123">-ReportId</span></span>
<span data-ttu-id="67653-124">이 cmdlet이 내보내는 DSC 노드 보고서의 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67653-124">Specifies the unique ID of the DSC node report that this cmdlet exports.</span></span>

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

### <span data-ttu-id="67653-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67653-125">-ResourceGroupName</span></span>
<span data-ttu-id="67653-126">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67653-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="67653-127">이 cmdlet은이 cmdlet에서 지정 하는 리소스 그룹에 속하는 DSC 노드에 대 한 보고서의 콘텐츠를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="67653-127">This cmdlet exports the contents of a report for the DSC node that belongs to the resource group that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="67653-128">-확인</span><span class="sxs-lookup"><span data-stu-id="67653-128">-Confirm</span></span>
<span data-ttu-id="67653-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="67653-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67653-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67653-130">-WhatIf</span></span>
<span data-ttu-id="67653-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="67653-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67653-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67653-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67653-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67653-133">CommonParameters</span></span>
<span data-ttu-id="67653-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67653-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67653-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67653-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67653-136">입력</span><span class="sxs-lookup"><span data-stu-id="67653-136">INPUTS</span></span>

### <span data-ttu-id="67653-137">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="67653-137">System.Guid</span></span>

### <span data-ttu-id="67653-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="67653-138">System.String</span></span>

## <span data-ttu-id="67653-139">출력</span><span class="sxs-lookup"><span data-stu-id="67653-139">OUTPUTS</span></span>

### <span data-ttu-id="67653-140">DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="67653-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="67653-141">상속자</span><span class="sxs-lookup"><span data-stu-id="67653-141">NOTES</span></span>

## <span data-ttu-id="67653-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67653-142">RELATED LINKS</span></span>

[<span data-ttu-id="67653-143">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="67653-143">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)

[<span data-ttu-id="67653-144">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="67653-144">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="67653-145">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="67653-145">Get-AzAutomationDscNodeReport</span></span>](./Get-AzAutomationDscNodeReport.md)


