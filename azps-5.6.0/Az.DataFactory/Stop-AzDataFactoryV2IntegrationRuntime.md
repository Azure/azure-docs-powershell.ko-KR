---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/stop-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 405754afec3ff62eb59d385646df43f699557d18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998489"
---
# <span data-ttu-id="3f13b-101">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3f13b-101">Stop-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="3f13b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f13b-102">SYNOPSIS</span></span>
<span data-ttu-id="3f13b-103">관리되는 전용 통합 런타임이 중지됩니다.</span><span class="sxs-lookup"><span data-stu-id="3f13b-103">Stops a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="3f13b-104">구문</span><span class="sxs-lookup"><span data-stu-id="3f13b-104">SYNTAX</span></span>

### <span data-ttu-id="3f13b-105">ByIntegrationRuntimeName(기본값)</span><span class="sxs-lookup"><span data-stu-id="3f13b-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f13b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3f13b-106">ByResourceId</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f13b-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="3f13b-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f13b-108">설명</span><span class="sxs-lookup"><span data-stu-id="3f13b-108">DESCRIPTION</span></span>
<span data-ttu-id="3f13b-109">**Stop-AzDataFactoryV2IntegrationRuntime** cmdlet은 관리되는 전용 통합 런타임이 '시작' 상태로 중지됩니다. 이 런타임은 Start-AzDataFactoryV2IntegrationRuntime cmdlet에서 시작했습니다.</span><span class="sxs-lookup"><span data-stu-id="3f13b-109">The **Stop-AzDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="3f13b-110">리소스가 릴리스된 후 상태가 '중지됨'으로 전송됩니다.</span><span class="sxs-lookup"><span data-stu-id="3f13b-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="3f13b-111">예제</span><span class="sxs-lookup"><span data-stu-id="3f13b-111">EXAMPLES</span></span>

### <span data-ttu-id="3f13b-112">예제 1: '시작' 상태인 관리되는 통합 런타임 중지</span><span class="sxs-lookup"><span data-stu-id="3f13b-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="3f13b-113">관리되는 통합 런타임 'test-reserlved-ir'은 '시작' 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="3f13b-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="3f13b-114">Stop-AzDataFactoryV2IntegrationRuntime cmdlet을 실행한 후 리소스가 릴리스되고 상태가 '중지됨'으로 전송됩니다.</span><span class="sxs-lookup"><span data-stu-id="3f13b-114">After running Stop-AzDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="3f13b-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3f13b-115">PARAMETERS</span></span>

### <span data-ttu-id="3f13b-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3f13b-116">-DataFactoryName</span></span>
<span data-ttu-id="3f13b-117">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f13b-117">The data factory name.</span></span>

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

### <span data-ttu-id="3f13b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f13b-118">-DefaultProfile</span></span>
<span data-ttu-id="3f13b-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3f13b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f13b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="3f13b-120">-Force</span></span>
<span data-ttu-id="3f13b-121">확인을 요청하지 않고 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="3f13b-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3f13b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f13b-122">-InputObject</span></span>
<span data-ttu-id="3f13b-123">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3f13b-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="3f13b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3f13b-124">-Name</span></span>
<span data-ttu-id="3f13b-125">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f13b-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="3f13b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f13b-126">-ResourceGroupName</span></span>
<span data-ttu-id="3f13b-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f13b-127">The resource group name.</span></span>

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

### <span data-ttu-id="3f13b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f13b-128">-ResourceId</span></span>
<span data-ttu-id="3f13b-129">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3f13b-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3f13b-130">-확인</span><span class="sxs-lookup"><span data-stu-id="3f13b-130">-Confirm</span></span>
<span data-ttu-id="3f13b-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3f13b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f13b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f13b-132">-WhatIf</span></span>
<span data-ttu-id="3f13b-133">cmdlet이 실행되지만 cmdlet을 실행하지 않는 경우 발생하는 것을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3f13b-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="3f13b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f13b-134">CommonParameters</span></span>
<span data-ttu-id="3f13b-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3f13b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f13b-136">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3f13b-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f13b-137">입력</span><span class="sxs-lookup"><span data-stu-id="3f13b-137">INPUTS</span></span>

### <span data-ttu-id="3f13b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="3f13b-138">System.String</span></span>

### <span data-ttu-id="3f13b-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3f13b-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="3f13b-140">출력</span><span class="sxs-lookup"><span data-stu-id="3f13b-140">OUTPUTS</span></span>

### <span data-ttu-id="3f13b-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="3f13b-141">System.Void</span></span>

## <span data-ttu-id="3f13b-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3f13b-142">NOTES</span></span>
<span data-ttu-id="3f13b-143">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리, 복사, 활동, 통합 런타임</span><span class="sxs-lookup"><span data-stu-id="3f13b-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="3f13b-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f13b-144">RELATED LINKS</span></span>

[<span data-ttu-id="3f13b-145">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3f13b-145">Start-AzDataFactoryV2IntegrationRuntime</span></span>]()
