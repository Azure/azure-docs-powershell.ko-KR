---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/start-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: eeb0db5c9dd180d8194d0bd506296f269c6c5386
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964896"
---
# <span data-ttu-id="505b7-101">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="505b7-101">Start-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="505b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="505b7-102">SYNOPSIS</span></span>
<span data-ttu-id="505b7-103">관리되는 전용 통합 런타임이 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="505b7-103">Starts a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="505b7-104">구문</span><span class="sxs-lookup"><span data-stu-id="505b7-104">SYNTAX</span></span>

### <span data-ttu-id="505b7-105">ByIntegrationRuntimeName(기본값)</span><span class="sxs-lookup"><span data-stu-id="505b7-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="505b7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="505b7-106">ByResourceId</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="505b7-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="505b7-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="505b7-108">설명</span><span class="sxs-lookup"><span data-stu-id="505b7-108">DESCRIPTION</span></span>
<span data-ttu-id="505b7-109">**Start-AzDataFactoryV2IntegrationRuntime** cmdlet은 관리되는 전용 통합 런타임을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="505b7-109">The **Start-AzDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="505b7-110">리소스가 프로비전된 후 작업 후에 상태가 '시작'입니다.</span><span class="sxs-lookup"><span data-stu-id="505b7-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="505b7-111">예제</span><span class="sxs-lookup"><span data-stu-id="505b7-111">EXAMPLES</span></span>

### <span data-ttu-id="505b7-112">예제 1: 통합 런타임 시작</span><span class="sxs-lookup"><span data-stu-id="505b7-112">Example 1: Start an integration runtime</span></span>
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

<span data-ttu-id="505b7-113">이 cmdlet은 'test-dedicated-ir'이라는 관리 전용 통합 런타임을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="505b7-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="505b7-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="505b7-114">PARAMETERS</span></span>

### <span data-ttu-id="505b7-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="505b7-115">-DataFactoryName</span></span>
<span data-ttu-id="505b7-116">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="505b7-116">The data factory name.</span></span>

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

### <span data-ttu-id="505b7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="505b7-117">-DefaultProfile</span></span>
<span data-ttu-id="505b7-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="505b7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="505b7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="505b7-119">-Force</span></span>
<span data-ttu-id="505b7-120">확인을 요청하지 않고 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="505b7-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="505b7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="505b7-121">-InputObject</span></span>
<span data-ttu-id="505b7-122">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="505b7-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="505b7-123">-Name</span><span class="sxs-lookup"><span data-stu-id="505b7-123">-Name</span></span>
<span data-ttu-id="505b7-124">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="505b7-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="505b7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="505b7-125">-ResourceGroupName</span></span>
<span data-ttu-id="505b7-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="505b7-126">The resource group name.</span></span>

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

### <span data-ttu-id="505b7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="505b7-127">-ResourceId</span></span>
<span data-ttu-id="505b7-128">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="505b7-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="505b7-129">-확인</span><span class="sxs-lookup"><span data-stu-id="505b7-129">-Confirm</span></span>
<span data-ttu-id="505b7-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="505b7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="505b7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="505b7-131">-WhatIf</span></span>
<span data-ttu-id="505b7-132">cmdlet이 실행되지만 cmdlet을 실행하지 않는 경우 발생하는 것을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="505b7-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="505b7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="505b7-133">CommonParameters</span></span>
<span data-ttu-id="505b7-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="505b7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="505b7-135">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="505b7-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="505b7-136">입력</span><span class="sxs-lookup"><span data-stu-id="505b7-136">INPUTS</span></span>

### <span data-ttu-id="505b7-137">System.String</span><span class="sxs-lookup"><span data-stu-id="505b7-137">System.String</span></span>

### <span data-ttu-id="505b7-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="505b7-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="505b7-139">출력</span><span class="sxs-lookup"><span data-stu-id="505b7-139">OUTPUTS</span></span>

### <span data-ttu-id="505b7-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="505b7-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="505b7-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="505b7-141">NOTES</span></span>

## <span data-ttu-id="505b7-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="505b7-142">RELATED LINKS</span></span>

[<span data-ttu-id="505b7-143">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="505b7-143">Stop-AzDataFactoryV2IntegrationRuntime</span></span>]()
