---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 63e78c0068d17986f845adaae9dbc5caf22b4b4d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355046"
---
# <span data-ttu-id="1cb47-101">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="1cb47-101">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="1cb47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cb47-102">SYNOPSIS</span></span>
<span data-ttu-id="1cb47-103">Azure Data Factory에서 데이터 흐름 디버그 세션을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="1cb47-103">Stops a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="1cb47-104">구문</span><span class="sxs-lookup"><span data-stu-id="1cb47-104">SYNTAX</span></span>

### <span data-ttu-id="1cb47-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="1cb47-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1cb47-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1cb47-106">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cb47-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1cb47-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cb47-108">설명</span><span class="sxs-lookup"><span data-stu-id="1cb47-108">DESCRIPTION</span></span>
<span data-ttu-id="1cb47-109">이 명령은 디버그 세션을 중지합니다. 그렇지 않은 경우 디버그 세션의 Time To Live 설정에 따라 세션이 자동으로 해제됩니다.</span><span class="sxs-lookup"><span data-stu-id="1cb47-109">This command stops the debug session, if not then the session will be automatically turned off according to Time To Live setting of the debug session.</span></span>

## <span data-ttu-id="1cb47-110">예제</span><span class="sxs-lookup"><span data-stu-id="1cb47-110">EXAMPLES</span></span>

### <span data-ttu-id="1cb47-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="1cb47-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Stop-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d

Confirm
Are you sure you want to stop data flow debug session 'fd76cd0d-8b37-4dc0-a370-3f9d43ac686d' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```
<span data-ttu-id="1cb47-112">데이터 팩터리 "WikiADF"에서 데이터 흐름 디버그 세션 "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d"를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="1cb47-112">Stops a data flow debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WikiADF"</span></span>

## <span data-ttu-id="1cb47-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1cb47-113">PARAMETERS</span></span>

### <span data-ttu-id="1cb47-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1cb47-114">-DataFactory</span></span>
<span data-ttu-id="1cb47-115">데이터 팩터리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1cb47-115">The data factory object.</span></span>

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

### <span data-ttu-id="1cb47-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1cb47-116">-DataFactoryName</span></span>
<span data-ttu-id="1cb47-117">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cb47-117">The data factory name.</span></span>

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

### <span data-ttu-id="1cb47-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cb47-118">-DefaultProfile</span></span>
<span data-ttu-id="1cb47-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1cb47-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cb47-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1cb47-120">-PassThru</span></span>
<span data-ttu-id="1cb47-121">지정된 경우 작업이 성공하는 경우 true를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="1cb47-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="1cb47-122">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1cb47-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="1cb47-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cb47-123">-ResourceGroupName</span></span>
<span data-ttu-id="1cb47-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cb47-124">The resource group name.</span></span>

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

### <span data-ttu-id="1cb47-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1cb47-125">-ResourceId</span></span>
<span data-ttu-id="1cb47-126">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1cb47-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1cb47-127">-SessionId</span><span class="sxs-lookup"><span data-stu-id="1cb47-127">-SessionId</span></span>
<span data-ttu-id="1cb47-128">데이터 흐름 디버그 세션 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1cb47-128">The data flow debug session ID.</span></span>

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

### <span data-ttu-id="1cb47-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1cb47-129">-Confirm</span></span>
<span data-ttu-id="1cb47-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1cb47-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cb47-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cb47-131">-WhatIf</span></span>
<span data-ttu-id="1cb47-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1cb47-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cb47-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1cb47-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cb47-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cb47-134">CommonParameters</span></span>
<span data-ttu-id="1cb47-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1cb47-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cb47-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1cb47-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cb47-137">입력</span><span class="sxs-lookup"><span data-stu-id="1cb47-137">INPUTS</span></span>

### <span data-ttu-id="1cb47-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1cb47-138">System.String</span></span>

### <span data-ttu-id="1cb47-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1cb47-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="1cb47-140">출력</span><span class="sxs-lookup"><span data-stu-id="1cb47-140">OUTPUTS</span></span>

### <span data-ttu-id="1cb47-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="1cb47-141">System.Void</span></span>

### <span data-ttu-id="1cb47-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1cb47-142">System.Boolean</span></span>

## <span data-ttu-id="1cb47-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1cb47-143">NOTES</span></span>
<span data-ttu-id="1cb47-144">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="1cb47-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1cb47-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1cb47-145">RELATED LINKS</span></span>

[<span data-ttu-id="1cb47-146">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="1cb47-146">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="1cb47-147">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="1cb47-147">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="1cb47-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="1cb47-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="1cb47-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="1cb47-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)