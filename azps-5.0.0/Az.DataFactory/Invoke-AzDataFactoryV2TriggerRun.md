---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: af0fcf4e96d919c2c52a2ab30e583f288d20fc4e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306209"
---
# <span data-ttu-id="6d386-101">Invoke-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="6d386-101">Invoke-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="6d386-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d386-102">SYNOPSIS</span></span>
 <span data-ttu-id="6d386-103">트리거 실행의 다른 인스턴스를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d386-103">Invokes another instance of a trigger run.</span></span>

## <span data-ttu-id="6d386-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6d386-104">SYNTAX</span></span>

### <span data-ttu-id="6d386-105">ByFactoryNameByParameterFile (기본값)</span><span class="sxs-lookup"><span data-stu-id="6d386-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6d386-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6d386-106">ByInputObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d386-107">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="6d386-107">ByFactoryName</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d386-108">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6d386-108">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d386-109">설명은</span><span class="sxs-lookup"><span data-stu-id="6d386-109">DESCRIPTION</span></span>
<span data-ttu-id="6d386-110">**AzDataFactoryV2TriggerRun** 명령은 새 트리거 실행 id를 사용 하 여 실행 되는 트리거의 다른 인스턴스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d386-110">The **Invoke-AzDataFactoryV2TriggerRun** command starts another instance of a trigger run with a new trigger run id.</span></span>

## <span data-ttu-id="6d386-111">예제의</span><span class="sxs-lookup"><span data-stu-id="6d386-111">EXAMPLES</span></span>

### <span data-ttu-id="6d386-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="6d386-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```
<span data-ttu-id="6d386-113">새 트리거 실행 id를 사용 하 여 트리거를 실행 하는 다른 인스턴스를 시작 하 고 원래 트리거로 실행 되는 동일한 windowStartTime 및 Windowstarttime을 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d386-113">Starts another instance of a trigger run with a new trigger run id, keeping the same windowStartTime and windowEndTime as the original trigger run.</span></span>

## <span data-ttu-id="6d386-114">변수</span><span class="sxs-lookup"><span data-stu-id="6d386-114">PARAMETERS</span></span>

### <span data-ttu-id="6d386-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6d386-115">-DataFactory</span></span>
<span data-ttu-id="6d386-116">Data factory 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6d386-116">The data factory object.</span></span>

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

### <span data-ttu-id="6d386-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6d386-117">-DataFactoryName</span></span>
<span data-ttu-id="6d386-118">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d386-118">The data factory name.</span></span>

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

### <span data-ttu-id="6d386-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d386-119">-DefaultProfile</span></span>
<span data-ttu-id="6d386-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6d386-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d386-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d386-121">-InputObject</span></span>
<span data-ttu-id="6d386-122">트리거 실행에 대 한 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="6d386-122">The information about the trigger run.</span></span>

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

### <span data-ttu-id="6d386-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d386-123">-PassThru</span></span>
<span data-ttu-id="6d386-124">지정 된 경우 cmdlet 쓰기 true를 대/소문자 구분 작업에 성공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d386-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="6d386-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d386-125">-ResourceGroupName</span></span>
<span data-ttu-id="6d386-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d386-126">The resource group name.</span></span>

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

### <span data-ttu-id="6d386-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="6d386-127">-TriggerName</span></span>
<span data-ttu-id="6d386-128">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d386-128">The trigger name.</span></span>

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

### <span data-ttu-id="6d386-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="6d386-129">-TriggerRunId</span></span>
<span data-ttu-id="6d386-130">트리거의 실행 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6d386-130">The Run ID of the trigger.</span></span>

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

### <span data-ttu-id="6d386-131">-확인</span><span class="sxs-lookup"><span data-stu-id="6d386-131">-Confirm</span></span>
<span data-ttu-id="6d386-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d386-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d386-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d386-133">-WhatIf</span></span>
<span data-ttu-id="6d386-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6d386-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d386-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d386-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d386-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d386-136">CommonParameters</span></span>
<span data-ttu-id="6d386-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d386-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d386-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6d386-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d386-139">입력</span><span class="sxs-lookup"><span data-stu-id="6d386-139">INPUTS</span></span>

### <span data-ttu-id="6d386-140">DataFactoryV2. PSTriggerRun/.</span><span class="sxs-lookup"><span data-stu-id="6d386-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="6d386-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6d386-141">System.String</span></span>

### <span data-ttu-id="6d386-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6d386-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="6d386-143">출력</span><span class="sxs-lookup"><span data-stu-id="6d386-143">OUTPUTS</span></span>

### <span data-ttu-id="6d386-144">DataFactoryV2. PSPipeline/.</span><span class="sxs-lookup"><span data-stu-id="6d386-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="6d386-145">상속자</span><span class="sxs-lookup"><span data-stu-id="6d386-145">NOTES</span></span>

## <span data-ttu-id="6d386-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d386-146">RELATED LINKS</span></span>
