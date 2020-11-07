---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 74966351f50be86f19441edc254af227f2e17fab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701625"
---
# <span data-ttu-id="20d87-101">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="20d87-101">Get-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="20d87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20d87-102">SYNOPSIS</span></span>
<span data-ttu-id="20d87-103">자동화에서 DSC 노드 구성 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="20d87-103">Gets DSC Node configuration deployments in Automation.</span></span>

## <span data-ttu-id="20d87-104">구문과</span><span class="sxs-lookup"><span data-stu-id="20d87-104">SYNTAX</span></span>

### <span data-ttu-id="20d87-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="20d87-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20d87-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="20d87-106">ByJobId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20d87-107">설명은</span><span class="sxs-lookup"><span data-stu-id="20d87-107">DESCRIPTION</span></span>
<span data-ttu-id="20d87-108">AzAutomationDscNodeConfigurationDeployment cmdlet은 Azure Automation의 DSC (원하는 상태 구성) 노드 구성을 위한 AP를 **가져옵니다** .</span><span class="sxs-lookup"><span data-stu-id="20d87-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deployes an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="20d87-109">예제의</span><span class="sxs-lookup"><span data-stu-id="20d87-109">EXAMPLES</span></span>

### <span data-ttu-id="20d87-110">예제 1: 노드 구성 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="20d87-110">Example 1: Get a node configuration deployment</span></span>
```
PS C:\> $deployment = Get-AzAutomationDscNodeConfigurationDeployment `
                         -JobId 35b14eb4-52b7-4a1d-ad62-8e9f84adc657 `
                         -AutomationAccountName "Contoso01"  `
                         -ResourceGroupName "ResourceGroup01" `
            
ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 35b14eb4-52b7-4a1d-ad62-8e9f84adc657
Job                   : Microsoft.Azure.Commands.Automation.Model.Job
JobStatus             : Running
NodeStatus            : {System.Collections.Generic.Dictionary`2[System.String,System.String], System.Collections.Generic.Dictionary`2[System.String,System.String]}
NodeConfigurationName : Config01.Node1
JobSchedule           :
JobScheduleId         : 00000000-0000-0000-0000-000000000000

PS C:\> $deployment | Select -expand nodeStatus

Key        Value
---        -----
WebServer  Pending
WebServer2 Pending
WebServer3 Compliant
```

<span data-ttu-id="20d87-111">위의 명령은 노드 이름의 지정 된 2 차원 배열에 "Config01" 라는 DSC 노드 구성을 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="20d87-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="20d87-112">구축은 미리 준비 된 방식으로 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="20d87-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="20d87-113">변수</span><span class="sxs-lookup"><span data-stu-id="20d87-113">PARAMETERS</span></span>

### <span data-ttu-id="20d87-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="20d87-114">-AutomationAccountName</span></span>
<span data-ttu-id="20d87-115">이 cmdlet이 컴파일하는 DSC 구성을 포함 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20d87-115">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="20d87-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20d87-116">-DefaultProfile</span></span>
<span data-ttu-id="20d87-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="20d87-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20d87-118">-EndTime</span><span class="sxs-lookup"><span data-stu-id="20d87-118">-EndTime</span></span>
<span data-ttu-id="20d87-119">종료 시간 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="20d87-119">End time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20d87-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="20d87-120">-JobId</span></span>
<span data-ttu-id="20d87-121">기존 배포 작업의 작업 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20d87-121">Specifies the Job id of an existing deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20d87-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20d87-122">-ResourceGroupName</span></span>
<span data-ttu-id="20d87-123">이 cmdlet이 구성을 컴파일하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20d87-123">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="20d87-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="20d87-124">-StartTime</span></span>
<span data-ttu-id="20d87-125">시작 시간 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="20d87-125">Start time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20d87-126">-상태</span><span class="sxs-lookup"><span data-stu-id="20d87-126">-Status</span></span>
<span data-ttu-id="20d87-127">작업 필터의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="20d87-127">Status of the Job filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20d87-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20d87-128">CommonParameters</span></span>
<span data-ttu-id="20d87-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="20d87-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20d87-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20d87-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20d87-131">입력</span><span class="sxs-lookup"><span data-stu-id="20d87-131">INPUTS</span></span>

### <span data-ttu-id="20d87-132">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="20d87-132">System.Guid</span></span>

### <span data-ttu-id="20d87-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="20d87-133">System.String</span></span>

## <span data-ttu-id="20d87-134">출력</span><span class="sxs-lookup"><span data-stu-id="20d87-134">OUTPUTS</span></span>

### <span data-ttu-id="20d87-135">NodeConfigurationDeployment를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="20d87-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="20d87-136">상속자</span><span class="sxs-lookup"><span data-stu-id="20d87-136">NOTES</span></span>

## <span data-ttu-id="20d87-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20d87-137">RELATED LINKS</span></span>

[<span data-ttu-id="20d87-138">시작-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="20d87-138">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="20d87-139">가져오기-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="20d87-139">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="20d87-140">시작-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="20d87-140">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="20d87-141">중지-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="20d87-141">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="20d87-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="20d87-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
