---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 5525dc4613fc1d6bccc56e27de065151b1890f7d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354446"
---
# <span data-ttu-id="f1265-101">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f1265-101">Get-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="f1265-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1265-102">SYNOPSIS</span></span>
<span data-ttu-id="f1265-103">통합 런타임 리소스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f1265-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="f1265-104">구문</span><span class="sxs-lookup"><span data-stu-id="f1265-104">SYNTAX</span></span>

### <span data-ttu-id="f1265-105">ByIntegrationRuntimeName(기본값)</span><span class="sxs-lookup"><span data-stu-id="f1265-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1265-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f1265-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1265-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="f1265-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1265-108">설명</span><span class="sxs-lookup"><span data-stu-id="f1265-108">DESCRIPTION</span></span>
<span data-ttu-id="f1265-109">Get-AzDataFactoryV2IntegrationRuntime cmdlet은 데이터 팩터리의 통합 런타임에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f1265-109">The Get-AzDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="f1265-110">통합 런타임의 이름을 지정하면 이 cmdlet은 해당 통합 런타임에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f1265-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="f1265-111">이름을 지정하지 않으면 이 cmdlet은 데이터 팩터리의 모든 통합 런타임에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f1265-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="f1265-112">예제</span><span class="sxs-lookup"><span data-stu-id="f1265-112">EXAMPLES</span></span>

### <span data-ttu-id="f1265-113">예제 1: 데이터 팩터리의 모든 통합 런타임 나열</span><span class="sxs-lookup"><span data-stu-id="f1265-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="f1265-114">'test-df-eu2'라는 데이터 팩터리의 모든 통합 런타임 나열</span><span class="sxs-lookup"><span data-stu-id="f1265-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="f1265-115">예제 2: 관리되는 전용 통합 런타임 얻기</span><span class="sxs-lookup"><span data-stu-id="f1265-115">Example 2: Get managed dedicated integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir

    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : test.database.windows.net
    CatalogAdminUserName         : test
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    PublicIPs                    : 
    State                        : Starting
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="f1265-116">이 명령은 'rg-test-dfv2'라는 리소스 그룹 및 'test-df-eu2'라는 데이터 팩터리에 대한 구독에서 'test-dedicated-ir'이라는 통합 런타임에 대한 정보를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="f1265-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="f1265-117">예제 3: 세부 정보를 통해 관리되는 전용 통합 런타임 얻기</span><span class="sxs-lookup"><span data-stu-id="f1265-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir -Status

    CreateTime                   : 
    Nodes                        : 
    OtherErrors                  : 
    LastOperation                : 
    State                        : Initial
    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : test.database.windows.net
    CatalogAdminUserName         : test
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    PublicIPs                    : 
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="f1265-118">이 명령은 'rg-test-dfv2'라는 리소스 그룹 및 'test-df-eu2'라는 데이터 팩터리에 대한 구독에서 'test-dedicated-ir'이라는 통합 런타임에 대한 정보를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="f1265-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="f1265-119">예제 4: 자체 호스팅 통합 런타임 얻기</span><span class="sxs-lookup"><span data-stu-id="f1265-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="f1265-120">이 명령은 'rg-test-dfv2'라는 리소스 그룹 및 'test-df-eu2'라는 데이터 팩터리에 대한 구독에서 'test-dedicated-ir'이라는 통합 런타임에 대한 정보를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="f1265-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="f1265-121">예제 5: 세부 정보를 통해 자체 호스팅 통합 런타임 얻기</span><span class="sxs-lookup"><span data-stu-id="f1265-121">Example 5: Get self-hosted integration runtime with detail status</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir -Status

    State                     : Online
    Version                   : 4.2.7233.1
    CreateTime                : 9/26/2019 6:00:08 AM
    AutoUpdate                : Off
    ScheduledUpdateDate       :
    UpdateDelayOffset         : 03:00:00
    LocalTimeZoneOffset       : 08:00:00
    InternalChannelEncryption :
    Capabilities              : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
    ServiceUrls               : {}
    Nodes                     : {}
    Links                     : {}
    AutoUpdateETA             :
    LatestVersion             : 4.3.7265.1
    PushedVersion             : 4.3.7265.1
    TaskQueueId               : fe2d60b5-86f5-58bf-bdae-7ef698284088
    VersionStatus             : UpdateAvailable
    Name                      : test-selfhost-ir
    Type                      : SelfHosted
    ResourceGroupName         : rg-test-dfv2
    DataFactoryName           : test-df-eu2
    Description               :
    Id                        : /subscriptions/41fcbc45-c594-4152-a8f1-fcbcd6452aea/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
```

## <span data-ttu-id="f1265-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1265-122">PARAMETERS</span></span>

### <span data-ttu-id="f1265-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f1265-123">-DataFactoryName</span></span>
<span data-ttu-id="f1265-124">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1265-124">The data factory name.</span></span>

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

### <span data-ttu-id="f1265-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1265-125">-DefaultProfile</span></span>
<span data-ttu-id="f1265-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f1265-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1265-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1265-127">-InputObject</span></span>
<span data-ttu-id="f1265-128">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f1265-128">The integration runtime object.</span></span>

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

### <span data-ttu-id="f1265-129">-Name</span><span class="sxs-lookup"><span data-stu-id="f1265-129">-Name</span></span>
<span data-ttu-id="f1265-130">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1265-130">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1265-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1265-131">-ResourceGroupName</span></span>
<span data-ttu-id="f1265-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1265-132">The resource group name.</span></span>

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

### <span data-ttu-id="f1265-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1265-133">-ResourceId</span></span>
<span data-ttu-id="f1265-134">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f1265-134">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f1265-135">-Status</span><span class="sxs-lookup"><span data-stu-id="f1265-135">-Status</span></span>
<span data-ttu-id="f1265-136">통합 런타임 세부 정보 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="f1265-136">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="f1265-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1265-137">CommonParameters</span></span>
<span data-ttu-id="f1265-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f1265-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1265-139">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f1265-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1265-140">입력</span><span class="sxs-lookup"><span data-stu-id="f1265-140">INPUTS</span></span>

### <span data-ttu-id="f1265-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f1265-141">System.String</span></span>

### <span data-ttu-id="f1265-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f1265-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="f1265-143">출력</span><span class="sxs-lookup"><span data-stu-id="f1265-143">OUTPUTS</span></span>

### <span data-ttu-id="f1265-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f1265-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="f1265-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f1265-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span></span>

### <span data-ttu-id="f1265-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f1265-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

### <span data-ttu-id="f1265-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f1265-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span></span>

## <span data-ttu-id="f1265-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f1265-148">NOTES</span></span>
<span data-ttu-id="f1265-149">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리, 복사, 활동, 통합 런타임</span><span class="sxs-lookup"><span data-stu-id="f1265-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="f1265-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1265-150">RELATED LINKS</span></span>

[<span data-ttu-id="f1265-151">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f1265-151">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="f1265-152">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f1265-152">Remove-AzDataFactoryV2IntegrationRuntime</span></span>]()
