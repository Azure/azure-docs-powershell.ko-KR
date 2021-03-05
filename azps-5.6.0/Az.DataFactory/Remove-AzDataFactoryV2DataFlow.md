---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 66f5cf02c4f50c699f790ec2790080fa37ab166d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009184"
---
# <span data-ttu-id="bb282-101">Remove-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="bb282-101">Remove-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="bb282-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb282-102">SYNOPSIS</span></span>
<span data-ttu-id="bb282-103">Data Factory에서 데이터 흐름을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bb282-103">Removes a data flow from Data Factory.</span></span>

## <span data-ttu-id="bb282-104">구문</span><span class="sxs-lookup"><span data-stu-id="bb282-104">SYNTAX</span></span>

### <span data-ttu-id="bb282-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="bb282-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb282-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bb282-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2DataFlow [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb282-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bb282-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Force] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb282-108">설명</span><span class="sxs-lookup"><span data-stu-id="bb282-108">DESCRIPTION</span></span>
<span data-ttu-id="bb282-109">Remove-AzDataFactoryV2DataFlow cmdlet은 Azure Data Factory에서 데이터 흐름을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bb282-109">The Remove-AzDataFactoryV2DataFlow cmdlet removes a data flow from Azure Data Factory.</span></span>

## <span data-ttu-id="bb282-110">예제</span><span class="sxs-lookup"><span data-stu-id="bb282-110">EXAMPLES</span></span>

### <span data-ttu-id="bb282-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="bb282-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Remove-AzDataFactoryV2DataFlow -ResourceGroupName adf -DataFactoryName WikiADF -DataFlowName "dataflow5"

Confirm
Are you sure you want to remove data flow 'dataflow5' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\WINDOWS\system32>
```

<span data-ttu-id="bb282-112">이 명령은 WikiADF라는 데이터 팩터리에서 dataflow5라는 데이터 흐름을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bb282-112">This command removes the data flow named dataflow5 from the data factory named WikiADF.</span></span>

## <span data-ttu-id="bb282-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bb282-113">PARAMETERS</span></span>

### <span data-ttu-id="bb282-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="bb282-114">-DataFactoryName</span></span>
<span data-ttu-id="bb282-115">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb282-115">The data factory name.</span></span>

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

### <span data-ttu-id="bb282-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb282-116">-DefaultProfile</span></span>
<span data-ttu-id="bb282-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bb282-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb282-118">-Force</span><span class="sxs-lookup"><span data-stu-id="bb282-118">-Force</span></span>
<span data-ttu-id="bb282-119">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bb282-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="bb282-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb282-120">-InputObject</span></span>
<span data-ttu-id="bb282-121">데이터 흐름 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="bb282-121">The data flow object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb282-122">-Name</span><span class="sxs-lookup"><span data-stu-id="bb282-122">-Name</span></span>
<span data-ttu-id="bb282-123">데이터 흐름 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb282-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFlowName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb282-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb282-124">-ResourceGroupName</span></span>
<span data-ttu-id="bb282-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb282-125">The resource group name.</span></span>

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

### <span data-ttu-id="bb282-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb282-126">-ResourceId</span></span>
<span data-ttu-id="bb282-127">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bb282-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="bb282-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb282-128">-PassThru</span></span>
<span data-ttu-id="bb282-129">지정한 경우 작업이 성공할 경우 true를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="bb282-129">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="bb282-130">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="bb282-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="bb282-131">-확인</span><span class="sxs-lookup"><span data-stu-id="bb282-131">-Confirm</span></span>
<span data-ttu-id="bb282-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bb282-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb282-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb282-133">-WhatIf</span></span>
<span data-ttu-id="bb282-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="bb282-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb282-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bb282-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb282-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb282-136">CommonParameters</span></span>
<span data-ttu-id="bb282-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bb282-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb282-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb282-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb282-139">입력</span><span class="sxs-lookup"><span data-stu-id="bb282-139">INPUTS</span></span>

### <span data-ttu-id="bb282-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="bb282-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="bb282-141">System.String</span><span class="sxs-lookup"><span data-stu-id="bb282-141">System.String</span></span>

## <span data-ttu-id="bb282-142">출력</span><span class="sxs-lookup"><span data-stu-id="bb282-142">OUTPUTS</span></span>

### <span data-ttu-id="bb282-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="bb282-143">System.Void</span></span>

### <span data-ttu-id="bb282-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bb282-144">System.Boolean</span></span>

## <span data-ttu-id="bb282-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bb282-145">NOTES</span></span>
<span data-ttu-id="bb282-146">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="bb282-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="bb282-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb282-147">RELATED LINKS</span></span>

[<span data-ttu-id="bb282-148">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="bb282-148">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="bb282-149">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="bb282-149">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

