---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 0c24f77b51bcfc50ec11e211fc7f11b60e348221
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329335"
---
# <span data-ttu-id="ee72d-101">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ee72d-101">Remove-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="ee72d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee72d-102">SYNOPSIS</span></span>
<span data-ttu-id="ee72d-103">통합 런타임이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee72d-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="ee72d-104">구문</span><span class="sxs-lookup"><span data-stu-id="ee72d-104">SYNTAX</span></span>

### <span data-ttu-id="ee72d-105">ByIntegrationRuntimeName(기본값)</span><span class="sxs-lookup"><span data-stu-id="ee72d-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee72d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ee72d-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee72d-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="ee72d-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ee72d-108">설명</span><span class="sxs-lookup"><span data-stu-id="ee72d-108">DESCRIPTION</span></span>
<span data-ttu-id="ee72d-109">Remove-AzDataFactoryV2IntegrationRuntime cmdlet은 통합 런타임이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee72d-109">The Remove-AzDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="ee72d-110">예제</span><span class="sxs-lookup"><span data-stu-id="ee72d-110">EXAMPLES</span></span>

### <span data-ttu-id="ee72d-111">예제 1: 통합 런타임 제거</span><span class="sxs-lookup"><span data-stu-id="ee72d-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="ee72d-112">이 명령은 'test-df'라는 데이터 팩터리에서 'test-reserved-ir'이라는 통합 런타임을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ee72d-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="ee72d-113">이 명령은 $True.</span><span class="sxs-lookup"><span data-stu-id="ee72d-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="ee72d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee72d-114">PARAMETERS</span></span>

### <span data-ttu-id="ee72d-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ee72d-115">-DataFactoryName</span></span>
<span data-ttu-id="ee72d-116">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee72d-116">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee72d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee72d-117">-DefaultProfile</span></span>
<span data-ttu-id="ee72d-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee72d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee72d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ee72d-119">-Force</span></span>
<span data-ttu-id="ee72d-120">확인 메시지를 표시하지 않고 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ee72d-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ee72d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee72d-121">-InputObject</span></span>
<span data-ttu-id="ee72d-122">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ee72d-122">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee72d-123">-LinkedDataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ee72d-123">-LinkedDataFactoryName</span></span>
<span data-ttu-id="ee72d-124">연결된 데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee72d-124">The linked data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee72d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ee72d-125">-Name</span></span>
<span data-ttu-id="ee72d-126">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee72d-126">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee72d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee72d-127">-ResourceGroupName</span></span>
<span data-ttu-id="ee72d-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee72d-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee72d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee72d-129">-ResourceId</span></span>
<span data-ttu-id="ee72d-130">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ee72d-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee72d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee72d-131">-Confirm</span></span>
<span data-ttu-id="ee72d-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee72d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee72d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee72d-133">-WhatIf</span></span>
<span data-ttu-id="ee72d-134">cmdlet이 실행되지만 cmdlet을 실행하지 않는 경우 발생하는 것을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ee72d-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ee72d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee72d-135">CommonParameters</span></span>
<span data-ttu-id="ee72d-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ee72d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee72d-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ee72d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee72d-138">입력</span><span class="sxs-lookup"><span data-stu-id="ee72d-138">INPUTS</span></span>

### <span data-ttu-id="ee72d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ee72d-139">System.String</span></span>

### <span data-ttu-id="ee72d-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ee72d-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ee72d-141">출력</span><span class="sxs-lookup"><span data-stu-id="ee72d-141">OUTPUTS</span></span>

### <span data-ttu-id="ee72d-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="ee72d-142">System.Void</span></span>

## <span data-ttu-id="ee72d-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ee72d-143">NOTES</span></span>
<span data-ttu-id="ee72d-144">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리, 복사, 활동, 통합 런타임</span><span class="sxs-lookup"><span data-stu-id="ee72d-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="ee72d-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee72d-145">RELATED LINKS</span></span>

[<span data-ttu-id="ee72d-146">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ee72d-146">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="ee72d-147">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ee72d-147">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

