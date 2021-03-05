---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
ms.openlocfilehash: 25653cb7423803f2722a87e218c4ee4b3d73be86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972859"
---
# <span data-ttu-id="002fd-101">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="002fd-101">Remove-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="002fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="002fd-102">SYNOPSIS</span></span>
<span data-ttu-id="002fd-103">Azure Data Factory에서 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="002fd-103">Removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="002fd-104">구문</span><span class="sxs-lookup"><span data-stu-id="002fd-104">SYNTAX</span></span>

### <span data-ttu-id="002fd-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="002fd-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="002fd-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="002fd-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="002fd-107">설명</span><span class="sxs-lookup"><span data-stu-id="002fd-107">DESCRIPTION</span></span>
<span data-ttu-id="002fd-108">**Remove-AzDataFactoryPipeline** cmdlet은 Azure Data Factory에서 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="002fd-108">The **Remove-AzDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="002fd-109">예제</span><span class="sxs-lookup"><span data-stu-id="002fd-109">EXAMPLES</span></span>

### <span data-ttu-id="002fd-110">예제 1: 파이프라인 제거</span><span class="sxs-lookup"><span data-stu-id="002fd-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="002fd-111">이 cmdlet은 WikiADF라는 데이터 팩터리에서 DPWikisample이라는 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="002fd-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="002fd-112">명령은 값의 $True.</span><span class="sxs-lookup"><span data-stu-id="002fd-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="002fd-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="002fd-113">PARAMETERS</span></span>

### <span data-ttu-id="002fd-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="002fd-114">-DataFactory</span></span>
<span data-ttu-id="002fd-115">**PSDataFactory 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="002fd-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="002fd-116">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에서 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="002fd-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="002fd-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="002fd-117">-DataFactoryName</span></span>
<span data-ttu-id="002fd-118">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="002fd-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="002fd-119">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에서 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="002fd-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="002fd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="002fd-120">-DefaultProfile</span></span>
<span data-ttu-id="002fd-121">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="002fd-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="002fd-122">-Force</span><span class="sxs-lookup"><span data-stu-id="002fd-122">-Force</span></span>
<span data-ttu-id="002fd-123">이 cmdlet은 확인을 요청하지 않고 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="002fd-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="002fd-124">-Name</span><span class="sxs-lookup"><span data-stu-id="002fd-124">-Name</span></span>
<span data-ttu-id="002fd-125">제거할 파이프라인의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="002fd-125">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="002fd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="002fd-126">-ResourceGroupName</span></span>
<span data-ttu-id="002fd-127">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="002fd-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="002fd-128">이 cmdlet은 이 매개 변수가 지정하는 그룹에서 파이프라인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="002fd-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="002fd-129">-확인</span><span class="sxs-lookup"><span data-stu-id="002fd-129">-Confirm</span></span>
<span data-ttu-id="002fd-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="002fd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="002fd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="002fd-131">-WhatIf</span></span>
<span data-ttu-id="002fd-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="002fd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="002fd-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="002fd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="002fd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="002fd-134">CommonParameters</span></span>
<span data-ttu-id="002fd-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="002fd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="002fd-136">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="002fd-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="002fd-137">입력</span><span class="sxs-lookup"><span data-stu-id="002fd-137">INPUTS</span></span>

### <span data-ttu-id="002fd-138">System.String</span><span class="sxs-lookup"><span data-stu-id="002fd-138">System.String</span></span>

### <span data-ttu-id="002fd-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="002fd-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="002fd-140">출력</span><span class="sxs-lookup"><span data-stu-id="002fd-140">OUTPUTS</span></span>

### <span data-ttu-id="002fd-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="002fd-141">System.Void</span></span>

## <span data-ttu-id="002fd-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="002fd-142">NOTES</span></span>
* <span data-ttu-id="002fd-143">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="002fd-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="002fd-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="002fd-144">RELATED LINKS</span></span>

[<span data-ttu-id="002fd-145">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="002fd-145">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="002fd-146">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="002fd-146">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="002fd-147">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="002fd-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="002fd-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="002fd-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="002fd-149">suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="002fd-149">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


