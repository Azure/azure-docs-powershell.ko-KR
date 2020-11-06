---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 3ddaf0d4ae609305bf9740fbbe38a5fddd414e18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535504"
---
# <span data-ttu-id="e5fd8-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="e5fd8-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="e5fd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5fd8-102">SYNOPSIS</span></span>
<span data-ttu-id="e5fd8-103">자동화에서 DSC 노드 구성 배포를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="e5fd8-104">현재 배포 작업만 중지 하 고 이미 할당 된 노드 구성을 할당 취소 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5fd8-105">구문과</span><span class="sxs-lookup"><span data-stu-id="e5fd8-105">SYNTAX</span></span>

### <span data-ttu-id="e5fd8-106">ByJobId (기본값)</span><span class="sxs-lookup"><span data-stu-id="e5fd8-106">ByJobId (Default)</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> -AutomationAccountName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5fd8-107">ByByInputObject</span><span class="sxs-lookup"><span data-stu-id="e5fd8-107">ByByInputObject</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> -AutomationAccountName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5fd8-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e5fd8-108">DESCRIPTION</span></span>
<span data-ttu-id="e5fd8-109">**AzureRmAutomationDscNodeConfigurationDeployment** Cmdlet은 Azure AUTOMATION의 DSC (원하는 상태 구성) 노드 구성 배포를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-109">The **Stop-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="e5fd8-110">할당할 항목이 남아 있지만 이미 할당 된 노드를 할당 취소 하지 않는 경우 노드 그룹에 대 한 노드 구성 할당을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="e5fd8-111">예약 된 작업의 등록을 취소 하려면 JobScheduleId와 함께 AzureRmAutomationScheduledRunbook를 사용 하 여 현재 예약 된 작업의 할당을 [취소](./Unregister-AzureRmAutomationScheduledRunbook.md) 하세요.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-111">To unregister a scheduled job, please use the [Unregister-AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="e5fd8-112">예제의</span><span class="sxs-lookup"><span data-stu-id="e5fd8-112">EXAMPLES</span></span>

### <span data-ttu-id="e5fd8-113">예제 1: 자동화에서 Azure DSC 노드 구성 배포</span><span class="sxs-lookup"><span data-stu-id="e5fd8-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzureRmAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="e5fd8-114">위 명령에서는 전달 된 jobId를 사용 하 여 DSC 노드 구성 배포 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="e5fd8-115">변수</span><span class="sxs-lookup"><span data-stu-id="e5fd8-115">PARAMETERS</span></span>

### <span data-ttu-id="e5fd8-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e5fd8-116">-AutomationAccountName</span></span>
<span data-ttu-id="e5fd8-117">이 cmdlet이 컴파일하는 DSC 구성을 포함 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5fd8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5fd8-118">-ResourceGroupName</span></span>
<span data-ttu-id="e5fd8-119">이 cmdlet이 구성을 컴파일하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-119">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="e5fd8-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="e5fd8-120">-JobId</span></span>
<span data-ttu-id="e5fd8-121">기존 배포 작업의 작업 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-121">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="e5fd8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5fd8-122">-PassThru</span></span>
<span data-ttu-id="e5fd8-123">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e5fd8-124">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e5fd8-125">-Force</span><span class="sxs-lookup"><span data-stu-id="e5fd8-125">-Force</span></span>
<span data-ttu-id="e5fd8-126">ps_force</span><span class="sxs-lookup"><span data-stu-id="e5fd8-126">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByJobId
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5fd8-127">-확인</span><span class="sxs-lookup"><span data-stu-id="e5fd8-127">-Confirm</span></span>
<span data-ttu-id="e5fd8-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5fd8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5fd8-129">-WhatIf</span></span>
<span data-ttu-id="e5fd8-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5fd8-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5fd8-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5fd8-132">-DefaultProfile</span></span>
<span data-ttu-id="e5fd8-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5fd8-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5fd8-134">-InputObject</span></span>
<span data-ttu-id="e5fd8-135">파이프에 대 한 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-135">Input object for Piping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment
Parameter Sets: ByByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5fd8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5fd8-136">CommonParameters</span></span>
<span data-ttu-id="e5fd8-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5fd8-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5fd8-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5fd8-139">입력</span><span class="sxs-lookup"><span data-stu-id="e5fd8-139">INPUTS</span></span>

## <span data-ttu-id="e5fd8-140">출력</span><span class="sxs-lookup"><span data-stu-id="e5fd8-140">OUTPUTS</span></span>

## <span data-ttu-id="e5fd8-141">상속자</span><span class="sxs-lookup"><span data-stu-id="e5fd8-141">NOTES</span></span>

## <span data-ttu-id="e5fd8-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5fd8-142">RELATED LINKS</span></span>

[<span data-ttu-id="e5fd8-143">시작-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="e5fd8-143">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="e5fd8-144">가져오기-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5fd8-144">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="e5fd8-145">시작-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="e5fd8-145">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="e5fd8-146">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="e5fd8-146">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="e5fd8-147">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="e5fd8-147">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)
