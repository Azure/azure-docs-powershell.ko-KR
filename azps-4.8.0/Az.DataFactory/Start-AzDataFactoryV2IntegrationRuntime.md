---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 1fc86fe0cd8d36e0bfcc1790c4e47f83daef9909
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212837"
---
# <span data-ttu-id="948d9-101">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="948d9-101">Start-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="948d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="948d9-102">SYNOPSIS</span></span>
<span data-ttu-id="948d9-103">관리 되는 전용 통합 런타임을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="948d9-103">Starts a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="948d9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="948d9-104">SYNTAX</span></span>

### <span data-ttu-id="948d9-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="948d9-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="948d9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="948d9-106">ByResourceId</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="948d9-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="948d9-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="948d9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="948d9-108">DESCRIPTION</span></span>
<span data-ttu-id="948d9-109">**AzDataFactoryV2IntegrationRuntime** cmdlet은 관리 되는 전용 통합 런타임을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="948d9-109">The **Start-AzDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="948d9-110">리소스가 프로 비전 되 고 작업 후 상태가 ' 시작 됨 '이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="948d9-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="948d9-111">예제의</span><span class="sxs-lookup"><span data-stu-id="948d9-111">EXAMPLES</span></span>

### <span data-ttu-id="948d9-112">예제 1: 통합 런타임 시작</span><span class="sxs-lookup"><span data-stu-id="948d9-112">Example 1: Start an integration runtime</span></span>
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

<span data-ttu-id="948d9-113">이 cmdlet은 ' 테스트 전용-ir ' 이라는 관리 전용 통합 런타임을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="948d9-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="948d9-114">변수</span><span class="sxs-lookup"><span data-stu-id="948d9-114">PARAMETERS</span></span>

### <span data-ttu-id="948d9-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="948d9-115">-DataFactoryName</span></span>
<span data-ttu-id="948d9-116">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="948d9-116">The data factory name.</span></span>

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

### <span data-ttu-id="948d9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="948d9-117">-DefaultProfile</span></span>
<span data-ttu-id="948d9-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="948d9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="948d9-119">-Force</span><span class="sxs-lookup"><span data-stu-id="948d9-119">-Force</span></span>
<span data-ttu-id="948d9-120">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="948d9-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="948d9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="948d9-121">-InputObject</span></span>
<span data-ttu-id="948d9-122">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="948d9-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="948d9-123">-이름</span><span class="sxs-lookup"><span data-stu-id="948d9-123">-Name</span></span>
<span data-ttu-id="948d9-124">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="948d9-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="948d9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="948d9-125">-ResourceGroupName</span></span>
<span data-ttu-id="948d9-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="948d9-126">The resource group name.</span></span>

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

### <span data-ttu-id="948d9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="948d9-127">-ResourceId</span></span>
<span data-ttu-id="948d9-128">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="948d9-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="948d9-129">-확인</span><span class="sxs-lookup"><span data-stu-id="948d9-129">-Confirm</span></span>
<span data-ttu-id="948d9-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="948d9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="948d9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="948d9-131">-WhatIf</span></span>
<span data-ttu-id="948d9-132">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="948d9-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="948d9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="948d9-133">CommonParameters</span></span>
<span data-ttu-id="948d9-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="948d9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="948d9-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="948d9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="948d9-136">입력</span><span class="sxs-lookup"><span data-stu-id="948d9-136">INPUTS</span></span>

### <span data-ttu-id="948d9-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="948d9-137">System.String</span></span>

### <span data-ttu-id="948d9-138">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="948d9-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="948d9-139">출력</span><span class="sxs-lookup"><span data-stu-id="948d9-139">OUTPUTS</span></span>

### <span data-ttu-id="948d9-140">DataFactoryV2. PSManagedIntegrationRuntimeStatus/.</span><span class="sxs-lookup"><span data-stu-id="948d9-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="948d9-141">상속자</span><span class="sxs-lookup"><span data-stu-id="948d9-141">NOTES</span></span>

## <span data-ttu-id="948d9-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="948d9-142">RELATED LINKS</span></span>

[<span data-ttu-id="948d9-143">중지-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="948d9-143">Stop-AzDataFactoryV2IntegrationRuntime</span></span>]()
