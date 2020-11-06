---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 83e6de07f7796e49732a35cfea4573002e6208df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532056"
---
# <span data-ttu-id="6d5b8-101">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6d5b8-101">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="6d5b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d5b8-102">SYNOPSIS</span></span>
<span data-ttu-id="6d5b8-103">통합 런타임 리소스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6d5b8-103">Gets information about integration runtime resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d5b8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6d5b8-104">SYNTAX</span></span>

### <span data-ttu-id="6d5b8-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="6d5b8-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d5b8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6d5b8-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d5b8-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="6d5b8-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d5b8-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6d5b8-108">DESCRIPTION</span></span>
<span data-ttu-id="6d5b8-109">Get-AzureRmDataFactoryV2IntegrationRuntime cmdlet은 data factory의 통합 런타임에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6d5b8-109">The Get-AzureRmDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="6d5b8-110">통합 런타임의 이름을 지정 하면이 cmdlet은 해당 통합 런타임에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6d5b8-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="6d5b8-111">이름을 지정 하지 않으면이 cmdlet은 데이터 팩터리의 모든 통합 런타임에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6d5b8-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="6d5b8-112">예제의</span><span class="sxs-lookup"><span data-stu-id="6d5b8-112">EXAMPLES</span></span>

### <span data-ttu-id="6d5b8-113">예제 1: 데이터 팩터리에 모든 통합 런타임 나열</span><span class="sxs-lookup"><span data-stu-id="6d5b8-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="6d5b8-114">' Eu2 ' 라는 데이터 팩터리의 모든 통합 런타임을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d5b8-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="6d5b8-115">예제 2: 관리 전용 통합 런타임 가져오기</span><span class="sxs-lookup"><span data-stu-id="6d5b8-115">Example 2: Get managed dedicated integration runtime</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir

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
    State                        : Starting
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="6d5b8-116">이 명령은 ' dfv2 ' (이) 라는 리소스 그룹의 구독에 대 한 ' 테스트 전용-ir ' 이라는 통합 런타임에 대 한 정보를 표시 하 고 ' test-df-eu2 ' 라는 data factory에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d5b8-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="6d5b8-117">예제 3: 세부 상태를 사용 하 여 관리 되는 전용 통합 런타임 가져오기</span><span class="sxs-lookup"><span data-stu-id="6d5b8-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir -Status

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
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="6d5b8-118">이 명령은 ' dfv2 ' (이) 라는 리소스 그룹의 구독에 대 한 ' 테스트 전용-ir ' 이라는 통합 런타임에 대 한 정보를 표시 하 고 ' test-df-eu2 ' 라는 data factory에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d5b8-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="6d5b8-119">예제 4: 자체 호스팅 통합 런타임 가져오기</span><span class="sxs-lookup"><span data-stu-id="6d5b8-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="6d5b8-120">이 명령은 ' dfv2 ' (이) 라는 리소스 그룹의 구독에 대 한 ' 테스트 전용-ir ' 이라는 통합 런타임에 대 한 정보를 표시 하 고 ' test-df-eu2 ' 라는 data factory에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d5b8-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="6d5b8-121">변수</span><span class="sxs-lookup"><span data-stu-id="6d5b8-121">PARAMETERS</span></span>

### <span data-ttu-id="6d5b8-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6d5b8-122">-DataFactoryName</span></span>
<span data-ttu-id="6d5b8-123">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d5b8-123">The data factory name.</span></span>

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

### <span data-ttu-id="6d5b8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d5b8-124">-DefaultProfile</span></span>
<span data-ttu-id="6d5b8-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6d5b8-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d5b8-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d5b8-126">-InputObject</span></span>
<span data-ttu-id="6d5b8-127">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6d5b8-127">The integration runtime object.</span></span>

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

### <span data-ttu-id="6d5b8-128">-이름</span><span class="sxs-lookup"><span data-stu-id="6d5b8-128">-Name</span></span>
<span data-ttu-id="6d5b8-129">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d5b8-129">The integration runtime name.</span></span>

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

### <span data-ttu-id="6d5b8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d5b8-130">-ResourceGroupName</span></span>
<span data-ttu-id="6d5b8-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d5b8-131">The resource group name.</span></span>

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

### <span data-ttu-id="6d5b8-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d5b8-132">-ResourceId</span></span>
<span data-ttu-id="6d5b8-133">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6d5b8-133">The Azure resource ID.</span></span>

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

### <span data-ttu-id="6d5b8-134">-상태</span><span class="sxs-lookup"><span data-stu-id="6d5b8-134">-Status</span></span>
<span data-ttu-id="6d5b8-135">통합 런타임 세부 정보 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="6d5b8-135">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="6d5b8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d5b8-136">CommonParameters</span></span>
<span data-ttu-id="6d5b8-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d5b8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d5b8-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d5b8-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d5b8-139">입력</span><span class="sxs-lookup"><span data-stu-id="6d5b8-139">INPUTS</span></span>

### <span data-ttu-id="6d5b8-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6d5b8-140">System.String</span></span>

### <span data-ttu-id="6d5b8-141">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="6d5b8-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="6d5b8-142">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6d5b8-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="6d5b8-143">출력</span><span class="sxs-lookup"><span data-stu-id="6d5b8-143">OUTPUTS</span></span>

### <span data-ttu-id="6d5b8-144">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="6d5b8-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="6d5b8-145">DataFactoryV2. PSManagedIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="6d5b8-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span></span>

### <span data-ttu-id="6d5b8-146">DataFactoryV2. PSSelfHostedIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="6d5b8-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

### <span data-ttu-id="6d5b8-147">DataFactoryV2. PSLinkedIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="6d5b8-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span></span>

## <span data-ttu-id="6d5b8-148">상속자</span><span class="sxs-lookup"><span data-stu-id="6d5b8-148">NOTES</span></span>
<span data-ttu-id="6d5b8-149">키워드: azure, azurerm, arm, resource, management, manager, data, 팩토리, 복사, 활동, 통합 런타임</span><span class="sxs-lookup"><span data-stu-id="6d5b8-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="6d5b8-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d5b8-150">RELATED LINKS</span></span>

[<span data-ttu-id="6d5b8-151">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6d5b8-151">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="6d5b8-152">제거-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6d5b8-152">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
