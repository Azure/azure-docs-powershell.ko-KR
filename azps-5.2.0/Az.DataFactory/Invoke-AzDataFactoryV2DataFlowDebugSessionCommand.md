---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2dataflowdebugsessioncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
ms.openlocfilehash: 4009835b2efe8346ff873bde59870954c73ab5d7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371904"
---
# <span data-ttu-id="cc3e4-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="cc3e4-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>

## <span data-ttu-id="cc3e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc3e4-102">SYNOPSIS</span></span>
<span data-ttu-id="cc3e4-103">데이터 흐름 디버그 세션에서 디버그 작업을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="cc3e4-103">Invoke debug action in data flow debug session.</span></span>

## <span data-ttu-id="cc3e4-104">구문</span><span class="sxs-lookup"><span data-stu-id="cc3e4-104">SYNTAX</span></span>

### <span data-ttu-id="cc3e4-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="cc3e4-105">ByFactoryName (Default)</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc3e4-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cc3e4-106">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc3e4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cc3e4-107">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc3e4-108">설명</span><span class="sxs-lookup"><span data-stu-id="cc3e4-108">DESCRIPTION</span></span>
<span data-ttu-id="cc3e4-109">이 명령은 디버그 세션에서 다양한 데이터 흐름 스트림에 대한 데이터 미리 보기/통계 미리 보기/식 미리 보기를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="cc3e4-109">This command executes data preview/stats preview/expression preview for different stream of data flow in debug session.</span></span>
<span data-ttu-id="cc3e4-110">데이터 흐름 디버그 워크플로에 대한 PowerShell 명령 시퀀스는 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="cc3e4-110">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="cc3e4-111">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="cc3e4-111">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="cc3e4-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="cc3e4-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="cc3e4-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand(다른 명령/대상에 대해 이 단계를 반복하거나 패키지 파일을 변경하기 위해 2-3단계를 반복)</span><span class="sxs-lookup"><span data-stu-id="cc3e4-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="cc3e4-114">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="cc3e4-114">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="cc3e4-115">예제</span><span class="sxs-lookup"><span data-stu-id="cc3e4-115">EXAMPLES</span></span>

### <span data-ttu-id="cc3e4-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="cc3e4-116">Example 1</span></span>
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

<span data-ttu-id="cc3e4-117">이 예제에서는 데이터 팩터리 "WiKiADF"에서 디버그 세션 "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d"에 대한 데이터 미리 보기 명령을 호출한 다음 JSON 출력을 읽을 수 있는 문자열로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="cc3e4-117">This example invokes data preview command for debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WiKiADF" and then convert the JSON output into readable string.</span></span>

## <span data-ttu-id="cc3e4-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc3e4-118">PARAMETERS</span></span>

### <span data-ttu-id="cc3e4-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc3e4-119">-AsJob</span></span>
<span data-ttu-id="cc3e4-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="cc3e4-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc3e4-121">-Columns</span><span class="sxs-lookup"><span data-stu-id="cc3e4-121">-Columns</span></span>
<span data-ttu-id="cc3e4-122">데이터 흐름 통계 미리 보기에 대한 열 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="cc3e4-122">The columns list for data flow statistics preview.</span></span>

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

### <span data-ttu-id="cc3e4-123">-Command</span><span class="sxs-lookup"><span data-stu-id="cc3e4-123">-Command</span></span>
<span data-ttu-id="cc3e4-124">데이터 흐름 디버그 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="cc3e4-124">The data flow debug command.</span></span> <span data-ttu-id="cc3e4-125">선택 사항으로 executePreviewQuery, executeStatisticsQuery 및 executeExpressionQuery가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cc3e4-125">Optionals are executePreviewQuery, executeStatisticsQuery and executeExpressionQuery</span></span>

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

### <span data-ttu-id="cc3e4-126">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="cc3e4-126">-DataFactory</span></span>
<span data-ttu-id="cc3e4-127">데이터 팩터리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="cc3e4-127">The data factory object.</span></span>

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

### <span data-ttu-id="cc3e4-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cc3e4-128">-DataFactoryName</span></span>
<span data-ttu-id="cc3e4-129">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cc3e4-129">The data factory name.</span></span>

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

### <span data-ttu-id="cc3e4-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc3e4-130">-DefaultProfile</span></span>
<span data-ttu-id="cc3e4-131">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cc3e4-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc3e4-132">-Expression</span><span class="sxs-lookup"><span data-stu-id="cc3e4-132">-Expression</span></span>
<span data-ttu-id="cc3e4-133">데이터 흐름 식 미리 보기에 대한 식입니다.</span><span class="sxs-lookup"><span data-stu-id="cc3e4-133">The expression for data flow expression preview.</span></span>

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

### <span data-ttu-id="cc3e4-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc3e4-134">-ResourceGroupName</span></span>
<span data-ttu-id="cc3e4-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cc3e4-135">The resource group name.</span></span>

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

### <span data-ttu-id="cc3e4-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc3e4-136">-ResourceId</span></span>
<span data-ttu-id="cc3e4-137">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cc3e4-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="cc3e4-138">-RowLimits</span><span class="sxs-lookup"><span data-stu-id="cc3e4-138">-RowLimits</span></span>
<span data-ttu-id="cc3e4-139">데이터 흐름 데이터 미리 보기에 대한 행 제한입니다.</span><span class="sxs-lookup"><span data-stu-id="cc3e4-139">The row limit for data flow data preview.</span></span>

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

### <span data-ttu-id="cc3e4-140">-SessionId</span><span class="sxs-lookup"><span data-stu-id="cc3e4-140">-SessionId</span></span>
<span data-ttu-id="cc3e4-141">데이터 흐름 디버그 세션 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cc3e4-141">The data flow debug session ID.</span></span>

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

### <span data-ttu-id="cc3e4-142">-StreamName</span><span class="sxs-lookup"><span data-stu-id="cc3e4-142">-StreamName</span></span>
<span data-ttu-id="cc3e4-143">디버깅을 위한 데이터 흐름의 스트림 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cc3e4-143">The stream name of data flow for debugging.</span></span>

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

### <span data-ttu-id="cc3e4-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc3e4-144">-Confirm</span></span>
<span data-ttu-id="cc3e4-145">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc3e4-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc3e4-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc3e4-146">-WhatIf</span></span>
<span data-ttu-id="cc3e4-147">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="cc3e4-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc3e4-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cc3e4-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc3e4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc3e4-149">CommonParameters</span></span>
<span data-ttu-id="cc3e4-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cc3e4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc3e4-151">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cc3e4-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc3e4-152">입력</span><span class="sxs-lookup"><span data-stu-id="cc3e4-152">INPUTS</span></span>

### <span data-ttu-id="cc3e4-153">System.String</span><span class="sxs-lookup"><span data-stu-id="cc3e4-153">System.String</span></span>

### <span data-ttu-id="cc3e4-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="cc3e4-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="cc3e4-155">출력</span><span class="sxs-lookup"><span data-stu-id="cc3e4-155">OUTPUTS</span></span>

### <span data-ttu-id="cc3e4-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span><span class="sxs-lookup"><span data-stu-id="cc3e4-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span></span>

## <span data-ttu-id="cc3e4-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cc3e4-157">NOTES</span></span>
<span data-ttu-id="cc3e4-158">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, factoriesKeywords: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="cc3e4-158">Keywords: azure, azurerm, arm, resource, management, manager, data, factoriesKeywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="cc3e4-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cc3e4-159">RELATED LINKS</span></span>

[<span data-ttu-id="cc3e4-160">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="cc3e4-160">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="cc3e4-161">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="cc3e4-161">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="cc3e4-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="cc3e4-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="cc3e4-163">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="cc3e4-163">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
