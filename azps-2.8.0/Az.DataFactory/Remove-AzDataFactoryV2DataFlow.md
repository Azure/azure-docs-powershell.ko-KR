---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 69d666d2338658b108386da74040a4d30bcbbebb
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100396016"
---
# <span data-ttu-id="40d93-101">Remove-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="40d93-101">Remove-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="40d93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40d93-102">SYNOPSIS</span></span>
<span data-ttu-id="40d93-103">Data Factory에서 데이터 흐름을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="40d93-103">Removes a data flow from Data Factory.</span></span>

## <span data-ttu-id="40d93-104">구문</span><span class="sxs-lookup"><span data-stu-id="40d93-104">SYNTAX</span></span>

### <span data-ttu-id="40d93-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="40d93-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="40d93-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="40d93-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2DataFlow [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40d93-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="40d93-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Force] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40d93-108">설명</span><span class="sxs-lookup"><span data-stu-id="40d93-108">DESCRIPTION</span></span>
<span data-ttu-id="40d93-109">이 Remove-AzDataFactoryV2DataFlow cmdlet은 Azure Data Factory에서 데이터 흐름을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="40d93-109">The Remove-AzDataFactoryV2DataFlow cmdlet removes a data flow from Azure Data Factory.</span></span>

## <span data-ttu-id="40d93-110">예제</span><span class="sxs-lookup"><span data-stu-id="40d93-110">EXAMPLES</span></span>

### <span data-ttu-id="40d93-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="40d93-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Remove-AzDataFactoryV2DataFlow -ResourceGroupName adf -DataFactoryName WikiADF -DataFlowName "dataflow5"

Confirm
Are you sure you want to remove data flow 'dataflow5' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\WINDOWS\system32>
```

<span data-ttu-id="40d93-112">이 명령은 WikiADF라는 데이터 팩터리에서 dataflow5라는 데이터 흐름을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="40d93-112">This command removes the data flow named dataflow5 from the data factory named WikiADF.</span></span>

## <span data-ttu-id="40d93-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40d93-113">PARAMETERS</span></span>

### <span data-ttu-id="40d93-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="40d93-114">-DataFactoryName</span></span>
<span data-ttu-id="40d93-115">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40d93-115">The data factory name.</span></span>

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

### <span data-ttu-id="40d93-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40d93-116">-DefaultProfile</span></span>
<span data-ttu-id="40d93-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="40d93-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40d93-118">-Force</span><span class="sxs-lookup"><span data-stu-id="40d93-118">-Force</span></span>
<span data-ttu-id="40d93-119">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="40d93-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="40d93-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40d93-120">-InputObject</span></span>
<span data-ttu-id="40d93-121">데이터 흐름 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="40d93-121">The data flow object.</span></span>

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

### <span data-ttu-id="40d93-122">-Name</span><span class="sxs-lookup"><span data-stu-id="40d93-122">-Name</span></span>
<span data-ttu-id="40d93-123">데이터 흐름 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40d93-123">The data flow name.</span></span>

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

### <span data-ttu-id="40d93-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40d93-124">-ResourceGroupName</span></span>
<span data-ttu-id="40d93-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40d93-125">The resource group name.</span></span>

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

### <span data-ttu-id="40d93-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40d93-126">-ResourceId</span></span>
<span data-ttu-id="40d93-127">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="40d93-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="40d93-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40d93-128">-PassThru</span></span>
<span data-ttu-id="40d93-129">지정된 경우 작업이 성공하는 경우 true를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="40d93-129">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="40d93-130">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="40d93-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="40d93-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40d93-131">-Confirm</span></span>
<span data-ttu-id="40d93-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="40d93-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40d93-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40d93-133">-WhatIf</span></span>
<span data-ttu-id="40d93-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="40d93-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40d93-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="40d93-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40d93-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d93-136">CommonParameters</span></span>
<span data-ttu-id="40d93-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="40d93-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d93-138">자세한 내용은 [다음](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="40d93-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d93-139">입력</span><span class="sxs-lookup"><span data-stu-id="40d93-139">INPUTS</span></span>

### <span data-ttu-id="40d93-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="40d93-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="40d93-141">System.String</span><span class="sxs-lookup"><span data-stu-id="40d93-141">System.String</span></span>

## <span data-ttu-id="40d93-142">출력</span><span class="sxs-lookup"><span data-stu-id="40d93-142">OUTPUTS</span></span>

### <span data-ttu-id="40d93-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="40d93-143">System.Void</span></span>

### <span data-ttu-id="40d93-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="40d93-144">System.Boolean</span></span>

## <span data-ttu-id="40d93-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="40d93-145">NOTES</span></span>
<span data-ttu-id="40d93-146">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="40d93-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="40d93-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40d93-147">RELATED LINKS</span></span>



