---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 889318c911ae6f34b3655583ea2e9693da3bf80f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531246"
---
# <span data-ttu-id="1fd18-101">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="1fd18-101">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="1fd18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fd18-102">SYNOPSIS</span></span>
<span data-ttu-id="1fd18-103">자동화에서 DSC 노드 구성 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1fd18-103">Gets DSC Node configuration deployments in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fd18-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1fd18-104">SYNTAX</span></span>

### <span data-ttu-id="1fd18-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="1fd18-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeployment [[-Status] <String>] [[-StartTime] <DateTimeOffset>]
 [[-EndTime] <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fd18-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="1fd18-106">ByJobId</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fd18-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1fd18-107">DESCRIPTION</span></span>
<span data-ttu-id="1fd18-108">AzureRmAutomationDscNodeConfigurationDeployment cmdlet은 Azure Automation의 DSC (원하는 상태 구성) 노드 구성을 위한 AP를 **가져옵니다** .</span><span class="sxs-lookup"><span data-stu-id="1fd18-108">The **Get-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet deployes an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="1fd18-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1fd18-109">EXAMPLES</span></span>

### <span data-ttu-id="1fd18-110">예제 1: 노드 구성 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="1fd18-110">Example 1: Get a node configuration deployment</span></span>
```
PS C:\> $deployment = Get-AzureRmAutomationDscNodeConfigurationDeployment `
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

<span data-ttu-id="1fd18-111">위의 명령은 노드 이름의 지정 된 2 차원 배열에 "Config01" 라는 DSC 노드 구성을 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fd18-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="1fd18-112">구축은 미리 준비 된 방식으로 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fd18-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="1fd18-113">변수</span><span class="sxs-lookup"><span data-stu-id="1fd18-113">PARAMETERS</span></span>

### <span data-ttu-id="1fd18-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="1fd18-114">-JobId</span></span>
<span data-ttu-id="1fd18-115">기존 배포 작업의 작업 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fd18-115">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="1fd18-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fd18-116">-ResourceGroupName</span></span>
<span data-ttu-id="1fd18-117">이 cmdlet이 구성을 컴파일하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fd18-117">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="1fd18-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1fd18-118">-AutomationAccountName</span></span>
<span data-ttu-id="1fd18-119">이 cmdlet이 컴파일하는 DSC 구성을 포함 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fd18-119">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="1fd18-120">-상태</span><span class="sxs-lookup"><span data-stu-id="1fd18-120">-Status</span></span>
<span data-ttu-id="1fd18-121">작업 필터의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="1fd18-121">Status of the Job filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fd18-122">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1fd18-122">-StartTime</span></span>
<span data-ttu-id="1fd18-123">시작 시간 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="1fd18-123">Start time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fd18-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="1fd18-124">-EndTime</span></span>
<span data-ttu-id="1fd18-125">종료 시간 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="1fd18-125">End time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fd18-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fd18-126">-DefaultProfile</span></span>
<span data-ttu-id="1fd18-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1fd18-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fd18-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fd18-128">CommonParameters</span></span>
<span data-ttu-id="1fd18-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fd18-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fd18-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fd18-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fd18-131">입력</span><span class="sxs-lookup"><span data-stu-id="1fd18-131">INPUTS</span></span>

## <span data-ttu-id="1fd18-132">출력</span><span class="sxs-lookup"><span data-stu-id="1fd18-132">OUTPUTS</span></span>

### <span data-ttu-id="1fd18-133">NodeConfigurationDeployment를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="1fd18-133">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="1fd18-134">상속자</span><span class="sxs-lookup"><span data-stu-id="1fd18-134">NOTES</span></span>

## <span data-ttu-id="1fd18-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1fd18-135">RELATED LINKS</span></span>

[<span data-ttu-id="1fd18-136">시작-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="1fd18-136">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="1fd18-137">가져오기-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fd18-137">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="1fd18-138">시작-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="1fd18-138">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="1fd18-139">중지-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="1fd18-139">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="1fd18-140">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="1fd18-140">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)
