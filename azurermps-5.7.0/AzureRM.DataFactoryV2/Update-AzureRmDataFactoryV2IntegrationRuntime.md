---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/update-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: a66ed7e910b5b9fbd1057d50e2fa3e5058400855
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529870"
---
# <span data-ttu-id="22ff4-101">Update-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="22ff4-101">Update-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="22ff4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22ff4-102">SYNOPSIS</span></span>
<span data-ttu-id="22ff4-103">통합 런타임을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="22ff4-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22ff4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="22ff4-104">SYNTAX</span></span>

### <span data-ttu-id="22ff4-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="22ff4-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22ff4-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="22ff4-106">ByResourceId</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22ff4-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="22ff4-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22ff4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="22ff4-108">DESCRIPTION</span></span>
<span data-ttu-id="22ff4-109">**업데이트 AzureRmDataFactoryV2IntegrationRuntime** cmdlet은 통합 런타임 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="22ff4-109">The **Update-AzureRmDataFactoryV2IntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="22ff4-110">현재 cmdlet은 자체 호스팅 통합 런타임으로 ' 자동 업데이트 ' 및 ' AutoUpdateDelayOffset ' 업데이트가 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="22ff4-110">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="22ff4-111">예제의</span><span class="sxs-lookup"><span data-stu-id="22ff4-111">EXAMPLES</span></span>

### <span data-ttu-id="22ff4-112">예제 1: 통합 런타임 업데이트</span><span class="sxs-lookup"><span data-stu-id="22ff4-112">Example 1: Updates an integration runtime</span></span>
```
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzureRmDataFactoryV2IntegrationRuntime `
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

<span data-ttu-id="22ff4-113">Cmdlet은 ' selfhost-ir ' 이라는 이름의 자체 호스팅된 통합 런타임을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="22ff4-113">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="22ff4-114">변수</span><span class="sxs-lookup"><span data-stu-id="22ff4-114">PARAMETERS</span></span>

### <span data-ttu-id="22ff4-115">-자동 업데이트</span><span class="sxs-lookup"><span data-stu-id="22ff4-115">-AutoUpdate</span></span>
<span data-ttu-id="22ff4-116">자체 호스팅 통합 런타임 자동 업데이트를 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22ff4-116">Enable or disable the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: On, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ff4-117">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="22ff4-117">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="22ff4-118">자체 호스팅된 통합 런타임 자동 업데이트에 대 한 일일 시간 (시간)입니다.</span><span class="sxs-lookup"><span data-stu-id="22ff4-118">The time in hour of the day for the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ff4-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="22ff4-119">-DataFactoryName</span></span>
<span data-ttu-id="22ff4-120">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22ff4-120">The data factory name.</span></span>

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

### <span data-ttu-id="22ff4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22ff4-121">-DefaultProfile</span></span>
<span data-ttu-id="22ff4-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="22ff4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ff4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22ff4-123">-InputObject</span></span>
<span data-ttu-id="22ff4-124">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="22ff4-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="22ff4-125">-이름</span><span class="sxs-lookup"><span data-stu-id="22ff4-125">-Name</span></span>
<span data-ttu-id="22ff4-126">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22ff4-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="22ff4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22ff4-127">-ResourceGroupName</span></span>
<span data-ttu-id="22ff4-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22ff4-128">The resource group name.</span></span>

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

### <span data-ttu-id="22ff4-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22ff4-129">-ResourceId</span></span>
<span data-ttu-id="22ff4-130">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="22ff4-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="22ff4-131">-확인</span><span class="sxs-lookup"><span data-stu-id="22ff4-131">-Confirm</span></span>
<span data-ttu-id="22ff4-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="22ff4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22ff4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22ff4-133">-WhatIf</span></span>
<span data-ttu-id="22ff4-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="22ff4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22ff4-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="22ff4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22ff4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22ff4-136">CommonParameters</span></span>
<span data-ttu-id="22ff4-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="22ff4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22ff4-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22ff4-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22ff4-139">입력</span><span class="sxs-lookup"><span data-stu-id="22ff4-139">INPUTS</span></span>

### <span data-ttu-id="22ff4-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="22ff4-140">System.String</span></span>
<span data-ttu-id="22ff4-141">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="22ff4-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="22ff4-142">출력</span><span class="sxs-lookup"><span data-stu-id="22ff4-142">OUTPUTS</span></span>

### <span data-ttu-id="22ff4-143">DataFactoryV2. PSSelfHostedIntegrationRuntimeStatus/.</span><span class="sxs-lookup"><span data-stu-id="22ff4-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="22ff4-144">상속자</span><span class="sxs-lookup"><span data-stu-id="22ff4-144">NOTES</span></span>
<span data-ttu-id="22ff4-145">키워드: azure, azurerm, arm, resource, management, manager, data, 팩토리, 복사, 활동, 통합 런타임</span><span class="sxs-lookup"><span data-stu-id="22ff4-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="22ff4-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22ff4-146">RELATED LINKS</span></span>

<span data-ttu-id="22ff4-147">[Set-AzureRmDataFactoryV2IntegrationRuntime]() 
 [Get-AzureRmDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="22ff4-147">[Set-AzureRmDataFactoryV2IntegrationRuntime]()
[Get-AzureRmDataFactoryV2IntegrationRuntime]()</span></span>

