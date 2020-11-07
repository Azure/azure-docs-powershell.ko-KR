---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/suspend-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Suspend-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Suspend-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: ecbf1a97ebaa7f4d008b63f9b7d4c49c49a09956
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535203"
---
# <span data-ttu-id="dfcbc-101">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="dfcbc-101">Suspend-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="dfcbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfcbc-102">SYNOPSIS</span></span>
<span data-ttu-id="dfcbc-103">Azure Data Factory에서 파이프라인을 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfcbc-103">Suspends a pipeline in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfcbc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dfcbc-104">SYNTAX</span></span>

### <span data-ttu-id="dfcbc-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="dfcbc-105">ByFactoryName (Default)</span></span>
```
Suspend-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfcbc-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="dfcbc-106">ByFactoryObject</span></span>
```
Suspend-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfcbc-107">설명은</span><span class="sxs-lookup"><span data-stu-id="dfcbc-107">DESCRIPTION</span></span>
<span data-ttu-id="dfcbc-108">**AzureRmDataFactoryPipeline** Cmdlet은 Azure Data Factory의 파이프라인을 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfcbc-108">The **Suspend-AzureRmDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="dfcbc-109">Resume-AzureRmDataFactoryPipeline cmdlet을 사용 하 여 파이프라인을 다시 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dfcbc-109">You can resume the pipeline by using the Resume-AzureRmDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="dfcbc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="dfcbc-110">EXAMPLES</span></span>

### <span data-ttu-id="dfcbc-111">예제 1: 파이프라인 일시 중단</span><span class="sxs-lookup"><span data-stu-id="dfcbc-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="dfcbc-112">이 명령은 WikiADF 이라는 data factory에서 DPWikiSample 라는 파이프라인을 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfcbc-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="dfcbc-113">이 명령은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfcbc-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="dfcbc-114">변수</span><span class="sxs-lookup"><span data-stu-id="dfcbc-114">PARAMETERS</span></span>

### <span data-ttu-id="dfcbc-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="dfcbc-115">-DataFactory</span></span>
<span data-ttu-id="dfcbc-116">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfcbc-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="dfcbc-117">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속하는 파이프라인을 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfcbc-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="dfcbc-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="dfcbc-118">-DataFactoryName</span></span>
<span data-ttu-id="dfcbc-119">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfcbc-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="dfcbc-120">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속하는 파이프라인을 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfcbc-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="dfcbc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfcbc-121">-DefaultProfile</span></span>
<span data-ttu-id="dfcbc-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="dfcbc-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfcbc-123">-이름</span><span class="sxs-lookup"><span data-stu-id="dfcbc-123">-Name</span></span>
<span data-ttu-id="dfcbc-124">일시 중단할 파이프라인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfcbc-124">Specifies the name of the pipeline to suspend.</span></span>

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

### <span data-ttu-id="dfcbc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfcbc-125">-ResourceGroupName</span></span>
<span data-ttu-id="dfcbc-126">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfcbc-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="dfcbc-127">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 파이프라인을 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfcbc-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="dfcbc-128">-확인</span><span class="sxs-lookup"><span data-stu-id="dfcbc-128">-Confirm</span></span>
<span data-ttu-id="dfcbc-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfcbc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfcbc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfcbc-130">-WhatIf</span></span>
<span data-ttu-id="dfcbc-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dfcbc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfcbc-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dfcbc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfcbc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfcbc-133">CommonParameters</span></span>
<span data-ttu-id="dfcbc-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfcbc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfcbc-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfcbc-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfcbc-136">입력</span><span class="sxs-lookup"><span data-stu-id="dfcbc-136">INPUTS</span></span>

### <span data-ttu-id="dfcbc-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dfcbc-137">System.String</span></span>

### <span data-ttu-id="dfcbc-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="dfcbc-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="dfcbc-139">출력</span><span class="sxs-lookup"><span data-stu-id="dfcbc-139">OUTPUTS</span></span>

### <span data-ttu-id="dfcbc-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="dfcbc-140">System.Boolean</span></span>

## <span data-ttu-id="dfcbc-141">상속자</span><span class="sxs-lookup"><span data-stu-id="dfcbc-141">NOTES</span></span>
* <span data-ttu-id="dfcbc-142">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="dfcbc-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="dfcbc-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dfcbc-143">RELATED LINKS</span></span>

[<span data-ttu-id="dfcbc-144">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="dfcbc-144">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="dfcbc-145">새로운 AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="dfcbc-145">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="dfcbc-146">제거-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="dfcbc-146">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="dfcbc-147">이력서-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="dfcbc-147">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="dfcbc-148">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="dfcbc-148">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

