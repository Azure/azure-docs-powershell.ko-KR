---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 181d63a41853105b21826353fabfca83cddf1bd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538196"
---
# <span data-ttu-id="40b55-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="40b55-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="40b55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40b55-102">SYNOPSIS</span></span>
<span data-ttu-id="40b55-103">관리 전용 통합 런타임을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b55-103">Stops a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40b55-104">구문과</span><span class="sxs-lookup"><span data-stu-id="40b55-104">SYNTAX</span></span>

### <span data-ttu-id="40b55-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="40b55-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="40b55-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="40b55-106">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="40b55-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="40b55-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="40b55-108">설명은</span><span class="sxs-lookup"><span data-stu-id="40b55-108">DESCRIPTION</span></span>
<span data-ttu-id="40b55-109">**AzureRmDataFactoryV2IntegrationRuntime** cmdlet은 ' 시작 됨 ' 상태의 관리 전용 통합 런타임을 중지 하며,이는 Start-AzureRmDataFactoryV2IntegrationRuntime cmdlet에 의해 시작 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="40b55-109">The **Stop-AzureRmDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="40b55-110">리소스가 해제 되 고 상태가 ' 중지 됨 '으로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="40b55-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="40b55-111">예제의</span><span class="sxs-lookup"><span data-stu-id="40b55-111">EXAMPLES</span></span>

### <span data-ttu-id="40b55-112">예제 1: ' 시작 됨 ' 상태의 관리 되는 통합 런타임 중지</span><span class="sxs-lookup"><span data-stu-id="40b55-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="40b55-113">관리 되는 통합 런타임 ' 테스트-reserlved-ir '은 ' 시작 됨 ' 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="40b55-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="40b55-114">Stop-AzureRmDataFactoryV2IntegrationRuntime cmdlet을 실행 한 후 리소스가 해제 되 고 상태가 ' 중지 됨 '으로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="40b55-114">After running Stop-AzureRmDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="40b55-115">변수</span><span class="sxs-lookup"><span data-stu-id="40b55-115">PARAMETERS</span></span>

### <span data-ttu-id="40b55-116">-확인</span><span class="sxs-lookup"><span data-stu-id="40b55-116">-Confirm</span></span>
<span data-ttu-id="40b55-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b55-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40b55-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="40b55-118">-DataFactoryName</span></span>
<span data-ttu-id="40b55-119">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40b55-119">The data factory name.</span></span>

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

### <span data-ttu-id="40b55-120">-Force</span><span class="sxs-lookup"><span data-stu-id="40b55-120">-Force</span></span>
<span data-ttu-id="40b55-121">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b55-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="40b55-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40b55-122">-InputObject</span></span>
<span data-ttu-id="40b55-123">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="40b55-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="40b55-124">-이름</span><span class="sxs-lookup"><span data-stu-id="40b55-124">-Name</span></span>
<span data-ttu-id="40b55-125">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40b55-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="40b55-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40b55-126">-ResourceGroupName</span></span>
<span data-ttu-id="40b55-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40b55-127">The resource group name.</span></span>

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

### <span data-ttu-id="40b55-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40b55-128">-ResourceId</span></span>
<span data-ttu-id="40b55-129">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="40b55-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="40b55-130">-확인</span><span class="sxs-lookup"><span data-stu-id="40b55-130">-Confirm</span></span>
<span data-ttu-id="40b55-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b55-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40b55-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40b55-132">-WhatIf</span></span>
<span data-ttu-id="40b55-133">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="40b55-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="40b55-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40b55-134">CommonParameters</span></span>
<span data-ttu-id="40b55-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b55-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40b55-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40b55-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40b55-137">입력</span><span class="sxs-lookup"><span data-stu-id="40b55-137">INPUTS</span></span>

### <span data-ttu-id="40b55-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="40b55-138">System.String</span></span>
<span data-ttu-id="40b55-139">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="40b55-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="40b55-140">출력</span><span class="sxs-lookup"><span data-stu-id="40b55-140">OUTPUTS</span></span>

### <span data-ttu-id="40b55-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="40b55-141">System.Boolean</span></span>

## <span data-ttu-id="40b55-142">상속자</span><span class="sxs-lookup"><span data-stu-id="40b55-142">NOTES</span></span>
<span data-ttu-id="40b55-143">키워드: azure, azurerm, arm, resource, management, manager, data, 팩토리, 복사, 활동, 통합 런타임</span><span class="sxs-lookup"><span data-stu-id="40b55-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="40b55-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40b55-144">RELATED LINKS</span></span>
[<span data-ttu-id="40b55-145">시작-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="40b55-145">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
