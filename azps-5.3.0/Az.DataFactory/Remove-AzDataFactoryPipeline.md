---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
ms.openlocfilehash: 2bae0bd597cbd97a81efeaecb07e052457b88438
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493524"
---
# <span data-ttu-id="1f4c7-101">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1f4c7-101">Remove-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="1f4c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f4c7-102">SYNOPSIS</span></span>
<span data-ttu-id="1f4c7-103">Azure Data Factory에서 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4c7-103">Removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="1f4c7-104">구문</span><span class="sxs-lookup"><span data-stu-id="1f4c7-104">SYNTAX</span></span>

### <span data-ttu-id="1f4c7-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="1f4c7-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f4c7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1f4c7-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f4c7-107">설명</span><span class="sxs-lookup"><span data-stu-id="1f4c7-107">DESCRIPTION</span></span>
<span data-ttu-id="1f4c7-108">**Remove-AzDataFactoryPipeline** cmdlet은 Azure Data Factory에서 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4c7-108">The **Remove-AzDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="1f4c7-109">예제</span><span class="sxs-lookup"><span data-stu-id="1f4c7-109">EXAMPLES</span></span>

### <span data-ttu-id="1f4c7-110">예제 1: 파이프라인 제거</span><span class="sxs-lookup"><span data-stu-id="1f4c7-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="1f4c7-111">이 cmdlet은 WikiADF라는 데이터 팩터리에서 DPWikisample이라는 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4c7-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="1f4c7-112">이 명령은 10진수의 $True.</span><span class="sxs-lookup"><span data-stu-id="1f4c7-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="1f4c7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f4c7-113">PARAMETERS</span></span>

### <span data-ttu-id="1f4c7-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1f4c7-114">-DataFactory</span></span>
<span data-ttu-id="1f4c7-115">**PSDataFactory 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="1f4c7-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="1f4c7-116">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에서 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4c7-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f4c7-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1f4c7-117">-DataFactoryName</span></span>
<span data-ttu-id="1f4c7-118">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4c7-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1f4c7-119">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에서 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4c7-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1f4c7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f4c7-120">-DefaultProfile</span></span>
<span data-ttu-id="1f4c7-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1f4c7-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f4c7-122">-Force</span><span class="sxs-lookup"><span data-stu-id="1f4c7-122">-Force</span></span>
<span data-ttu-id="1f4c7-123">이 cmdlet이 확인 메시지를 표시하지 않고 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4c7-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="1f4c7-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1f4c7-124">-Name</span></span>
<span data-ttu-id="1f4c7-125">제거할 파이프라인의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4c7-125">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f4c7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f4c7-126">-ResourceGroupName</span></span>
<span data-ttu-id="1f4c7-127">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4c7-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1f4c7-128">이 cmdlet은 이 매개 변수가 지정하는 그룹에서 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4c7-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1f4c7-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f4c7-129">-Confirm</span></span>
<span data-ttu-id="1f4c7-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f4c7-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f4c7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f4c7-131">-WhatIf</span></span>
<span data-ttu-id="1f4c7-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1f4c7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f4c7-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4c7-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f4c7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f4c7-134">CommonParameters</span></span>
<span data-ttu-id="1f4c7-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4c7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f4c7-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1f4c7-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f4c7-137">입력</span><span class="sxs-lookup"><span data-stu-id="1f4c7-137">INPUTS</span></span>

### <span data-ttu-id="1f4c7-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1f4c7-138">System.String</span></span>

### <span data-ttu-id="1f4c7-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1f4c7-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="1f4c7-140">출력</span><span class="sxs-lookup"><span data-stu-id="1f4c7-140">OUTPUTS</span></span>

### <span data-ttu-id="1f4c7-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="1f4c7-141">System.Void</span></span>

## <span data-ttu-id="1f4c7-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1f4c7-142">NOTES</span></span>
* <span data-ttu-id="1f4c7-143">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="1f4c7-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1f4c7-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f4c7-144">RELATED LINKS</span></span>

[<span data-ttu-id="1f4c7-145">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1f4c7-145">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="1f4c7-146">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1f4c7-146">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="1f4c7-147">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1f4c7-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="1f4c7-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="1f4c7-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="1f4c7-149">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1f4c7-149">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


