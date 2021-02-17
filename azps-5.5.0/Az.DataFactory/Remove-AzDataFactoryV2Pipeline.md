---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: b1d39c3d60d043485cc4ec4dc0c4ba986a97e800
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186249"
---
# <span data-ttu-id="ac390-101">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="ac390-101">Remove-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="ac390-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac390-102">SYNOPSIS</span></span>
<span data-ttu-id="ac390-103">Data Factory에서 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ac390-103">Removes a pipeline from Data Factory.</span></span>

## <span data-ttu-id="ac390-104">구문</span><span class="sxs-lookup"><span data-stu-id="ac390-104">SYNTAX</span></span>

### <span data-ttu-id="ac390-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="ac390-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac390-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ac390-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac390-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ac390-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac390-108">설명</span><span class="sxs-lookup"><span data-stu-id="ac390-108">DESCRIPTION</span></span>
<span data-ttu-id="ac390-109">이 Remove-AzDataFactoryV2Pipeline cmdlet은 Azure Data Factory에서 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ac390-109">The Remove-AzDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="ac390-110">예제</span><span class="sxs-lookup"><span data-stu-id="ac390-110">EXAMPLES</span></span>

### <span data-ttu-id="ac390-111">예제 1: 파이프라인 제거</span><span class="sxs-lookup"><span data-stu-id="ac390-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="ac390-112">이 cmdlet은 WikiADF라는 데이터 팩터리에서 DPWikisample이라는 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ac390-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="ac390-113">이 명령은 10진수의 $True.</span><span class="sxs-lookup"><span data-stu-id="ac390-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="ac390-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac390-114">PARAMETERS</span></span>

### <span data-ttu-id="ac390-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ac390-115">-DataFactoryName</span></span>
<span data-ttu-id="ac390-116">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ac390-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ac390-117">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에서 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ac390-117">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ac390-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac390-118">-DefaultProfile</span></span>
<span data-ttu-id="ac390-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ac390-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac390-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ac390-120">-Force</span></span>
<span data-ttu-id="ac390-121">확인 메시지를 표시하지 않고 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ac390-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ac390-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac390-122">-InputObject</span></span>
<span data-ttu-id="ac390-123">파이프라인 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ac390-123">Specifies a Pipeline object.</span></span>
<span data-ttu-id="ac390-124">이 cmdlet은 이 매개 변수가 지정하는 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ac390-124">This cmdlet removes the pipeline that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac390-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ac390-125">-Name</span></span>
<span data-ttu-id="ac390-126">제거할 파이프라인의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ac390-126">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac390-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac390-127">-ResourceGroupName</span></span>
<span data-ttu-id="ac390-128">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ac390-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ac390-129">이 cmdlet은 이 매개 변수가 지정하는 그룹에서 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ac390-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ac390-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac390-130">-ResourceId</span></span>
<span data-ttu-id="ac390-131">제거할 파이프라인의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ac390-131">The Azure resource ID of the pipeline to remove.</span></span>

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

### <span data-ttu-id="ac390-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac390-132">-Confirm</span></span>
<span data-ttu-id="ac390-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac390-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac390-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac390-134">-WhatIf</span></span>
<span data-ttu-id="ac390-135">cmdlet이 실행되지만 cmdlet을 실행하지 않는 경우 발생하는 것을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ac390-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ac390-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac390-136">CommonParameters</span></span>
<span data-ttu-id="ac390-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ac390-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac390-138">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ac390-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac390-139">입력</span><span class="sxs-lookup"><span data-stu-id="ac390-139">INPUTS</span></span>

### <span data-ttu-id="ac390-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="ac390-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="ac390-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ac390-141">System.String</span></span>

## <span data-ttu-id="ac390-142">출력</span><span class="sxs-lookup"><span data-stu-id="ac390-142">OUTPUTS</span></span>

### <span data-ttu-id="ac390-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ac390-143">System.Boolean</span></span>

## <span data-ttu-id="ac390-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ac390-144">NOTES</span></span>
<span data-ttu-id="ac390-145">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="ac390-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ac390-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ac390-146">RELATED LINKS</span></span>

[<span data-ttu-id="ac390-147">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="ac390-147">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="ac390-148">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="ac390-148">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="ac390-149">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="ac390-149">Invoke-AzDataFactoryV2Pipeline</span></span>]()

