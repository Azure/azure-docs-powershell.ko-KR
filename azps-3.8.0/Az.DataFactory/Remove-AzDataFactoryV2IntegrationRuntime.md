---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 0c24f77b51bcfc50ec11e211fc7f11b60e348221
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879421"
---
# <span data-ttu-id="4039f-101">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4039f-101">Remove-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="4039f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4039f-102">SYNOPSIS</span></span>
<span data-ttu-id="4039f-103">통합 런타임을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4039f-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="4039f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4039f-104">SYNTAX</span></span>

### <span data-ttu-id="4039f-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="4039f-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4039f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4039f-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4039f-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="4039f-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4039f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4039f-108">DESCRIPTION</span></span>
<span data-ttu-id="4039f-109">Remove-AzDataFactoryV2IntegrationRuntime cmdlet은 통합 런타임을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4039f-109">The Remove-AzDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="4039f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4039f-110">EXAMPLES</span></span>

### <span data-ttu-id="4039f-111">예제 1: 통합 런타임 제거</span><span class="sxs-lookup"><span data-stu-id="4039f-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="4039f-112">이 명령은 ' test-df ' 라는 데이터 팩터리에 ' test-reserved-ir ' 이라는 통합 런타임을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4039f-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="4039f-113">이 명령은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4039f-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="4039f-114">변수</span><span class="sxs-lookup"><span data-stu-id="4039f-114">PARAMETERS</span></span>

### <span data-ttu-id="4039f-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4039f-115">-DataFactoryName</span></span>
<span data-ttu-id="4039f-116">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4039f-116">The data factory name.</span></span>

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

### <span data-ttu-id="4039f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4039f-117">-DefaultProfile</span></span>
<span data-ttu-id="4039f-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4039f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4039f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4039f-119">-Force</span></span>
<span data-ttu-id="4039f-120">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4039f-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="4039f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4039f-121">-InputObject</span></span>
<span data-ttu-id="4039f-122">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4039f-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="4039f-123">-LinkedDataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4039f-123">-LinkedDataFactoryName</span></span>
<span data-ttu-id="4039f-124">연결 된 data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4039f-124">The linked data factory name.</span></span>

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

### <span data-ttu-id="4039f-125">-이름</span><span class="sxs-lookup"><span data-stu-id="4039f-125">-Name</span></span>
<span data-ttu-id="4039f-126">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4039f-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="4039f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4039f-127">-ResourceGroupName</span></span>
<span data-ttu-id="4039f-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4039f-128">The resource group name.</span></span>

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

### <span data-ttu-id="4039f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4039f-129">-ResourceId</span></span>
<span data-ttu-id="4039f-130">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4039f-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="4039f-131">-확인</span><span class="sxs-lookup"><span data-stu-id="4039f-131">-Confirm</span></span>
<span data-ttu-id="4039f-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4039f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4039f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4039f-133">-WhatIf</span></span>
<span data-ttu-id="4039f-134">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4039f-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="4039f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4039f-135">CommonParameters</span></span>
<span data-ttu-id="4039f-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4039f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4039f-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4039f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4039f-138">입력</span><span class="sxs-lookup"><span data-stu-id="4039f-138">INPUTS</span></span>

### <span data-ttu-id="4039f-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4039f-139">System.String</span></span>

### <span data-ttu-id="4039f-140">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="4039f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="4039f-141">출력</span><span class="sxs-lookup"><span data-stu-id="4039f-141">OUTPUTS</span></span>

### <span data-ttu-id="4039f-142">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="4039f-142">System.Void</span></span>

## <span data-ttu-id="4039f-143">상속자</span><span class="sxs-lookup"><span data-stu-id="4039f-143">NOTES</span></span>
<span data-ttu-id="4039f-144">키워드: azure, azurerm, arm, resource, management, manager, data, 팩토리, 복사, 활동, 통합 런타임</span><span class="sxs-lookup"><span data-stu-id="4039f-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="4039f-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4039f-145">RELATED LINKS</span></span>

[<span data-ttu-id="4039f-146">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4039f-146">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="4039f-147">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4039f-147">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

