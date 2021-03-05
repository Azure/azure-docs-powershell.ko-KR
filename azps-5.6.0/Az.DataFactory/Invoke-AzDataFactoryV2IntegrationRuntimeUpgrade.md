---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/invoke-azdatafactoryv2integrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
ms.openlocfilehash: 941e820bb1c274a74cc52042b80cdf1b259a34b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975099"
---
# <span data-ttu-id="0ce82-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="0ce82-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="0ce82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ce82-102">SYNOPSIS</span></span>
<span data-ttu-id="0ce82-103">자체 호스팅 통합 런타임을 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="0ce82-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="0ce82-104">구문</span><span class="sxs-lookup"><span data-stu-id="0ce82-104">SYNTAX</span></span>

### <span data-ttu-id="0ce82-105">ByIntegrationRuntimeName(기본값)</span><span class="sxs-lookup"><span data-stu-id="0ce82-105">ByIntegrationRuntimeName (Default)</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0ce82-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0ce82-106">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ce82-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="0ce82-107">ByIntegrationRuntimeObject</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ce82-108">설명</span><span class="sxs-lookup"><span data-stu-id="0ce82-108">DESCRIPTION</span></span>
<span data-ttu-id="0ce82-109">**Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** cmdlet은 새 버전을 사용할 수 있는 경우 자체 호스팅 통합 런타임을 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="0ce82-109">The **Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="0ce82-110">예제</span><span class="sxs-lookup"><span data-stu-id="0ce82-110">EXAMPLES</span></span>

### <span data-ttu-id="0ce82-111">예제 1: 자체 호스팅 통합 런타임 업그레이드</span><span class="sxs-lookup"><span data-stu-id="0ce82-111">Example 1: Upgrades a self-hosted integration runtime</span></span>
```
PS C:\> Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="0ce82-112">cmdlet은 데이터 팩터리 'test-df-eu2'에서 'test-selfhost-ir'이라는 자체 호스팅 통합 런타임을 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="0ce82-112">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

## <span data-ttu-id="0ce82-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0ce82-113">PARAMETERS</span></span>

### <span data-ttu-id="0ce82-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0ce82-114">-DataFactoryName</span></span>
<span data-ttu-id="0ce82-115">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ce82-115">The data factory name.</span></span>

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

### <span data-ttu-id="0ce82-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ce82-116">-DefaultProfile</span></span>
<span data-ttu-id="0ce82-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ce82-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ce82-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ce82-118">-InputObject</span></span>
<span data-ttu-id="0ce82-119">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0ce82-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="0ce82-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0ce82-120">-Name</span></span>
<span data-ttu-id="0ce82-121">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ce82-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="0ce82-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ce82-122">-ResourceGroupName</span></span>
<span data-ttu-id="0ce82-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ce82-123">The resource group name.</span></span>

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

### <span data-ttu-id="0ce82-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ce82-124">-ResourceId</span></span>
<span data-ttu-id="0ce82-125">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0ce82-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0ce82-126">-확인</span><span class="sxs-lookup"><span data-stu-id="0ce82-126">-Confirm</span></span>
<span data-ttu-id="0ce82-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ce82-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ce82-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ce82-128">-WhatIf</span></span>
<span data-ttu-id="0ce82-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0ce82-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ce82-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ce82-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ce82-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ce82-131">CommonParameters</span></span>
<span data-ttu-id="0ce82-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0ce82-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ce82-133">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0ce82-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ce82-134">입력</span><span class="sxs-lookup"><span data-stu-id="0ce82-134">INPUTS</span></span>

### <span data-ttu-id="0ce82-135">System.String</span><span class="sxs-lookup"><span data-stu-id="0ce82-135">System.String</span></span>

### <span data-ttu-id="0ce82-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0ce82-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="0ce82-137">출력</span><span class="sxs-lookup"><span data-stu-id="0ce82-137">OUTPUTS</span></span>

### <span data-ttu-id="0ce82-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="0ce82-138">System.Void</span></span>

## <span data-ttu-id="0ce82-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0ce82-139">NOTES</span></span>
<span data-ttu-id="0ce82-140">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리, 복사, 활동, 통합 런타임</span><span class="sxs-lookup"><span data-stu-id="0ce82-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="0ce82-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ce82-141">RELATED LINKS</span></span>

<span data-ttu-id="0ce82-142">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="0ce82-142">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

