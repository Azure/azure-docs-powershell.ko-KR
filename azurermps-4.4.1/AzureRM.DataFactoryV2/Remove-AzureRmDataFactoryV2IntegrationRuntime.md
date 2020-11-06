---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 81b05b8229530a8975be023a3b4a5e8c93d93c80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537316"
---
# <span data-ttu-id="abb57-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="abb57-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="abb57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abb57-102">SYNOPSIS</span></span>
<span data-ttu-id="abb57-103">통합 런타임을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="abb57-103">Removes an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abb57-104">구문과</span><span class="sxs-lookup"><span data-stu-id="abb57-104">SYNTAX</span></span>

### <span data-ttu-id="abb57-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="abb57-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="abb57-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="abb57-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="abb57-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="abb57-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="abb57-108">설명은</span><span class="sxs-lookup"><span data-stu-id="abb57-108">DESCRIPTION</span></span>
<span data-ttu-id="abb57-109">Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet은 통합 런타임을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="abb57-109">The Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="abb57-110">예제의</span><span class="sxs-lookup"><span data-stu-id="abb57-110">EXAMPLES</span></span>

### <span data-ttu-id="abb57-111">예제 1: 통합 런타임 제거</span><span class="sxs-lookup"><span data-stu-id="abb57-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="abb57-112">이 명령은 ' test-df ' 라는 데이터 팩터리에 ' test-reserved-ir ' 이라는 통합 런타임을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="abb57-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="abb57-113">이 명령은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="abb57-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="abb57-114">변수</span><span class="sxs-lookup"><span data-stu-id="abb57-114">PARAMETERS</span></span>

### <span data-ttu-id="abb57-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="abb57-115">-DataFactoryName</span></span>
<span data-ttu-id="abb57-116">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="abb57-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abb57-117">-Force</span><span class="sxs-lookup"><span data-stu-id="abb57-117">-Force</span></span>
<span data-ttu-id="abb57-118">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="abb57-118">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abb57-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abb57-119">-InputObject</span></span>
<span data-ttu-id="abb57-120">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="abb57-120">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abb57-121">-이름</span><span class="sxs-lookup"><span data-stu-id="abb57-121">-Name</span></span>
<span data-ttu-id="abb57-122">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="abb57-122">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abb57-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abb57-123">-ResourceGroupName</span></span>
<span data-ttu-id="abb57-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="abb57-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abb57-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abb57-125">-ResourceId</span></span>
<span data-ttu-id="abb57-126">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="abb57-126">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abb57-127">-확인</span><span class="sxs-lookup"><span data-stu-id="abb57-127">-Confirm</span></span>
<span data-ttu-id="abb57-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="abb57-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abb57-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abb57-129">-WhatIf</span></span>
<span data-ttu-id="abb57-130">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="abb57-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="abb57-131">입력</span><span class="sxs-lookup"><span data-stu-id="abb57-131">INPUTS</span></span>

### <span data-ttu-id="abb57-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="abb57-132">System.String</span></span>
<span data-ttu-id="abb57-133">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="abb57-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="abb57-134">출력</span><span class="sxs-lookup"><span data-stu-id="abb57-134">OUTPUTS</span></span>

### <span data-ttu-id="abb57-135">System. 개체</span><span class="sxs-lookup"><span data-stu-id="abb57-135">System.Object</span></span>

## <span data-ttu-id="abb57-136">상속자</span><span class="sxs-lookup"><span data-stu-id="abb57-136">NOTES</span></span>
<span data-ttu-id="abb57-137">키워드: azure, azurerm, arm, resource, management, manager, data, 팩토리, 복사, 활동, 통합 런타임</span><span class="sxs-lookup"><span data-stu-id="abb57-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="abb57-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="abb57-138">RELATED LINKS</span></span>
[<span data-ttu-id="abb57-139">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="abb57-139">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="abb57-140">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="abb57-140">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

