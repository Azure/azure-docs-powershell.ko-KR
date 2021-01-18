---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 63e78c0068d17986f845adaae9dbc5caf22b4b4d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493502"
---
# <span data-ttu-id="3b1e6-101">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="3b1e6-101">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="3b1e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b1e6-102">SYNOPSIS</span></span>
<span data-ttu-id="3b1e6-103">Azure Data Factory에서 데이터 흐름 디버그 세션을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="3b1e6-103">Stops a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="3b1e6-104">구문</span><span class="sxs-lookup"><span data-stu-id="3b1e6-104">SYNTAX</span></span>

### <span data-ttu-id="3b1e6-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="3b1e6-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b1e6-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3b1e6-106">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b1e6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3b1e6-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b1e6-108">설명</span><span class="sxs-lookup"><span data-stu-id="3b1e6-108">DESCRIPTION</span></span>
<span data-ttu-id="3b1e6-109">이 명령은 디버그 세션을 중지합니다. 그렇지 않은 경우 디버그 세션의 Time To Live 설정에 따라 세션이 자동으로 해제됩니다.</span><span class="sxs-lookup"><span data-stu-id="3b1e6-109">This command stops the debug session, if not then the session will be automatically turned off according to Time To Live setting of the debug session.</span></span>

## <span data-ttu-id="3b1e6-110">예제</span><span class="sxs-lookup"><span data-stu-id="3b1e6-110">EXAMPLES</span></span>

### <span data-ttu-id="3b1e6-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3b1e6-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Stop-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d

Confirm
Are you sure you want to stop data flow debug session 'fd76cd0d-8b37-4dc0-a370-3f9d43ac686d' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```
<span data-ttu-id="3b1e6-112">데이터 팩터리 "WikiADF"에서 데이터 흐름 디버그 세션 "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d"를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="3b1e6-112">Stops a data flow debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WikiADF"</span></span>

## <span data-ttu-id="3b1e6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b1e6-113">PARAMETERS</span></span>

### <span data-ttu-id="3b1e6-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="3b1e6-114">-DataFactory</span></span>
<span data-ttu-id="3b1e6-115">데이터 팩터리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3b1e6-115">The data factory object.</span></span>

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

### <span data-ttu-id="3b1e6-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3b1e6-116">-DataFactoryName</span></span>
<span data-ttu-id="3b1e6-117">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b1e6-117">The data factory name.</span></span>

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

### <span data-ttu-id="3b1e6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b1e6-118">-DefaultProfile</span></span>
<span data-ttu-id="3b1e6-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3b1e6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b1e6-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b1e6-120">-PassThru</span></span>
<span data-ttu-id="3b1e6-121">지정된 경우 작업이 성공하는 경우 true를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="3b1e6-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="3b1e6-122">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="3b1e6-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="3b1e6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b1e6-123">-ResourceGroupName</span></span>
<span data-ttu-id="3b1e6-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b1e6-124">The resource group name.</span></span>

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

### <span data-ttu-id="3b1e6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b1e6-125">-ResourceId</span></span>
<span data-ttu-id="3b1e6-126">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3b1e6-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3b1e6-127">-SessionId</span><span class="sxs-lookup"><span data-stu-id="3b1e6-127">-SessionId</span></span>
<span data-ttu-id="3b1e6-128">데이터 흐름 디버그 세션 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3b1e6-128">The data flow debug session ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b1e6-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b1e6-129">-Confirm</span></span>
<span data-ttu-id="3b1e6-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3b1e6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b1e6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b1e6-131">-WhatIf</span></span>
<span data-ttu-id="3b1e6-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3b1e6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b1e6-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3b1e6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b1e6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b1e6-134">CommonParameters</span></span>
<span data-ttu-id="3b1e6-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3b1e6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b1e6-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3b1e6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b1e6-137">입력</span><span class="sxs-lookup"><span data-stu-id="3b1e6-137">INPUTS</span></span>

### <span data-ttu-id="3b1e6-138">System.String</span><span class="sxs-lookup"><span data-stu-id="3b1e6-138">System.String</span></span>

### <span data-ttu-id="3b1e6-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3b1e6-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="3b1e6-140">출력</span><span class="sxs-lookup"><span data-stu-id="3b1e6-140">OUTPUTS</span></span>

### <span data-ttu-id="3b1e6-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="3b1e6-141">System.Void</span></span>

### <span data-ttu-id="3b1e6-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3b1e6-142">System.Boolean</span></span>

## <span data-ttu-id="3b1e6-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3b1e6-143">NOTES</span></span>
<span data-ttu-id="3b1e6-144">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="3b1e6-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3b1e6-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3b1e6-145">RELATED LINKS</span></span>

[<span data-ttu-id="3b1e6-146">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="3b1e6-146">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="3b1e6-147">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="3b1e6-147">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="3b1e6-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="3b1e6-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="3b1e6-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="3b1e6-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)