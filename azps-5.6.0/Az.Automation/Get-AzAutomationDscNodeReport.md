---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
ms.openlocfilehash: bb88bc38f6102f18b4d45b3b80902886975e2628
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987051"
---
# <span data-ttu-id="18fb2-101">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="18fb2-101">Get-AzAutomationDscNodeReport</span></span>

## <span data-ttu-id="18fb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18fb2-102">SYNOPSIS</span></span>
<span data-ttu-id="18fb2-103">DSC 노드에서 Automation으로 전송된 보고서를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="18fb2-103">Gets reports sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="18fb2-104">구문</span><span class="sxs-lookup"><span data-stu-id="18fb2-104">SYNTAX</span></span>

### <span data-ttu-id="18fb2-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="18fb2-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="18fb2-106">ByLatest</span><span class="sxs-lookup"><span data-stu-id="18fb2-106">ByLatest</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18fb2-107">ById</span><span class="sxs-lookup"><span data-stu-id="18fb2-107">ById</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18fb2-108">설명</span><span class="sxs-lookup"><span data-stu-id="18fb2-108">DESCRIPTION</span></span>
<span data-ttu-id="18fb2-109">**Get-AzAutomationDscNodeReport** cmdlet은 APS 원하는 상태 구성(DSC) 노드에서 Azure Automation으로 전송된 보고서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="18fb2-109">The **Get-AzAutomationDscNodeReport** cmdlet gets reports sent from an APS Desired State Configuration (DSC) node to Azure Automation.</span></span>

## <span data-ttu-id="18fb2-110">예제</span><span class="sxs-lookup"><span data-stu-id="18fb2-110">EXAMPLES</span></span>

### <span data-ttu-id="18fb2-111">예제 1: DSC 노드에 대한 모든 보고서 사용</span><span class="sxs-lookup"><span data-stu-id="18fb2-111">Example 1: Get all reports for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

<span data-ttu-id="18fb2-112">첫 번째 명령은 Contoso17이라는 Automation 계정에서 Computer14라는 컴퓨터에 대한 DSC 노드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="18fb2-112">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="18fb2-113">명령은 이 개체를 $Node 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="18fb2-113">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="18fb2-114">두 번째 명령은 Computer14라는 DSC 노드에서 Contoso17이라는 Automation 계정으로 전송된 모든 보고서의 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="18fb2-114">The second command gets metadata for all reports sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>
<span data-ttu-id="18fb2-115">명령은 개체의 **ID** 속성을 사용하여 노드를 $Node 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="18fb2-115">The command specifies the node by using the **Id** property of the $Node object.</span></span>

### <span data-ttu-id="18fb2-116">예제 2: 보고서 ID로 DSC 노드에 대한 보고서 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="18fb2-116">Example 2: Get a report for a DSC node by report ID</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="18fb2-117">첫 번째 명령은 Contoso17이라는 Automation 계정에서 Computer14라는 컴퓨터에 대한 DSC 노드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="18fb2-117">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="18fb2-118">명령은 이 개체를 $Node 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="18fb2-118">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="18fb2-119">두 번째 명령은 Computer14라는 DSC 노드에서 Contoso17이라는 Automation 계정으로 전송된 지정된 ID로 식별된 보고서의 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="18fb2-119">The second command gets metadata for the report identified by the specified ID sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

### <span data-ttu-id="18fb2-120">예제 3: DSC 노드에 대한 최신 보고서 다운로드</span><span class="sxs-lookup"><span data-stu-id="18fb2-120">Example 3: Get the latest report for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

<span data-ttu-id="18fb2-121">첫 번째 명령은 Contoso17이라는 Automation 계정에서 Computer14라는 컴퓨터에 대한 DSC 노드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="18fb2-121">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="18fb2-122">명령은 이 개체를 $Node 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="18fb2-122">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="18fb2-123">두 번째 명령은 Computer14라는 DSC 노드에서 Contoso17이라는 Automation 계정으로 전송된 최신 보고서의 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="18fb2-123">The second command gets metadata for the latest report sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

## <span data-ttu-id="18fb2-124">매개 변수</span><span class="sxs-lookup"><span data-stu-id="18fb2-124">PARAMETERS</span></span>

### <span data-ttu-id="18fb2-125">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="18fb2-125">-AutomationAccountName</span></span>
<span data-ttu-id="18fb2-126">Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="18fb2-126">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="18fb2-127">이 cmdlet은 이 매개 변수가 지정하는 계정에 속하는 DSC 노드에 대한 보고서를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="18fb2-127">This cmdlet exports reports for a DSC node that belongs to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="18fb2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18fb2-128">-DefaultProfile</span></span>
<span data-ttu-id="18fb2-129">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="18fb2-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18fb2-130">-EndTime</span><span class="sxs-lookup"><span data-stu-id="18fb2-130">-EndTime</span></span>
<span data-ttu-id="18fb2-131">종료 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="18fb2-131">Specifies an end time.</span></span>
<span data-ttu-id="18fb2-132">이 cmdlet은 자동화가 이 시간 전에 수신한 보고서를 수신합니다.</span><span class="sxs-lookup"><span data-stu-id="18fb2-132">This cmdlet gets reports that Automation received before this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18fb2-133">-Id</span><span class="sxs-lookup"><span data-stu-id="18fb2-133">-Id</span></span>
<span data-ttu-id="18fb2-134">이 cmdlet에서 얻을 DSC 노드 보고서의 고유 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="18fb2-134">Specifies the unique ID of the DSC node report for this cmdlet to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: ReportId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18fb2-135">-Latest</span><span class="sxs-lookup"><span data-stu-id="18fb2-135">-Latest</span></span>
<span data-ttu-id="18fb2-136">이 cmdlet은 지정된 노드에만 대한 최신 DSC 보고서를 을 를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="18fb2-136">Indicates that this cmdlet gets the latest DSC report for the specified node only.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByLatest
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18fb2-137">-NodeId</span><span class="sxs-lookup"><span data-stu-id="18fb2-137">-NodeId</span></span>
<span data-ttu-id="18fb2-138">이 cmdlet에서 보고서를 얻을 수 있는 DSC 노드의 고유 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="18fb2-138">Specifies the unique ID of the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="18fb2-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18fb2-139">-ResourceGroupName</span></span>
<span data-ttu-id="18fb2-140">이 cmdlet에서 보고서를 받을 DSC 노드를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="18fb2-140">Specifies the name of a resource group that contains the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="18fb2-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="18fb2-141">-StartTime</span></span>
<span data-ttu-id="18fb2-142">시작 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="18fb2-142">Specifies a start time.</span></span>
<span data-ttu-id="18fb2-143">이 cmdlet은 자동화가 이 시간 이후에 수신한 보고서를 수신합니다.</span><span class="sxs-lookup"><span data-stu-id="18fb2-143">This cmdlet gets reports that Automation received after this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18fb2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18fb2-144">CommonParameters</span></span>
<span data-ttu-id="18fb2-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="18fb2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18fb2-146">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="18fb2-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18fb2-147">입력</span><span class="sxs-lookup"><span data-stu-id="18fb2-147">INPUTS</span></span>

### <span data-ttu-id="18fb2-148">System.Guid</span><span class="sxs-lookup"><span data-stu-id="18fb2-148">System.Guid</span></span>

### <span data-ttu-id="18fb2-149">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="18fb2-149">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="18fb2-150">System.String</span><span class="sxs-lookup"><span data-stu-id="18fb2-150">System.String</span></span>

## <span data-ttu-id="18fb2-151">출력</span><span class="sxs-lookup"><span data-stu-id="18fb2-151">OUTPUTS</span></span>

### <span data-ttu-id="18fb2-152">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="18fb2-152">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="18fb2-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="18fb2-153">NOTES</span></span>

## <span data-ttu-id="18fb2-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="18fb2-154">RELATED LINKS</span></span>

[<span data-ttu-id="18fb2-155">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="18fb2-155">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="18fb2-156">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="18fb2-156">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)


