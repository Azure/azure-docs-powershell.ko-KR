---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: b1d39c3d60d043485cc4ec4dc0c4ba986a97e800
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212840"
---
# <span data-ttu-id="726d4-101">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="726d4-101">Remove-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="726d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="726d4-102">SYNOPSIS</span></span>
<span data-ttu-id="726d4-103">Data Factory에서 파이프라인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d4-103">Removes a pipeline from Data Factory.</span></span>

## <span data-ttu-id="726d4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="726d4-104">SYNTAX</span></span>

### <span data-ttu-id="726d4-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="726d4-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="726d4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="726d4-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="726d4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="726d4-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="726d4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="726d4-108">DESCRIPTION</span></span>
<span data-ttu-id="726d4-109">Remove-AzDataFactoryV2Pipeline cmdlet은 Azure Data Factory에서 파이프라인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d4-109">The Remove-AzDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="726d4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="726d4-110">EXAMPLES</span></span>

### <span data-ttu-id="726d4-111">예제 1: 파이프라인 제거</span><span class="sxs-lookup"><span data-stu-id="726d4-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="726d4-112">이 cmdlet은 WikiADF 이라는 data factory에서 DPWikisample 이라는 파이프라인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d4-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="726d4-113">이 명령은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d4-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="726d4-114">변수</span><span class="sxs-lookup"><span data-stu-id="726d4-114">PARAMETERS</span></span>

### <span data-ttu-id="726d4-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="726d4-115">-DataFactoryName</span></span>
<span data-ttu-id="726d4-116">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d4-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="726d4-117">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 파이프라인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d4-117">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="726d4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="726d4-118">-DefaultProfile</span></span>
<span data-ttu-id="726d4-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="726d4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="726d4-120">-Force</span><span class="sxs-lookup"><span data-stu-id="726d4-120">-Force</span></span>
<span data-ttu-id="726d4-121">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d4-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="726d4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="726d4-122">-InputObject</span></span>
<span data-ttu-id="726d4-123">파이프라인 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d4-123">Specifies a Pipeline object.</span></span>
<span data-ttu-id="726d4-124">이 cmdlet은이 매개 변수에서 지정 하는 파이프라인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d4-124">This cmdlet removes the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="726d4-125">-이름</span><span class="sxs-lookup"><span data-stu-id="726d4-125">-Name</span></span>
<span data-ttu-id="726d4-126">제거할 파이프라인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d4-126">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="726d4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="726d4-127">-ResourceGroupName</span></span>
<span data-ttu-id="726d4-128">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d4-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="726d4-129">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 파이프라인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d4-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="726d4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="726d4-130">-ResourceId</span></span>
<span data-ttu-id="726d4-131">제거할 파이프라인의 Azure resource ID입니다.</span><span class="sxs-lookup"><span data-stu-id="726d4-131">The Azure resource ID of the pipeline to remove.</span></span>

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

### <span data-ttu-id="726d4-132">-확인</span><span class="sxs-lookup"><span data-stu-id="726d4-132">-Confirm</span></span>
<span data-ttu-id="726d4-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="726d4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="726d4-134">-WhatIf</span></span>
<span data-ttu-id="726d4-135">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="726d4-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="726d4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="726d4-136">CommonParameters</span></span>
<span data-ttu-id="726d4-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="726d4-138">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="726d4-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="726d4-139">입력</span><span class="sxs-lookup"><span data-stu-id="726d4-139">INPUTS</span></span>

### <span data-ttu-id="726d4-140">DataFactoryV2. PSPipeline/.</span><span class="sxs-lookup"><span data-stu-id="726d4-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="726d4-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="726d4-141">System.String</span></span>

## <span data-ttu-id="726d4-142">출력</span><span class="sxs-lookup"><span data-stu-id="726d4-142">OUTPUTS</span></span>

### <span data-ttu-id="726d4-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="726d4-143">System.Boolean</span></span>

## <span data-ttu-id="726d4-144">상속자</span><span class="sxs-lookup"><span data-stu-id="726d4-144">NOTES</span></span>
<span data-ttu-id="726d4-145">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="726d4-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="726d4-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="726d4-146">RELATED LINKS</span></span>

[<span data-ttu-id="726d4-147">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="726d4-147">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="726d4-148">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="726d4-148">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="726d4-149">AzDataFactoryV2Pipeline-호출</span><span class="sxs-lookup"><span data-stu-id="726d4-149">Invoke-AzDataFactoryV2Pipeline</span></span>]()

