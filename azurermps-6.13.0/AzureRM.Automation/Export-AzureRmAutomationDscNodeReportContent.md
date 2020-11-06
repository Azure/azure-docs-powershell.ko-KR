---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/export-azurermautomationdscnodereportcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscNodeReportContent.md
ms.openlocfilehash: 52ed2c5925758a4d40fdf39dcdadf73eb2fc53b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524668"
---
# <span data-ttu-id="08183-101">Export-AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="08183-101">Export-AzureRmAutomationDscNodeReportContent</span></span>

## <span data-ttu-id="08183-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08183-102">SYNOPSIS</span></span>
<span data-ttu-id="08183-103">DSC 노드에서 전송 되는 DSC 보고서의 원시 콘텐츠를 자동화로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="08183-103">Exports the raw content of a DSC report sent from a DSC node to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08183-104">구문과</span><span class="sxs-lookup"><span data-stu-id="08183-104">SYNTAX</span></span>

```
Export-AzureRmAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08183-105">설명은</span><span class="sxs-lookup"><span data-stu-id="08183-105">DESCRIPTION</span></span>
<span data-ttu-id="08183-106">**Export-AzureRmAutomationDscNodeReportContent** CMDLET은 DSC (원하는 상태 구성) 보고서의 원시 콘텐츠를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="08183-106">The **Export-AzureRmAutomationDscNodeReportContent** cmdlet exports the raw contents of an APS Desired State Configuration (DSC) report.</span></span>
<span data-ttu-id="08183-107">DSC 노드에서는 DSC 보고서를 Azure 자동화로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="08183-107">A DSC node sends a DSC report to Azure Automation.</span></span>

## <span data-ttu-id="08183-108">예제의</span><span class="sxs-lookup"><span data-stu-id="08183-108">EXAMPLES</span></span>

### <span data-ttu-id="08183-109">예제 1: DSC 노드에서 보고서 내보내기</span><span class="sxs-lookup"><span data-stu-id="08183-109">Example 1: Export a report from a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzureRmAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="08183-110">이 명령 집합은 Computer14 이라는 DSC 노드에서 최신 보고서를 데스크톱으로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="08183-110">This set of commands exports the latest report from the DSC node named Computer14 to the desktop.</span></span>

## <span data-ttu-id="08183-111">변수</span><span class="sxs-lookup"><span data-stu-id="08183-111">PARAMETERS</span></span>

### <span data-ttu-id="08183-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="08183-112">-AutomationAccountName</span></span>
<span data-ttu-id="08183-113">Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08183-113">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="08183-114">이 cmdlet은이 매개 변수에서 지정 하는 자동화 계정에 속하는 DSC 노드에 대 한 보고서 콘텐츠를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="08183-114">This cmdlet exports report content for a DSC node that belongs to the Automation account that this parameter specifies.</span></span>

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

### <span data-ttu-id="08183-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08183-115">-DefaultProfile</span></span>
<span data-ttu-id="08183-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="08183-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08183-117">-Force</span><span class="sxs-lookup"><span data-stu-id="08183-117">-Force</span></span>
<span data-ttu-id="08183-118">이 cmdlet이 기존 로컬 파일을 동일한 이름을 가진 새 파일로 대체 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="08183-118">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="08183-119">-NodeId</span><span class="sxs-lookup"><span data-stu-id="08183-119">-NodeId</span></span>
<span data-ttu-id="08183-120">이 cmdlet이 보고서 콘텐츠를 내보내는 DSC 노드의 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08183-120">Specifies the unique ID of the DSC node for which this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="08183-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="08183-121">-OutputFolder</span></span>
<span data-ttu-id="08183-122">이 cmdlet이 보고서 콘텐츠를 내보내는 출력 폴더를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08183-122">Specifies the output folder where this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="08183-123">-ReportId</span><span class="sxs-lookup"><span data-stu-id="08183-123">-ReportId</span></span>
<span data-ttu-id="08183-124">이 cmdlet이 내보내는 DSC 노드 보고서의 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08183-124">Specifies the unique ID of the DSC node report that this cmdlet exports.</span></span>

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

### <span data-ttu-id="08183-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08183-125">-ResourceGroupName</span></span>
<span data-ttu-id="08183-126">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08183-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="08183-127">이 cmdlet은이 cmdlet에서 지정 하는 리소스 그룹에 속하는 DSC 노드에 대 한 보고서의 콘텐츠를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="08183-127">This cmdlet exports the contents of a report for the DSC node that belongs to the resource group that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="08183-128">-확인</span><span class="sxs-lookup"><span data-stu-id="08183-128">-Confirm</span></span>
<span data-ttu-id="08183-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="08183-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08183-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08183-130">-WhatIf</span></span>
<span data-ttu-id="08183-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="08183-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08183-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="08183-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08183-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08183-133">CommonParameters</span></span>
<span data-ttu-id="08183-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="08183-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08183-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08183-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08183-136">입력</span><span class="sxs-lookup"><span data-stu-id="08183-136">INPUTS</span></span>

### <span data-ttu-id="08183-137">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="08183-137">System.Guid</span></span>

### <span data-ttu-id="08183-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="08183-138">System.String</span></span>

## <span data-ttu-id="08183-139">출력</span><span class="sxs-lookup"><span data-stu-id="08183-139">OUTPUTS</span></span>

### <span data-ttu-id="08183-140">DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="08183-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="08183-141">상속자</span><span class="sxs-lookup"><span data-stu-id="08183-141">NOTES</span></span>

## <span data-ttu-id="08183-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="08183-142">RELATED LINKS</span></span>

[<span data-ttu-id="08183-143">Export-AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="08183-143">Export-AzureRmAutomationDscNodeReportContent</span></span>](./Export-AzureRmAutomationDscNodeReportContent.md)

[<span data-ttu-id="08183-144">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="08183-144">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="08183-145">Get-AzureRmAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="08183-145">Get-AzureRmAutomationDscNodeReport</span></span>](./Get-AzureRmAutomationDscNodeReport.md)


