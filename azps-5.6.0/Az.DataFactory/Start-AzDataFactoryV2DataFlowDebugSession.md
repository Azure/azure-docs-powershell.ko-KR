---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/start-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: be94460a2296874acefab3232f4a73d394a523d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964912"
---
# <span data-ttu-id="7a874-101">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="7a874-101">Start-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="7a874-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a874-102">SYNOPSIS</span></span>
<span data-ttu-id="7a874-103">Azure Data Factory에서 데이터 흐름 디버그 세션 시작</span><span class="sxs-lookup"><span data-stu-id="7a874-103">Starts a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="7a874-104">구문</span><span class="sxs-lookup"><span data-stu-id="7a874-104">SYNTAX</span></span>

### <span data-ttu-id="7a874-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="7a874-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a874-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7a874-106">ByFactoryObject</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7a874-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7a874-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a874-108">설명</span><span class="sxs-lookup"><span data-stu-id="7a874-108">DESCRIPTION</span></span>
<span data-ttu-id="7a874-109">이 장기 실행 명령은 예정된 디버그 명령에 대한 데이터 흐름 디버그 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="7a874-109">This long running command starts a data flow debug session for the upcoming debug commands.</span></span> <span data-ttu-id="7a874-110">이 명령은 통합 런타임 정의와 연결하여 디버그 세션 클러스터의 크기/유형을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a874-110">This command can attach with an integration runtime definition to configure the size/type of debug session cluster.</span></span>
<span data-ttu-id="7a874-111">데이터 흐름 디버그 워크플로에 대한 PowerShell 명령 시퀀스는 다음을 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a874-111">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="7a874-112">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="7a874-112">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="7a874-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="7a874-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="7a874-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand(다른 명령/대상에 대해 이 단계를 반복하거나 패키지 파일을 변경하기 위해 2-3단계를 반복)</span><span class="sxs-lookup"><span data-stu-id="7a874-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="7a874-115">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="7a874-115">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="7a874-116">예제</span><span class="sxs-lookup"><span data-stu-id="7a874-116">EXAMPLES</span></span>

### <span data-ttu-id="7a874-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="7a874-117">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> $job = Start-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName jikma0601sea -AsJob
PS C:\WINDOWS\system32> $job 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Running       True            localhost            Start-AzDataFactoryV2D...

(After 5 minutes)

PS C:\WINDOWS\system32> $job

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Completed     True            localhost            Start-AzDataFactoryV2D...


PS C:\WINDOWS\system32> $job.Output

SessionId                            Status
---------                            ------
550effe4-93a3-485c-8525-eaf25259efbd Succeeded

```

<span data-ttu-id="7a874-118">AsJob 플래그로 디버그 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="7a874-118">Starts a debug session with AsJob flag.</span></span>

## <span data-ttu-id="7a874-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7a874-119">PARAMETERS</span></span>

### <span data-ttu-id="7a874-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a874-120">-AsJob</span></span>
<span data-ttu-id="7a874-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7a874-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a874-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="7a874-122">-DataFactory</span></span>
<span data-ttu-id="7a874-123">데이터 팩터리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7a874-123">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a874-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7a874-124">-DataFactoryName</span></span>
<span data-ttu-id="7a874-125">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a874-125">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a874-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a874-126">-DefaultProfile</span></span>
<span data-ttu-id="7a874-127">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a874-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a874-128">-IntegrationRuntimeFile</span><span class="sxs-lookup"><span data-stu-id="7a874-128">-IntegrationRuntimeFile</span></span>
<span data-ttu-id="7a874-129">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="7a874-129">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a874-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a874-130">-ResourceGroupName</span></span>
<span data-ttu-id="7a874-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a874-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a874-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a874-132">-ResourceId</span></span>
<span data-ttu-id="7a874-133">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7a874-133">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a874-134">-확인</span><span class="sxs-lookup"><span data-stu-id="7a874-134">-Confirm</span></span>
<span data-ttu-id="7a874-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a874-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a874-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a874-136">-WhatIf</span></span>
<span data-ttu-id="7a874-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7a874-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a874-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a874-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a874-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a874-139">CommonParameters</span></span>
<span data-ttu-id="7a874-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7a874-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a874-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a874-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a874-142">입력</span><span class="sxs-lookup"><span data-stu-id="7a874-142">INPUTS</span></span>

### <span data-ttu-id="7a874-143">System.String</span><span class="sxs-lookup"><span data-stu-id="7a874-143">System.String</span></span>

### <span data-ttu-id="7a874-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="7a874-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="7a874-145">출력</span><span class="sxs-lookup"><span data-stu-id="7a874-145">OUTPUTS</span></span>

### <span data-ttu-id="7a874-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="7a874-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span></span>

## <span data-ttu-id="7a874-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7a874-147">NOTES</span></span>
<span data-ttu-id="7a874-148">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="7a874-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7a874-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a874-149">RELATED LINKS</span></span>

[<span data-ttu-id="7a874-150">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="7a874-150">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="7a874-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="7a874-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="7a874-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="7a874-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="7a874-153">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="7a874-153">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)