---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnodeconfigurationdeploymentschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md
ms.openlocfilehash: f29c4f5587b79fdc2c6eb03907ed5c1327406e8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703495"
---
# <span data-ttu-id="8ca34-101">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="8ca34-101">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="8ca34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ca34-102">SYNOPSIS</span></span>
<span data-ttu-id="8ca34-103">자동화에서 DSC 노드 구성 배포 작업 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8ca34-103">Gets a DSC Node configuration deployment job schedule in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ca34-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8ca34-104">SYNTAX</span></span>

### <span data-ttu-id="8ca34-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="8ca34-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ca34-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="8ca34-106">ByJobScheduleId</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ca34-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8ca34-107">DESCRIPTION</span></span>
<span data-ttu-id="8ca34-108">AzureRmAutomationDscNodeConfigurationDeployment cmdlet은 Azure Automation의 DSC (원하는 상태 구성) 노드 구성을 위한 AP를 **가져옵니다** .</span><span class="sxs-lookup"><span data-stu-id="8ca34-108">The **Get-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet deployes an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="8ca34-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8ca34-109">EXAMPLES</span></span>

### <span data-ttu-id="8ca34-110">예제 1: 모든 배포 일정 가져오기</span><span class="sxs-lookup"><span data-stu-id="8ca34-110">Example 1: Get all the deployment schedules</span></span>
```
PS C:\> Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01"

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : e347dfc4-62fe-4ed6-adfb-55518c57b558
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1
```

### <span data-ttu-id="8ca34-111">예제 2: 배포 일정 가져오기</span><span class="sxs-lookup"><span data-stu-id="8ca34-111">Example 2: Get a deployment schedule</span></span>
```
PS C:\> $js= Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule `
                 -AutomationAccountName "Contoso01" `
                 -ResourceGroupName "ResourceGroup01" `
                 -JobScheduleId 2b1d7738-093d-4ff7-b87b-e4b2321319e5

PS C:\> $js

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSche
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1

PS C:\> $js.JobSchedule

ResourceGroupName     : ResourceGroup01
RunOn                 :
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1
ScheduleName          : TestScheduleName
Parameters            : {AutomationAccountName, NodeConfigurationName, ResourceGroupName, ListOfNodeNames}
HybridWorker          :
```

<span data-ttu-id="8ca34-112">위의 명령은 노드 이름의 지정 된 2 차원 배열에 "Config01" 라는 DSC 노드 구성을 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ca34-112">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="8ca34-113">구축은 미리 준비 된 방식으로 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ca34-113">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="8ca34-114">변수</span><span class="sxs-lookup"><span data-stu-id="8ca34-114">PARAMETERS</span></span>

### <span data-ttu-id="8ca34-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8ca34-115">-AutomationAccountName</span></span>
<span data-ttu-id="8ca34-116">이 cmdlet이 컴파일하는 DSC 구성을 포함 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ca34-116">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="8ca34-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ca34-117">-DefaultProfile</span></span>
<span data-ttu-id="8ca34-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8ca34-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ca34-119">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="8ca34-119">-JobScheduleId</span></span>
<span data-ttu-id="8ca34-120">기존 예약 된 배포 작업의 작업 일정 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ca34-120">Specifies the Job Schedule id of an existing scheduled deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobScheduleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ca34-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ca34-121">-ResourceGroupName</span></span>
<span data-ttu-id="8ca34-122">이 cmdlet이 구성을 컴파일하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ca34-122">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="8ca34-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ca34-123">CommonParameters</span></span>
<span data-ttu-id="8ca34-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ca34-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ca34-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ca34-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ca34-126">입력</span><span class="sxs-lookup"><span data-stu-id="8ca34-126">INPUTS</span></span>

### <span data-ttu-id="8ca34-127">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="8ca34-127">System.Guid</span></span>

### <span data-ttu-id="8ca34-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8ca34-128">System.String</span></span>

## <span data-ttu-id="8ca34-129">출력</span><span class="sxs-lookup"><span data-stu-id="8ca34-129">OUTPUTS</span></span>

### <span data-ttu-id="8ca34-130">NodeConfigurationDeploymentSchedule를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="8ca34-130">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="8ca34-131">상속자</span><span class="sxs-lookup"><span data-stu-id="8ca34-131">NOTES</span></span>

## <span data-ttu-id="8ca34-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ca34-132">RELATED LINKS</span></span>

[<span data-ttu-id="8ca34-133">시작-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="8ca34-133">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="8ca34-134">가져오기-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ca34-134">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="8ca34-135">시작-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="8ca34-135">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="8ca34-136">중지-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="8ca34-136">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="8ca34-137">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="8ca34-137">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)
