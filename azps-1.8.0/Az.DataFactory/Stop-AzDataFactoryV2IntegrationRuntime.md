---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 04e93db967a589c9dbcca4a88ed29d75f742ba7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868670"
---
# <span data-ttu-id="d9c7c-101">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d9c7c-101">Stop-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="d9c7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9c7c-102">SYNOPSIS</span></span>
<span data-ttu-id="d9c7c-103">관리 전용 통합 런타임을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9c7c-103">Stops a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="d9c7c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d9c7c-104">SYNTAX</span></span>

### <span data-ttu-id="d9c7c-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d9c7c-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9c7c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d9c7c-106">ByResourceId</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9c7c-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="d9c7c-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9c7c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d9c7c-108">DESCRIPTION</span></span>
<span data-ttu-id="d9c7c-109">**AzDataFactoryV2IntegrationRuntime** cmdlet은 ' 시작 됨 ' 상태의 관리 전용 통합 런타임을 중지 하며,이는 Start-AzDataFactoryV2IntegrationRuntime cmdlet에 의해 시작 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d9c7c-109">The **Stop-AzDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="d9c7c-110">리소스가 해제 되 고 상태가 ' 중지 됨 '으로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9c7c-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="d9c7c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d9c7c-111">EXAMPLES</span></span>

### <span data-ttu-id="d9c7c-112">예제 1: ' 시작 됨 ' 상태의 관리 되는 통합 런타임 중지</span><span class="sxs-lookup"><span data-stu-id="d9c7c-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="d9c7c-113">관리 되는 통합 런타임 ' 테스트-reserlved-ir '은 ' 시작 됨 ' 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="d9c7c-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="d9c7c-114">Stop-AzDataFactoryV2IntegrationRuntime cmdlet을 실행 한 후 리소스가 해제 되 고 상태가 ' 중지 됨 '으로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9c7c-114">After running Stop-AzDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="d9c7c-115">변수</span><span class="sxs-lookup"><span data-stu-id="d9c7c-115">PARAMETERS</span></span>

### <span data-ttu-id="d9c7c-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d9c7c-116">-DataFactoryName</span></span>
<span data-ttu-id="d9c7c-117">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d9c7c-117">The data factory name.</span></span>

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

### <span data-ttu-id="d9c7c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9c7c-118">-DefaultProfile</span></span>
<span data-ttu-id="d9c7c-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d9c7c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9c7c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d9c7c-120">-Force</span></span>
<span data-ttu-id="d9c7c-121">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9c7c-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d9c7c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9c7c-122">-InputObject</span></span>
<span data-ttu-id="d9c7c-123">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d9c7c-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="d9c7c-124">-이름</span><span class="sxs-lookup"><span data-stu-id="d9c7c-124">-Name</span></span>
<span data-ttu-id="d9c7c-125">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d9c7c-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="d9c7c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9c7c-126">-ResourceGroupName</span></span>
<span data-ttu-id="d9c7c-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d9c7c-127">The resource group name.</span></span>

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

### <span data-ttu-id="d9c7c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9c7c-128">-ResourceId</span></span>
<span data-ttu-id="d9c7c-129">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d9c7c-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d9c7c-130">-확인</span><span class="sxs-lookup"><span data-stu-id="d9c7c-130">-Confirm</span></span>
<span data-ttu-id="d9c7c-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9c7c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9c7c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9c7c-132">-WhatIf</span></span>
<span data-ttu-id="d9c7c-133">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d9c7c-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="d9c7c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9c7c-134">CommonParameters</span></span>
<span data-ttu-id="d9c7c-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9c7c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9c7c-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9c7c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9c7c-137">입력</span><span class="sxs-lookup"><span data-stu-id="d9c7c-137">INPUTS</span></span>

### <span data-ttu-id="d9c7c-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d9c7c-138">System.String</span></span>

### <span data-ttu-id="d9c7c-139">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="d9c7c-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="d9c7c-140">출력</span><span class="sxs-lookup"><span data-stu-id="d9c7c-140">OUTPUTS</span></span>

### <span data-ttu-id="d9c7c-141">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="d9c7c-141">System.Void</span></span>

## <span data-ttu-id="d9c7c-142">상속자</span><span class="sxs-lookup"><span data-stu-id="d9c7c-142">NOTES</span></span>
<span data-ttu-id="d9c7c-143">키워드: azure, azurerm, arm, resource, management, manager, data, 팩토리, 복사, 활동, 통합 런타임</span><span class="sxs-lookup"><span data-stu-id="d9c7c-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="d9c7c-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d9c7c-144">RELATED LINKS</span></span>

[<span data-ttu-id="d9c7c-145">시작-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d9c7c-145">Start-AzDataFactoryV2IntegrationRuntime</span></span>]()
