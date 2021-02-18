---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 487a4592217ac725fa46ef717c6e556cc433fcb4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200585"
---
# <span data-ttu-id="2c987-101">Update-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2c987-101">Update-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="2c987-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c987-102">SYNOPSIS</span></span>
<span data-ttu-id="2c987-103">통합 런타임 업데이트</span><span class="sxs-lookup"><span data-stu-id="2c987-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="2c987-104">구문</span><span class="sxs-lookup"><span data-stu-id="2c987-104">SYNTAX</span></span>

### <span data-ttu-id="2c987-105">ByIntegrationRuntimeName(기본값)</span><span class="sxs-lookup"><span data-stu-id="2c987-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c987-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2c987-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c987-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="2c987-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c987-108">설명</span><span class="sxs-lookup"><span data-stu-id="2c987-108">DESCRIPTION</span></span>
<span data-ttu-id="2c987-109">**Update-AzDataFactoryV2IntegrationRuntime** cmdlet은 통합 런타임 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2c987-109">The **Update-AzDataFactoryV2IntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="2c987-110">현재 cmdlet은 자체 호스팅 통합 런타임에 대해 'AutoUpdate' 및 'AutoUpdateDelayOffset' 업데이트만 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2c987-110">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="2c987-111">예제</span><span class="sxs-lookup"><span data-stu-id="2c987-111">EXAMPLES</span></span>

### <span data-ttu-id="2c987-112">예제 1: 통합 런타임 업데이트</span><span class="sxs-lookup"><span data-stu-id="2c987-112">Example 1: Updates an integration runtime</span></span>
```
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzDataFactoryV2IntegrationRuntime `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -Name 'test-selfhost-ir' `
    -AutoUpdate Off `
    -AutoUpdateDelayOffset $ts

Nodes                     : {Node_1}
CreateTime                : 11/18/2017 2:45:38 PM
InternalChannelEncryption : 
Version                   : 3.2.6519.3
Capabilities              : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
ScheduledUpdateDate       : 
UpdateDelayOffset         : 
LocalTimeZoneOffset       : 
AutoUpdate                : Off
ServiceUrls               : {wu.frontend.int.clouddatahub-int.net, *.servicebus.windows.net}
State                     : Online
Id                        : /subscriptions/41fcbc45-c594-4152-a8f1-fcbcd6452aea/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
Type                      : SelfHosted
ResourceGroupName         : rg-test-dfv2
DataFactoryName           : test-df-eu2
Name                      : test-selfhost-ir
Description               : New 2 description
```

<span data-ttu-id="2c987-113">cmdlet은 'test-selfhost-ir'이라는 자체 호스팅 통합 런타임을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2c987-113">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="2c987-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c987-114">PARAMETERS</span></span>

### <span data-ttu-id="2c987-115">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="2c987-115">-AutoUpdate</span></span>
<span data-ttu-id="2c987-116">자체 호스팅 통합 런타임 자동 업데이트를 사용하도록 설정하거나 해제합니다.</span><span class="sxs-lookup"><span data-stu-id="2c987-116">Enable or disable the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: On, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c987-117">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="2c987-117">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="2c987-118">자체 호스팅 통합 런타임 자동 업데이트에 대한 시간(시간)입니다.</span><span class="sxs-lookup"><span data-stu-id="2c987-118">The time in hour of the day for the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c987-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2c987-119">-DataFactoryName</span></span>
<span data-ttu-id="2c987-120">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c987-120">The data factory name.</span></span>

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

### <span data-ttu-id="2c987-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c987-121">-DefaultProfile</span></span>
<span data-ttu-id="2c987-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c987-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c987-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c987-123">-InputObject</span></span>
<span data-ttu-id="2c987-124">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2c987-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="2c987-125">-Name</span><span class="sxs-lookup"><span data-stu-id="2c987-125">-Name</span></span>
<span data-ttu-id="2c987-126">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c987-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="2c987-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c987-127">-ResourceGroupName</span></span>
<span data-ttu-id="2c987-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c987-128">The resource group name.</span></span>

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

### <span data-ttu-id="2c987-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c987-129">-ResourceId</span></span>
<span data-ttu-id="2c987-130">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2c987-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2c987-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c987-131">-Confirm</span></span>
<span data-ttu-id="2c987-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2c987-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c987-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c987-133">-WhatIf</span></span>
<span data-ttu-id="2c987-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2c987-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c987-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c987-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c987-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c987-136">CommonParameters</span></span>
<span data-ttu-id="2c987-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2c987-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c987-138">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2c987-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c987-139">입력</span><span class="sxs-lookup"><span data-stu-id="2c987-139">INPUTS</span></span>

### <span data-ttu-id="2c987-140">System.String</span><span class="sxs-lookup"><span data-stu-id="2c987-140">System.String</span></span>

### <span data-ttu-id="2c987-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2c987-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="2c987-142">출력</span><span class="sxs-lookup"><span data-stu-id="2c987-142">OUTPUTS</span></span>

### <span data-ttu-id="2c987-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="2c987-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="2c987-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2c987-144">NOTES</span></span>
<span data-ttu-id="2c987-145">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리, 복사, 활동, 통합 런타임</span><span class="sxs-lookup"><span data-stu-id="2c987-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="2c987-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c987-146">RELATED LINKS</span></span>

<span data-ttu-id="2c987-147">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="2c987-147">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

