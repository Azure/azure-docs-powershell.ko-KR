---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: a2515b3713f449d25963af5952e233117e078ba9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525176"
---
# <span data-ttu-id="d5cd0-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d5cd0-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="d5cd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5cd0-102">SYNOPSIS</span></span>
<span data-ttu-id="d5cd0-103">통합 런타임을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5cd0-103">Removes an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5cd0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d5cd0-104">SYNTAX</span></span>

### <span data-ttu-id="d5cd0-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d5cd0-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5cd0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d5cd0-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5cd0-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="d5cd0-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5cd0-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d5cd0-108">DESCRIPTION</span></span>
<span data-ttu-id="d5cd0-109">Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet은 통합 런타임을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5cd0-109">The Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="d5cd0-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d5cd0-110">EXAMPLES</span></span>

### <span data-ttu-id="d5cd0-111">예제 1: 통합 런타임 제거</span><span class="sxs-lookup"><span data-stu-id="d5cd0-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="d5cd0-112">이 명령은 ' test-df ' 라는 데이터 팩터리에 ' test-reserved-ir ' 이라는 통합 런타임을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5cd0-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="d5cd0-113">이 명령은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5cd0-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="d5cd0-114">변수</span><span class="sxs-lookup"><span data-stu-id="d5cd0-114">PARAMETERS</span></span>

### <span data-ttu-id="d5cd0-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d5cd0-115">-DataFactoryName</span></span>
<span data-ttu-id="d5cd0-116">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5cd0-116">The data factory name.</span></span>

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

### <span data-ttu-id="d5cd0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5cd0-117">-DefaultProfile</span></span>
<span data-ttu-id="d5cd0-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d5cd0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5cd0-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d5cd0-119">-Force</span></span>
<span data-ttu-id="d5cd0-120">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5cd0-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d5cd0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5cd0-121">-InputObject</span></span>
<span data-ttu-id="d5cd0-122">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d5cd0-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="d5cd0-123">-이름</span><span class="sxs-lookup"><span data-stu-id="d5cd0-123">-Name</span></span>
<span data-ttu-id="d5cd0-124">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5cd0-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="d5cd0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5cd0-125">-ResourceGroupName</span></span>
<span data-ttu-id="d5cd0-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5cd0-126">The resource group name.</span></span>

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

### <span data-ttu-id="d5cd0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5cd0-127">-ResourceId</span></span>
<span data-ttu-id="d5cd0-128">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d5cd0-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d5cd0-129">-확인</span><span class="sxs-lookup"><span data-stu-id="d5cd0-129">-Confirm</span></span>
<span data-ttu-id="d5cd0-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5cd0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5cd0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5cd0-131">-WhatIf</span></span>
<span data-ttu-id="d5cd0-132">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d5cd0-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="d5cd0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5cd0-133">CommonParameters</span></span>
<span data-ttu-id="d5cd0-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5cd0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5cd0-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5cd0-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5cd0-136">입력</span><span class="sxs-lookup"><span data-stu-id="d5cd0-136">INPUTS</span></span>

### <span data-ttu-id="d5cd0-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d5cd0-137">System.String</span></span>
<span data-ttu-id="d5cd0-138">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="d5cd0-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="d5cd0-139">출력</span><span class="sxs-lookup"><span data-stu-id="d5cd0-139">OUTPUTS</span></span>

### <span data-ttu-id="d5cd0-140">System. 개체</span><span class="sxs-lookup"><span data-stu-id="d5cd0-140">System.Object</span></span>

## <span data-ttu-id="d5cd0-141">상속자</span><span class="sxs-lookup"><span data-stu-id="d5cd0-141">NOTES</span></span>
<span data-ttu-id="d5cd0-142">키워드: azure, azurerm, arm, resource, management, manager, data, 팩토리, 복사, 활동, 통합 런타임</span><span class="sxs-lookup"><span data-stu-id="d5cd0-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="d5cd0-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5cd0-143">RELATED LINKS</span></span>

[<span data-ttu-id="d5cd0-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d5cd0-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="d5cd0-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d5cd0-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

