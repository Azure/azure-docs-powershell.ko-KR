---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: e2800614e414a041073ae5396fb4b0e1e5833b59
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330345"
---
# <span data-ttu-id="0f880-101">Stop-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="0f880-101">Stop-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="0f880-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f880-102">SYNOPSIS</span></span>
<span data-ttu-id="0f880-103">데이터 팩터리에서 트리거 실행을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="0f880-103">Stops a trigger run in a data factory.</span></span>

## <span data-ttu-id="0f880-104">구문</span><span class="sxs-lookup"><span data-stu-id="0f880-104">SYNTAX</span></span>

### <span data-ttu-id="0f880-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="0f880-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f880-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0f880-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f880-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0f880-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0f880-108">설명</span><span class="sxs-lookup"><span data-stu-id="0f880-108">DESCRIPTION</span></span>
<span data-ttu-id="0f880-109">**Stop-AzDataFactoryV2TriggerRun** cmdlet은 트리거 이름 및 트리거 실행 ID로 지정된 데이터 팩터리에서 트리거 실행을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="0f880-109">The **Stop-AzDataFactoryV2TriggerRun** cmdlet stops a trigger run in a data factory specified with the trigger name and trigger run ID.</span></span>
<span data-ttu-id="0f880-110">현재 WaitingOnDependency 상태의 TumblingWindowTriggers에서만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f880-110">Currently only supported for TumblingWindowTriggers in WaitingOnDependency State.</span></span>

## <span data-ttu-id="0f880-111">예제</span><span class="sxs-lookup"><span data-stu-id="0f880-111">EXAMPLES</span></span>

### <span data-ttu-id="0f880-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="0f880-112">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```

<span data-ttu-id="0f880-113">이 명령은 팩터리 WikiADF에서 '085860024680058888497807248799CU16'으로 트리거 실행을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="0f880-113">This command stops the trigger run with id '08586002468005888497807248799CU16' in the factory WikiADF.</span></span>

## <span data-ttu-id="0f880-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f880-114">PARAMETERS</span></span>

### <span data-ttu-id="0f880-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0f880-115">-DataFactory</span></span>
<span data-ttu-id="0f880-116">데이터 팩터리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0f880-116">The data factory object.</span></span>

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

### <span data-ttu-id="0f880-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0f880-117">-DataFactoryName</span></span>
<span data-ttu-id="0f880-118">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0f880-118">The data factory name.</span></span>

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

### <span data-ttu-id="0f880-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f880-119">-DefaultProfile</span></span>
<span data-ttu-id="0f880-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0f880-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f880-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f880-121">-InputObject</span></span>
<span data-ttu-id="0f880-122">트리거 실행에 대한 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="0f880-122">The information about the trigger run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f880-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f880-123">-PassThru</span></span>
<span data-ttu-id="0f880-124">cmdlet을 지정한 경우 작업이 성공하는 경우 true를 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="0f880-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="0f880-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f880-125">-ResourceGroupName</span></span>
<span data-ttu-id="0f880-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0f880-126">The resource group name.</span></span>

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

### <span data-ttu-id="0f880-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="0f880-127">-TriggerName</span></span>
<span data-ttu-id="0f880-128">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0f880-128">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f880-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="0f880-129">-TriggerRunId</span></span>
<span data-ttu-id="0f880-130">트리거의 실행 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0f880-130">The Run ID of the trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f880-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f880-131">-Confirm</span></span>
<span data-ttu-id="0f880-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f880-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f880-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f880-133">-WhatIf</span></span>
<span data-ttu-id="0f880-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0f880-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f880-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0f880-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f880-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f880-136">CommonParameters</span></span>
<span data-ttu-id="0f880-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0f880-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f880-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0f880-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f880-139">입력</span><span class="sxs-lookup"><span data-stu-id="0f880-139">INPUTS</span></span>

### <span data-ttu-id="0f880-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="0f880-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="0f880-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0f880-141">System.String</span></span>

### <span data-ttu-id="0f880-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0f880-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="0f880-143">출력</span><span class="sxs-lookup"><span data-stu-id="0f880-143">OUTPUTS</span></span>

### <span data-ttu-id="0f880-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0f880-144">System.Boolean</span></span>

## <span data-ttu-id="0f880-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0f880-145">NOTES</span></span>

## <span data-ttu-id="0f880-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f880-146">RELATED LINKS</span></span>
