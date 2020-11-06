---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
ms.openlocfilehash: c3ae9da7959d606ec8ab92ed7a05e502d03b12a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531241"
---
# <span data-ttu-id="dc3d4-101">Get-AzureRmAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="dc3d4-101">Get-AzureRmAutomationDscNodeReport</span></span>

## <span data-ttu-id="dc3d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc3d4-102">SYNOPSIS</span></span>
<span data-ttu-id="dc3d4-103">DSC 노드에서 자동화로 전송 되는 보고서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-103">Gets reports sent from a DSC node to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc3d4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dc3d4-104">SYNTAX</span></span>

### <span data-ttu-id="dc3d4-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="dc3d4-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc3d4-106">최신 버전</span><span class="sxs-lookup"><span data-stu-id="dc3d4-106">ByLatest</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc3d4-107">ById</span><span class="sxs-lookup"><span data-stu-id="dc3d4-107">ById</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc3d4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="dc3d4-108">DESCRIPTION</span></span>
<span data-ttu-id="dc3d4-109">**AzureRmAutomationDscNodeReport** CMDLET은 DSC (Ap 원하는 상태 구성) 노드에서 Azure Automation으로 보낸 보고서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-109">The **Get-AzureRmAutomationDscNodeReport** cmdlet gets reports sent from an APS Desired State Configuration (DSC) node to Azure Automation.</span></span>

## <span data-ttu-id="dc3d4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="dc3d4-110">EXAMPLES</span></span>

### <span data-ttu-id="dc3d4-111">예제 1: DSC 노드에 대 한 모든 보고서 가져오기</span><span class="sxs-lookup"><span data-stu-id="dc3d4-111">Example 1: Get all reports for a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

<span data-ttu-id="dc3d4-112">첫 번째 명령은 Contoso17 이라는 Automation 계정에서 Computer14 이라는 컴퓨터에 대 한 DSC 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-112">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="dc3d4-113">이 명령은 $Node 변수에이 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-113">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="dc3d4-114">두 번째 명령은 Computer14 이라는 DSC 노드에서 Contoso17 이라는 Automation 계정으로 전송 된 모든 보고서에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-114">The second command gets metadata for all reports sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>
<span data-ttu-id="dc3d4-115">이 명령은 $Node 개체의 **Id** 속성을 사용 하 여 노드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-115">The command specifies the node by using the **Id** property of the $Node object.</span></span>

### <span data-ttu-id="dc3d4-116">예제 2: 보고서 ID를 기준으로 DSC 노드에 대 한 보고서 가져오기</span><span class="sxs-lookup"><span data-stu-id="dc3d4-116">Example 2: Get a report for a DSC node by report ID</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="dc3d4-117">첫 번째 명령은 Contoso17 이라는 Automation 계정에서 Computer14 이라는 컴퓨터에 대 한 DSC 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-117">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="dc3d4-118">이 명령은 $Node 변수에이 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-118">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="dc3d4-119">두 번째 명령은 Computer14 이라는 DSC 노드에서 Contoso17 이라는 자동화 계정으로 보낸 지정 된 ID로 식별 되는 보고서의 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-119">The second command gets metadata for the report identified by the specified ID sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

### <span data-ttu-id="dc3d4-120">예제 3: DSC 노드에 대 한 최신 보고서 가져오기</span><span class="sxs-lookup"><span data-stu-id="dc3d4-120">Example 3: Get the latest report for a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

<span data-ttu-id="dc3d4-121">첫 번째 명령은 Contoso17 이라는 Automation 계정에서 Computer14 이라는 컴퓨터에 대 한 DSC 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-121">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="dc3d4-122">이 명령은 $Node 변수에이 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-122">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="dc3d4-123">두 번째 명령은 Computer14 이라는 DSC 노드에서 Contoso17 이라는 자동화 계정으로 전송 된 최신 보고서의 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-123">The second command gets metadata for the latest report sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

## <span data-ttu-id="dc3d4-124">변수</span><span class="sxs-lookup"><span data-stu-id="dc3d4-124">PARAMETERS</span></span>

### <span data-ttu-id="dc3d4-125">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dc3d4-125">-AutomationAccountName</span></span>
<span data-ttu-id="dc3d4-126">Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-126">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="dc3d4-127">이 cmdlet은이 매개 변수에서 지정 하는 계정에 속하는 DSC 노드에 대 한 보고서를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-127">This cmdlet exports reports for a DSC node that belongs to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="dc3d4-128">-EndTime</span><span class="sxs-lookup"><span data-stu-id="dc3d4-128">-EndTime</span></span>
<span data-ttu-id="dc3d4-129">종료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-129">Specifies an end time.</span></span>
<span data-ttu-id="dc3d4-130">이 cmdlet은이 시간 전에 자동으로 받은 보고서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-130">This cmdlet gets reports that Automation received before this time.</span></span>

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

### <span data-ttu-id="dc3d4-131">-Id</span><span class="sxs-lookup"><span data-stu-id="dc3d4-131">-Id</span></span>
<span data-ttu-id="dc3d4-132">이 cmdlet이 가져올 DSC 노드 보고서의 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-132">Specifies the unique ID of the DSC node report for this cmdlet to get.</span></span>

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

### <span data-ttu-id="dc3d4-133">-최신 버전</span><span class="sxs-lookup"><span data-stu-id="dc3d4-133">-Latest</span></span>
<span data-ttu-id="dc3d4-134">이 cmdlet이 지정 된 노드에 대 한 최신 DSC 보고서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-134">Indicates that this cmdlet gets the latest DSC report for the specified node only.</span></span>

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

### <span data-ttu-id="dc3d4-135">-NodeId</span><span class="sxs-lookup"><span data-stu-id="dc3d4-135">-NodeId</span></span>
<span data-ttu-id="dc3d4-136">이 cmdlet에서 보고서를 가져올 DSC 노드의 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-136">Specifies the unique ID of the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="dc3d4-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc3d4-137">-ResourceGroupName</span></span>
<span data-ttu-id="dc3d4-138">이 cmdlet에서 보고서를 가져올 DSC 노드가 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-138">Specifies the name of a resource group that contains the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="dc3d4-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="dc3d4-139">-StartTime</span></span>
<span data-ttu-id="dc3d4-140">시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-140">Specifies a start time.</span></span>
<span data-ttu-id="dc3d4-141">이 cmdlet은이 시간 이후에 자동으로 받은 보고서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-141">This cmdlet gets reports that Automation received after this time.</span></span>

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

### <span data-ttu-id="dc3d4-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc3d4-142">-DefaultProfile</span></span>
<span data-ttu-id="dc3d4-143">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc3d4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc3d4-144">CommonParameters</span></span>
<span data-ttu-id="dc3d4-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc3d4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc3d4-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc3d4-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc3d4-147">입력</span><span class="sxs-lookup"><span data-stu-id="dc3d4-147">INPUTS</span></span>

## <span data-ttu-id="dc3d4-148">출력</span><span class="sxs-lookup"><span data-stu-id="dc3d4-148">OUTPUTS</span></span>

### <span data-ttu-id="dc3d4-149">Microsoft Azure.-DscNode</span><span class="sxs-lookup"><span data-stu-id="dc3d4-149">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="dc3d4-150">상속자</span><span class="sxs-lookup"><span data-stu-id="dc3d4-150">NOTES</span></span>

## <span data-ttu-id="dc3d4-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc3d4-151">RELATED LINKS</span></span>

[<span data-ttu-id="dc3d4-152">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="dc3d4-152">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="dc3d4-153">Export-AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="dc3d4-153">Export-AzureRmAutomationDscNodeReportContent</span></span>](./Export-AzureRmAutomationDscNodeReportContent.md)


