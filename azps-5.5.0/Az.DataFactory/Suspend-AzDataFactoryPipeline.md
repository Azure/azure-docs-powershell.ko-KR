---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/suspend-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
ms.openlocfilehash: f2538ecf8d4f6f962be85196ca49b8a0958f69e6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208685"
---
# <span data-ttu-id="be277-101">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="be277-101">Suspend-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="be277-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be277-102">SYNOPSIS</span></span>
<span data-ttu-id="be277-103">Azure Data Factory에서 파이프라인을 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="be277-103">Suspends a pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="be277-104">구문</span><span class="sxs-lookup"><span data-stu-id="be277-104">SYNTAX</span></span>

### <span data-ttu-id="be277-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="be277-105">ByFactoryName (Default)</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be277-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="be277-106">ByFactoryObject</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be277-107">설명</span><span class="sxs-lookup"><span data-stu-id="be277-107">DESCRIPTION</span></span>
<span data-ttu-id="be277-108">**Suspend-AzDataFactoryPipeline** cmdlet은 Azure Data Factory에서 파이프라인을 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="be277-108">The **Suspend-AzDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="be277-109">Resume-AzDataFactoryPipeline cmdlet을 사용하여 파이프라인을 다시 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be277-109">You can resume the pipeline by using the Resume-AzDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="be277-110">예제</span><span class="sxs-lookup"><span data-stu-id="be277-110">EXAMPLES</span></span>

### <span data-ttu-id="be277-111">예제 1: 파이프라인 일시 중단</span><span class="sxs-lookup"><span data-stu-id="be277-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="be277-112">이 명령은 WikiADF라는 데이터 팩터리에서 DPWikiSample이라는 파이프라인을 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="be277-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="be277-113">이 명령은 10진수의 $True.</span><span class="sxs-lookup"><span data-stu-id="be277-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="be277-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be277-114">PARAMETERS</span></span>

### <span data-ttu-id="be277-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="be277-115">-DataFactory</span></span>
<span data-ttu-id="be277-116">**PSDataFactory 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="be277-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="be277-117">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 파이프라인을 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="be277-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="be277-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="be277-118">-DataFactoryName</span></span>
<span data-ttu-id="be277-119">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="be277-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="be277-120">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 파이프라인을 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="be277-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="be277-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be277-121">-DefaultProfile</span></span>
<span data-ttu-id="be277-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="be277-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be277-123">-Name</span><span class="sxs-lookup"><span data-stu-id="be277-123">-Name</span></span>
<span data-ttu-id="be277-124">일시 중단할 파이프라인의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="be277-124">Specifies the name of the pipeline to suspend.</span></span>

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

### <span data-ttu-id="be277-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be277-125">-ResourceGroupName</span></span>
<span data-ttu-id="be277-126">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="be277-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="be277-127">이 cmdlet은 이 매개 변수가 지정하는 그룹에 속하는 파이프라인을 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="be277-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="be277-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be277-128">-Confirm</span></span>
<span data-ttu-id="be277-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="be277-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be277-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be277-130">-WhatIf</span></span>
<span data-ttu-id="be277-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="be277-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be277-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be277-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be277-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be277-133">CommonParameters</span></span>
<span data-ttu-id="be277-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="be277-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be277-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="be277-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be277-136">입력</span><span class="sxs-lookup"><span data-stu-id="be277-136">INPUTS</span></span>

### <span data-ttu-id="be277-137">System.String</span><span class="sxs-lookup"><span data-stu-id="be277-137">System.String</span></span>

### <span data-ttu-id="be277-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="be277-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="be277-139">출력</span><span class="sxs-lookup"><span data-stu-id="be277-139">OUTPUTS</span></span>

### <span data-ttu-id="be277-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="be277-140">System.Boolean</span></span>

## <span data-ttu-id="be277-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="be277-141">NOTES</span></span>
* <span data-ttu-id="be277-142">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="be277-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="be277-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="be277-143">RELATED LINKS</span></span>

[<span data-ttu-id="be277-144">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="be277-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="be277-145">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="be277-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="be277-146">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="be277-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="be277-147">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="be277-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="be277-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="be277-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


