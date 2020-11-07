---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 2b5f01047bf0b86fc885a01f0c58a9ab094f7698
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711903"
---
# <span data-ttu-id="982ce-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="982ce-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="982ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="982ce-102">SYNOPSIS</span></span>
<span data-ttu-id="982ce-103">관리 되는 전용 통합 런타임을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="982ce-103">Starts a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="982ce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="982ce-104">SYNTAX</span></span>

### <span data-ttu-id="982ce-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="982ce-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="982ce-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="982ce-106">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="982ce-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="982ce-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="982ce-108">설명은</span><span class="sxs-lookup"><span data-stu-id="982ce-108">DESCRIPTION</span></span>
<span data-ttu-id="982ce-109">**AzureRmDataFactoryV2IntegrationRuntime** cmdlet은 관리 되는 전용 통합 런타임을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="982ce-109">The **Start-AzureRmDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="982ce-110">리소스가 프로 비전 되 고 작업 후 상태가 ' 시작 됨 '이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="982ce-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="982ce-111">예제의</span><span class="sxs-lookup"><span data-stu-id="982ce-111">EXAMPLES</span></span>

### <span data-ttu-id="982ce-112">예제 1: 통합 런타임 시작</span><span class="sxs-lookup"><span data-stu-id="982ce-112">Example 1: Start an integration runtime</span></span>
```
PS C:\> Start-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name test-dedicated-ir' -Force

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
    Id                           : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-dedicated-ir
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="982ce-113">이 cmdlet은 ' 테스트 전용-ir ' 이라는 관리 전용 통합 런타임을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="982ce-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="982ce-114">변수</span><span class="sxs-lookup"><span data-stu-id="982ce-114">PARAMETERS</span></span>

### <span data-ttu-id="982ce-115">-확인</span><span class="sxs-lookup"><span data-stu-id="982ce-115">-Confirm</span></span>
<span data-ttu-id="982ce-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="982ce-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="982ce-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="982ce-117">-DataFactoryName</span></span>
<span data-ttu-id="982ce-118">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="982ce-118">The data factory name.</span></span>

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

### <span data-ttu-id="982ce-119">-Force</span><span class="sxs-lookup"><span data-stu-id="982ce-119">-Force</span></span>
<span data-ttu-id="982ce-120">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="982ce-120">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="982ce-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="982ce-121">-InputObject</span></span>
<span data-ttu-id="982ce-122">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="982ce-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="982ce-123">-이름</span><span class="sxs-lookup"><span data-stu-id="982ce-123">-Name</span></span>
<span data-ttu-id="982ce-124">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="982ce-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="982ce-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="982ce-125">-ResourceGroupName</span></span>
<span data-ttu-id="982ce-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="982ce-126">The resource group name.</span></span>

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

### <span data-ttu-id="982ce-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="982ce-127">-ResourceId</span></span>
<span data-ttu-id="982ce-128">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="982ce-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="982ce-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="982ce-129">-WhatIf</span></span>
<span data-ttu-id="982ce-130">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="982ce-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="982ce-131">입력</span><span class="sxs-lookup"><span data-stu-id="982ce-131">INPUTS</span></span>

### <span data-ttu-id="982ce-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="982ce-132">System.String</span></span>
<span data-ttu-id="982ce-133">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="982ce-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="982ce-134">출력</span><span class="sxs-lookup"><span data-stu-id="982ce-134">OUTPUTS</span></span>

### <span data-ttu-id="982ce-135">DataFactoryV2. PSManagedIntegrationRuntimeStatus/.</span><span class="sxs-lookup"><span data-stu-id="982ce-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="982ce-136">상속자</span><span class="sxs-lookup"><span data-stu-id="982ce-136">NOTES</span></span>

## <span data-ttu-id="982ce-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="982ce-137">RELATED LINKS</span></span>
[<span data-ttu-id="982ce-138">중지-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="982ce-138">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
