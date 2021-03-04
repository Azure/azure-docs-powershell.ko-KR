---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: eb832037080550a1a22c3cacce2386eba7c4e6f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971136"
---
# <span data-ttu-id="db871-101">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="db871-101">Remove-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="db871-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db871-102">SYNOPSIS</span></span>
<span data-ttu-id="db871-103">Data Factory에서 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="db871-103">Removes a pipeline from Data Factory.</span></span>

## <span data-ttu-id="db871-104">구문</span><span class="sxs-lookup"><span data-stu-id="db871-104">SYNTAX</span></span>

### <span data-ttu-id="db871-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="db871-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db871-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="db871-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db871-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="db871-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db871-108">설명</span><span class="sxs-lookup"><span data-stu-id="db871-108">DESCRIPTION</span></span>
<span data-ttu-id="db871-109">Remove-AzDataFactoryV2Pipeline cmdlet은 Azure Data Factory에서 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="db871-109">The Remove-AzDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="db871-110">예제</span><span class="sxs-lookup"><span data-stu-id="db871-110">EXAMPLES</span></span>

### <span data-ttu-id="db871-111">예제 1: 파이프라인 제거</span><span class="sxs-lookup"><span data-stu-id="db871-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="db871-112">이 cmdlet은 WikiADF라는 데이터 팩터리에서 DPWikisample이라는 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="db871-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="db871-113">명령은 값의 $True.</span><span class="sxs-lookup"><span data-stu-id="db871-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="db871-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="db871-114">PARAMETERS</span></span>

### <span data-ttu-id="db871-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="db871-115">-DataFactoryName</span></span>
<span data-ttu-id="db871-116">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="db871-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="db871-117">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에서 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="db871-117">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="db871-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db871-118">-DefaultProfile</span></span>
<span data-ttu-id="db871-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="db871-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db871-120">-Force</span><span class="sxs-lookup"><span data-stu-id="db871-120">-Force</span></span>
<span data-ttu-id="db871-121">확인을 요청하지 않고 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="db871-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="db871-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db871-122">-InputObject</span></span>
<span data-ttu-id="db871-123">파이프라인 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="db871-123">Specifies a Pipeline object.</span></span>
<span data-ttu-id="db871-124">이 cmdlet은 이 매개 변수가 지정하는 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="db871-124">This cmdlet removes the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="db871-125">-Name</span><span class="sxs-lookup"><span data-stu-id="db871-125">-Name</span></span>
<span data-ttu-id="db871-126">제거할 파이프라인의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="db871-126">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="db871-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db871-127">-ResourceGroupName</span></span>
<span data-ttu-id="db871-128">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="db871-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="db871-129">이 cmdlet은 이 매개 변수가 지정하는 그룹에서 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="db871-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="db871-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db871-130">-ResourceId</span></span>
<span data-ttu-id="db871-131">제거할 파이프라인의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="db871-131">The Azure resource ID of the pipeline to remove.</span></span>

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

### <span data-ttu-id="db871-132">-확인</span><span class="sxs-lookup"><span data-stu-id="db871-132">-Confirm</span></span>
<span data-ttu-id="db871-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="db871-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db871-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db871-134">-WhatIf</span></span>
<span data-ttu-id="db871-135">cmdlet이 실행되지만 cmdlet을 실행하지 않는 경우 발생하는 것을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="db871-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="db871-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db871-136">CommonParameters</span></span>
<span data-ttu-id="db871-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="db871-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db871-138">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="db871-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db871-139">입력</span><span class="sxs-lookup"><span data-stu-id="db871-139">INPUTS</span></span>

### <span data-ttu-id="db871-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="db871-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="db871-141">System.String</span><span class="sxs-lookup"><span data-stu-id="db871-141">System.String</span></span>

## <span data-ttu-id="db871-142">출력</span><span class="sxs-lookup"><span data-stu-id="db871-142">OUTPUTS</span></span>

### <span data-ttu-id="db871-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="db871-143">System.Boolean</span></span>

## <span data-ttu-id="db871-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="db871-144">NOTES</span></span>
<span data-ttu-id="db871-145">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="db871-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="db871-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="db871-146">RELATED LINKS</span></span>

[<span data-ttu-id="db871-147">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="db871-147">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="db871-148">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="db871-148">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="db871-149">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="db871-149">Invoke-AzDataFactoryV2Pipeline</span></span>]()

