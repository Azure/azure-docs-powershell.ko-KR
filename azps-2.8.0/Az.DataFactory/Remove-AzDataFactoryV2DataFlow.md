---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 75c155b765a1bcbc565a85fc0f47130a6d2a5cf0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697000"
---
# <span data-ttu-id="e3051-101">Remove-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="e3051-101">Remove-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="e3051-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3051-102">SYNOPSIS</span></span>
<span data-ttu-id="e3051-103">Data Factory에서 데이터 흐름을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3051-103">Removes a data flow from Data Factory.</span></span>

## <span data-ttu-id="e3051-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e3051-104">SYNTAX</span></span>

### <span data-ttu-id="e3051-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="e3051-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3051-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e3051-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2DataFlow [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3051-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e3051-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Force] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3051-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e3051-108">DESCRIPTION</span></span>
<span data-ttu-id="e3051-109">Remove-AzDataFactoryV2DataFlow cmdlet은 Azure Data Factory에서 데이터 흐름을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3051-109">The Remove-AzDataFactoryV2DataFlow cmdlet removes a data flow from Azure Data Factory.</span></span>

## <span data-ttu-id="e3051-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e3051-110">EXAMPLES</span></span>

### <span data-ttu-id="e3051-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e3051-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Remove-AzDataFactoryV2DataFlow -ResourceGroupName adf -DataFactoryName WikiADF -DataFlowName "dataflow5"

Confirm
Are you sure you want to remove data flow 'dataflow5' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\WINDOWS\system32>
```

<span data-ttu-id="e3051-112">이 명령은 WikiADF 이라는 data factory에서 dataflow5 라는 데이터 흐름을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3051-112">This command removes the data flow named dataflow5 from the data factory named WikiADF.</span></span>

## <span data-ttu-id="e3051-113">변수</span><span class="sxs-lookup"><span data-stu-id="e3051-113">PARAMETERS</span></span>

### <span data-ttu-id="e3051-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e3051-114">-DataFactoryName</span></span>
<span data-ttu-id="e3051-115">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3051-115">The data factory name.</span></span>

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

### <span data-ttu-id="e3051-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3051-116">-DefaultProfile</span></span>
<span data-ttu-id="e3051-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e3051-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3051-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e3051-118">-Force</span></span>
<span data-ttu-id="e3051-119">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3051-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e3051-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3051-120">-InputObject</span></span>
<span data-ttu-id="e3051-121">데이터 흐름 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e3051-121">The data flow object.</span></span>

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

### <span data-ttu-id="e3051-122">-이름</span><span class="sxs-lookup"><span data-stu-id="e3051-122">-Name</span></span>
<span data-ttu-id="e3051-123">데이터 흐름 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3051-123">The data flow name.</span></span>

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

### <span data-ttu-id="e3051-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3051-124">-ResourceGroupName</span></span>
<span data-ttu-id="e3051-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3051-125">The resource group name.</span></span>

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

### <span data-ttu-id="e3051-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3051-126">-ResourceId</span></span>
<span data-ttu-id="e3051-127">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e3051-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e3051-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3051-128">-PassThru</span></span>
<span data-ttu-id="e3051-129">지정 된 경우 대/소문자 구분 작업이 성공한 경우 true를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="e3051-129">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="e3051-130">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="e3051-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="e3051-131">-확인</span><span class="sxs-lookup"><span data-stu-id="e3051-131">-Confirm</span></span>
<span data-ttu-id="e3051-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3051-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3051-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3051-133">-WhatIf</span></span>
<span data-ttu-id="e3051-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e3051-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3051-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3051-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3051-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3051-136">CommonParameters</span></span>
<span data-ttu-id="e3051-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3051-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3051-138">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e3051-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3051-139">입력</span><span class="sxs-lookup"><span data-stu-id="e3051-139">INPUTS</span></span>

### <span data-ttu-id="e3051-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="e3051-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="e3051-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e3051-141">System.String</span></span>

## <span data-ttu-id="e3051-142">출력</span><span class="sxs-lookup"><span data-stu-id="e3051-142">OUTPUTS</span></span>

### <span data-ttu-id="e3051-143">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="e3051-143">System.Void</span></span>

### <span data-ttu-id="e3051-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e3051-144">System.Boolean</span></span>

## <span data-ttu-id="e3051-145">상속자</span><span class="sxs-lookup"><span data-stu-id="e3051-145">NOTES</span></span>
<span data-ttu-id="e3051-146">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="e3051-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e3051-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3051-147">RELATED LINKS</span></span>

[<span data-ttu-id="e3051-148">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="e3051-148">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="e3051-149">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="e3051-149">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

