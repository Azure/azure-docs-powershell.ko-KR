---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 1fc86fe0cd8d36e0bfcc1790c4e47f83daef9909
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493503"
---
# <span data-ttu-id="33730-101">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="33730-101">Start-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="33730-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33730-102">SYNOPSIS</span></span>
<span data-ttu-id="33730-103">관리되는 전용 통합 런타임이 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="33730-103">Starts a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="33730-104">구문</span><span class="sxs-lookup"><span data-stu-id="33730-104">SYNTAX</span></span>

### <span data-ttu-id="33730-105">ByIntegrationRuntimeName(기본값)</span><span class="sxs-lookup"><span data-stu-id="33730-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33730-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="33730-106">ByResourceId</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33730-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="33730-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33730-108">설명</span><span class="sxs-lookup"><span data-stu-id="33730-108">DESCRIPTION</span></span>
<span data-ttu-id="33730-109">**Start-AzDataFactoryV2IntegrationRuntime** cmdlet은 관리되는 전용 통합 런타임을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="33730-109">The **Start-AzDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="33730-110">리소스가 프로비전된 후 작업 후에 상태가 '시작'됩니다.</span><span class="sxs-lookup"><span data-stu-id="33730-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="33730-111">예제</span><span class="sxs-lookup"><span data-stu-id="33730-111">EXAMPLES</span></span>

### <span data-ttu-id="33730-112">예제 1: 통합 런타임 시작</span><span class="sxs-lookup"><span data-stu-id="33730-112">Example 1: Start an integration runtime</span></span>
```
PS C:\> Start-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name test-dedicated-ir' -Force

    CreateTime                   : 9/11/2017 2:16:12 PM
    Nodes                        : {tvm-1650185656_1-20170911t141751z}
    OtherErrors                  : {}
    LastOperation                : 
    State                        : Started
    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : testsvr.database.windows.net
    CatalogAdminUserName         : admin
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    PublicIPs                    : 
    Id                           : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-dedicated-ir
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="33730-113">이 cmdlet은 'test-dedicated-ir'이라는 관리형 전용 통합 런타임이 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="33730-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="33730-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33730-114">PARAMETERS</span></span>

### <span data-ttu-id="33730-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="33730-115">-DataFactoryName</span></span>
<span data-ttu-id="33730-116">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33730-116">The data factory name.</span></span>

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

### <span data-ttu-id="33730-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33730-117">-DefaultProfile</span></span>
<span data-ttu-id="33730-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="33730-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33730-119">-Force</span><span class="sxs-lookup"><span data-stu-id="33730-119">-Force</span></span>
<span data-ttu-id="33730-120">확인 메시지를 표시하지 않고 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="33730-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="33730-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33730-121">-InputObject</span></span>
<span data-ttu-id="33730-122">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="33730-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="33730-123">-Name</span><span class="sxs-lookup"><span data-stu-id="33730-123">-Name</span></span>
<span data-ttu-id="33730-124">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33730-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="33730-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33730-125">-ResourceGroupName</span></span>
<span data-ttu-id="33730-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33730-126">The resource group name.</span></span>

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

### <span data-ttu-id="33730-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33730-127">-ResourceId</span></span>
<span data-ttu-id="33730-128">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="33730-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="33730-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33730-129">-Confirm</span></span>
<span data-ttu-id="33730-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="33730-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33730-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33730-131">-WhatIf</span></span>
<span data-ttu-id="33730-132">cmdlet이 실행되지만 cmdlet을 실행하지 않는 경우 발생하는 것을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="33730-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="33730-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33730-133">CommonParameters</span></span>
<span data-ttu-id="33730-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="33730-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33730-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="33730-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33730-136">입력</span><span class="sxs-lookup"><span data-stu-id="33730-136">INPUTS</span></span>

### <span data-ttu-id="33730-137">System.String</span><span class="sxs-lookup"><span data-stu-id="33730-137">System.String</span></span>

### <span data-ttu-id="33730-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="33730-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="33730-139">출력</span><span class="sxs-lookup"><span data-stu-id="33730-139">OUTPUTS</span></span>

### <span data-ttu-id="33730-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="33730-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="33730-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="33730-141">NOTES</span></span>

## <span data-ttu-id="33730-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33730-142">RELATED LINKS</span></span>

[<span data-ttu-id="33730-143">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="33730-143">Stop-AzDataFactoryV2IntegrationRuntime</span></span>]()
