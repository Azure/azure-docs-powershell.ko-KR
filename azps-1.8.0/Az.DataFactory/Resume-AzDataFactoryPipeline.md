---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F522841A-4246-4028-A754-393D8DADD924
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/resume-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Resume-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Resume-AzDataFactoryPipeline.md
ms.openlocfilehash: 221fb414464c062a2f1798223bfe68a09543d7c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701122"
---
# <span data-ttu-id="36210-101">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="36210-101">Resume-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="36210-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36210-102">SYNOPSIS</span></span>
<span data-ttu-id="36210-103">Data Factory에서 일시 중단 된 파이프라인을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="36210-103">Resumes a suspended pipeline in Data Factory.</span></span>

## <span data-ttu-id="36210-104">구문과</span><span class="sxs-lookup"><span data-stu-id="36210-104">SYNTAX</span></span>

### <span data-ttu-id="36210-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="36210-105">ByFactoryName (Default)</span></span>
```
Resume-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36210-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="36210-106">ByFactoryObject</span></span>
```
Resume-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36210-107">설명은</span><span class="sxs-lookup"><span data-stu-id="36210-107">DESCRIPTION</span></span>
<span data-ttu-id="36210-108">**AzDataFactoryPipeline** Cmdlet은 Azure Data Factory에서 일시 중단 된 파이프라인을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="36210-108">The **Resume-AzDataFactoryPipeline** cmdlet resumes a suspended pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="36210-109">예제의</span><span class="sxs-lookup"><span data-stu-id="36210-109">EXAMPLES</span></span>

### <span data-ttu-id="36210-110">예제 1: 파이프라인 다시 시작</span><span class="sxs-lookup"><span data-stu-id="36210-110">Example 1: Resume a pipeline</span></span>
```
PS C:\>Resume-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to resume pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="36210-111">이 명령은 WikiADF 이라는 data factory에서 DPWikisample 라는 파이프라인을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="36210-111">This command resumes the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="36210-112">파이프라인을 일시 중단 하려면 **AzDataFactoryPipeline** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="36210-112">Use the **Suspend-AzDataFactoryPipeline** cmdlet to suspend a pipeline.</span></span>
<span data-ttu-id="36210-113">이 명령은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="36210-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="36210-114">변수</span><span class="sxs-lookup"><span data-stu-id="36210-114">PARAMETERS</span></span>

### <span data-ttu-id="36210-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="36210-115">-DataFactory</span></span>
<span data-ttu-id="36210-116">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36210-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="36210-117">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속한 파이프라인을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="36210-117">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="36210-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="36210-118">-DataFactoryName</span></span>
<span data-ttu-id="36210-119">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36210-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="36210-120">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속한 파이프라인을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="36210-120">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="36210-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36210-121">-DefaultProfile</span></span>
<span data-ttu-id="36210-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="36210-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36210-123">-이름</span><span class="sxs-lookup"><span data-stu-id="36210-123">-Name</span></span>
<span data-ttu-id="36210-124">다시 시작할 파이프라인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36210-124">Specifies the name of the pipeline to resume.</span></span>

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

### <span data-ttu-id="36210-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36210-125">-ResourceGroupName</span></span>
<span data-ttu-id="36210-126">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36210-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="36210-127">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 파이프라인을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="36210-127">This cmdlet resumes a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="36210-128">-확인</span><span class="sxs-lookup"><span data-stu-id="36210-128">-Confirm</span></span>
<span data-ttu-id="36210-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="36210-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36210-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36210-130">-WhatIf</span></span>
<span data-ttu-id="36210-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="36210-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36210-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36210-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36210-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36210-133">CommonParameters</span></span>
<span data-ttu-id="36210-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="36210-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36210-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36210-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36210-136">입력</span><span class="sxs-lookup"><span data-stu-id="36210-136">INPUTS</span></span>

### <span data-ttu-id="36210-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="36210-137">System.String</span></span>

### <span data-ttu-id="36210-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="36210-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="36210-139">출력</span><span class="sxs-lookup"><span data-stu-id="36210-139">OUTPUTS</span></span>

### <span data-ttu-id="36210-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="36210-140">System.Boolean</span></span>

## <span data-ttu-id="36210-141">상속자</span><span class="sxs-lookup"><span data-stu-id="36210-141">NOTES</span></span>
* <span data-ttu-id="36210-142">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="36210-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="36210-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36210-143">RELATED LINKS</span></span>

[<span data-ttu-id="36210-144">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="36210-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="36210-145">새로운 AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="36210-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="36210-146">제거-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="36210-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="36210-147">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="36210-147">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="36210-148">일시 중단-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="36210-148">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


