---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/invoke-azdatafactoryv2dataflowdebugsessioncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
ms.openlocfilehash: e54823cc6dff1f58b594604841c1d37bf249b7ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975104"
---
# <span data-ttu-id="352f7-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="352f7-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>

## <span data-ttu-id="352f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="352f7-102">SYNOPSIS</span></span>
<span data-ttu-id="352f7-103">데이터 흐름 디버그 세션에서 디버그 작업을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="352f7-103">Invoke debug action in data flow debug session.</span></span>

## <span data-ttu-id="352f7-104">구문</span><span class="sxs-lookup"><span data-stu-id="352f7-104">SYNTAX</span></span>

### <span data-ttu-id="352f7-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="352f7-105">ByFactoryName (Default)</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="352f7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="352f7-106">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="352f7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="352f7-107">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="352f7-108">설명</span><span class="sxs-lookup"><span data-stu-id="352f7-108">DESCRIPTION</span></span>
<span data-ttu-id="352f7-109">이 명령은 디버그 세션에서 다양한 데이터 흐름 스트림에 대한 데이터 미리 보기/통계 미리 보기/식 미리 보기를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="352f7-109">This command executes data preview/stats preview/expression preview for different stream of data flow in debug session.</span></span>
<span data-ttu-id="352f7-110">데이터 흐름 디버그 워크플로에 대한 PowerShell 명령 시퀀스는 다음을 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="352f7-110">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="352f7-111">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="352f7-111">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="352f7-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="352f7-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="352f7-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand(다른 명령/대상에 대해 이 단계를 반복하거나 패키지 파일을 변경하기 위해 2-3단계를 반복)</span><span class="sxs-lookup"><span data-stu-id="352f7-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="352f7-114">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="352f7-114">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="352f7-115">예제</span><span class="sxs-lookup"><span data-stu-id="352f7-115">EXAMPLES</span></span>

### <span data-ttu-id="352f7-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="352f7-116">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> $result = Invoke-AzDataFactoryV2DataFlowDebugSessionCommand -ResourceGroupName adf -DataFactoryName WiKiADF -Command executePreviewQuery -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d -StreamName source1 -RowLimits 100 -AsJob
PS C:\WINDOWS\system32> $result

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
3      Long Running... AzureLongRun... Running       True            localhost            Invoke-AzDataFactoryV2...


(After 2 minutes)

PS C:\WINDOWS\system32> $result

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
3      Long Running... AzureLongRun... Completed     True            localhost            Invoke-AzDataFactoryV2...

PS C:\WINDOWS\system32> $output = ConvertFrom-Json($result.Output.Data)
PS C:\WINDOWS\system32> $output.output

    {
      "schema": "output(ResourceAgencyNum as string, PublicName as string)" ,
      "data": [["4445679354", "Syrian Refugee Information", 1], ["44456793", "Syrian Refugee Information", 1]]
    }


```

<span data-ttu-id="352f7-117">이 예제에서는 데이터 팩터리 "WiKiADF"에서 디버그 세션 "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d"에 대한 데이터 미리 보기 명령을 호출한 다음 JSON 출력을 읽을 수 있는 문자열로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="352f7-117">This example invokes data preview command for debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WiKiADF" and then convert the JSON output into readable string.</span></span>

## <span data-ttu-id="352f7-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="352f7-118">PARAMETERS</span></span>

### <span data-ttu-id="352f7-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="352f7-119">-AsJob</span></span>
<span data-ttu-id="352f7-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="352f7-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="352f7-121">-Columns</span><span class="sxs-lookup"><span data-stu-id="352f7-121">-Columns</span></span>
<span data-ttu-id="352f7-122">데이터 흐름 통계 미리 보기에 대한 열 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="352f7-122">The columns list for data flow statistics preview.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="352f7-123">-Command</span><span class="sxs-lookup"><span data-stu-id="352f7-123">-Command</span></span>
<span data-ttu-id="352f7-124">데이터 흐름 디버그 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="352f7-124">The data flow debug command.</span></span> <span data-ttu-id="352f7-125">선택 사항은PreviewQuery를 실행하고StatisticsQuery를 실행하고ExpressionQuery를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="352f7-125">Optionals are executePreviewQuery, executeStatisticsQuery and executeExpressionQuery</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="352f7-126">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="352f7-126">-DataFactory</span></span>
<span data-ttu-id="352f7-127">데이터 팩터리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="352f7-127">The data factory object.</span></span>

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

### <span data-ttu-id="352f7-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="352f7-128">-DataFactoryName</span></span>
<span data-ttu-id="352f7-129">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="352f7-129">The data factory name.</span></span>

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

### <span data-ttu-id="352f7-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="352f7-130">-DefaultProfile</span></span>
<span data-ttu-id="352f7-131">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="352f7-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="352f7-132">-식</span><span class="sxs-lookup"><span data-stu-id="352f7-132">-Expression</span></span>
<span data-ttu-id="352f7-133">데이터 흐름 식 미리 보기에 대한 식입니다.</span><span class="sxs-lookup"><span data-stu-id="352f7-133">The expression for data flow expression preview.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="352f7-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="352f7-134">-ResourceGroupName</span></span>
<span data-ttu-id="352f7-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="352f7-135">The resource group name.</span></span>

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

### <span data-ttu-id="352f7-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="352f7-136">-ResourceId</span></span>
<span data-ttu-id="352f7-137">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="352f7-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="352f7-138">-RowLimits</span><span class="sxs-lookup"><span data-stu-id="352f7-138">-RowLimits</span></span>
<span data-ttu-id="352f7-139">데이터 흐름 데이터 미리 보기의 행 제한입니다.</span><span class="sxs-lookup"><span data-stu-id="352f7-139">The row limit for data flow data preview.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="352f7-140">-SessionId</span><span class="sxs-lookup"><span data-stu-id="352f7-140">-SessionId</span></span>
<span data-ttu-id="352f7-141">데이터 흐름 디버그 세션 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="352f7-141">The data flow debug session ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="352f7-142">-StreamName</span><span class="sxs-lookup"><span data-stu-id="352f7-142">-StreamName</span></span>
<span data-ttu-id="352f7-143">디버깅을 위한 데이터 흐름의 스트림 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="352f7-143">The stream name of data flow for debugging.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="352f7-144">-확인</span><span class="sxs-lookup"><span data-stu-id="352f7-144">-Confirm</span></span>
<span data-ttu-id="352f7-145">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="352f7-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="352f7-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="352f7-146">-WhatIf</span></span>
<span data-ttu-id="352f7-147">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="352f7-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="352f7-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="352f7-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="352f7-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="352f7-149">CommonParameters</span></span>
<span data-ttu-id="352f7-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="352f7-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="352f7-151">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="352f7-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="352f7-152">입력</span><span class="sxs-lookup"><span data-stu-id="352f7-152">INPUTS</span></span>

### <span data-ttu-id="352f7-153">System.String</span><span class="sxs-lookup"><span data-stu-id="352f7-153">System.String</span></span>

### <span data-ttu-id="352f7-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="352f7-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="352f7-155">출력</span><span class="sxs-lookup"><span data-stu-id="352f7-155">OUTPUTS</span></span>

### <span data-ttu-id="352f7-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtaFlowDebugSessionCommandResult</span><span class="sxs-lookup"><span data-stu-id="352f7-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span></span>

## <span data-ttu-id="352f7-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="352f7-157">NOTES</span></span>
<span data-ttu-id="352f7-158">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리Keywords: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="352f7-158">Keywords: azure, azurerm, arm, resource, management, manager, data, factoriesKeywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="352f7-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="352f7-159">RELATED LINKS</span></span>

[<span data-ttu-id="352f7-160">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="352f7-160">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="352f7-161">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="352f7-161">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="352f7-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="352f7-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="352f7-163">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="352f7-163">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
