---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2integrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
ms.openlocfilehash: c7ffe4348d11658da6e7c9caeccaa14f17a6329b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879493"
---
# <span data-ttu-id="24793-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="24793-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="24793-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24793-102">SYNOPSIS</span></span>
<span data-ttu-id="24793-103">자체 호스팅 통합 런타임을 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="24793-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="24793-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24793-104">SYNTAX</span></span>

### <span data-ttu-id="24793-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="24793-105">ByIntegrationRuntimeName (Default)</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24793-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="24793-106">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24793-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="24793-107">ByIntegrationRuntimeObject</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24793-108">설명은</span><span class="sxs-lookup"><span data-stu-id="24793-108">DESCRIPTION</span></span>
<span data-ttu-id="24793-109">새 버전을 사용할 수 있는 경우 **AzDataFactoryV2IntegrationRuntimeUpgrade** cmdlet은 자체 호스트 된 통합 런타임을 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="24793-109">The **Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="24793-110">예제의</span><span class="sxs-lookup"><span data-stu-id="24793-110">EXAMPLES</span></span>

### <span data-ttu-id="24793-111">예제 1: 자체 호스팅 통합 런타임 업그레이드</span><span class="sxs-lookup"><span data-stu-id="24793-111">Example 1: Upgrades a self-hosted integration runtime</span></span>
```
PS C:\> Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="24793-112">Cmdlet이 ' selfhost-ir ' (data factory ' 테스트-df-eu2 ')의 자체 호스트 된 통합 런타임을 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="24793-112">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

## <span data-ttu-id="24793-113">변수</span><span class="sxs-lookup"><span data-stu-id="24793-113">PARAMETERS</span></span>

### <span data-ttu-id="24793-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="24793-114">-DataFactoryName</span></span>
<span data-ttu-id="24793-115">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24793-115">The data factory name.</span></span>

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

### <span data-ttu-id="24793-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24793-116">-DefaultProfile</span></span>
<span data-ttu-id="24793-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24793-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24793-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24793-118">-InputObject</span></span>
<span data-ttu-id="24793-119">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="24793-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="24793-120">-이름</span><span class="sxs-lookup"><span data-stu-id="24793-120">-Name</span></span>
<span data-ttu-id="24793-121">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24793-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="24793-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24793-122">-ResourceGroupName</span></span>
<span data-ttu-id="24793-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24793-123">The resource group name.</span></span>

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

### <span data-ttu-id="24793-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24793-124">-ResourceId</span></span>
<span data-ttu-id="24793-125">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="24793-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="24793-126">-확인</span><span class="sxs-lookup"><span data-stu-id="24793-126">-Confirm</span></span>
<span data-ttu-id="24793-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="24793-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24793-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24793-128">-WhatIf</span></span>
<span data-ttu-id="24793-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="24793-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24793-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24793-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24793-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24793-131">CommonParameters</span></span>
<span data-ttu-id="24793-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24793-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24793-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24793-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24793-134">입력</span><span class="sxs-lookup"><span data-stu-id="24793-134">INPUTS</span></span>

### <span data-ttu-id="24793-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="24793-135">System.String</span></span>

### <span data-ttu-id="24793-136">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="24793-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="24793-137">출력</span><span class="sxs-lookup"><span data-stu-id="24793-137">OUTPUTS</span></span>

### <span data-ttu-id="24793-138">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="24793-138">System.Void</span></span>

## <span data-ttu-id="24793-139">상속자</span><span class="sxs-lookup"><span data-stu-id="24793-139">NOTES</span></span>
<span data-ttu-id="24793-140">키워드: azure, azurerm, arm, resource, management, manager, data, 팩토리, 복사, 활동, 통합 런타임</span><span class="sxs-lookup"><span data-stu-id="24793-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="24793-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24793-141">RELATED LINKS</span></span>

<span data-ttu-id="24793-142">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="24793-142">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

