---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 4c46ebfb5031d64e685a77768ef6d4c7353d8462
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531813"
---
# <span data-ttu-id="ec7f8-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="ec7f8-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="ec7f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec7f8-102">SYNOPSIS</span></span>
<span data-ttu-id="ec7f8-103">통합 런타임에서 지정 된 이름의 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7f8-103">Remove a node with the given name on an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec7f8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ec7f8-104">SYNTAX</span></span>

### <span data-ttu-id="ec7f8-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="ec7f8-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec7f8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ec7f8-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec7f8-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="ec7f8-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ec7f8-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ec7f8-108">DESCRIPTION</span></span>
<span data-ttu-id="ec7f8-109">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode cmdlet은 통합 런타임에서 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7f8-109">The Remove-AzureRmDataFactoryV2IntegrationRuntimeNode cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="ec7f8-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ec7f8-110">EXAMPLES</span></span>

### <span data-ttu-id="ec7f8-111">예제 1: 통합 런타임에서 노드 제거</span><span class="sxs-lookup"><span data-stu-id="ec7f8-111">Example 1: Remove a node from an integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="ec7f8-112">이 명령은 ' selfhost-eu2 ' 이라는 리소스 그룹에 대 한 구독의 ' dfv2-ir ' 이라는 통합 런타임에서 ' t e-t e m ' (이 하)의 ' Node_1 ' 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7f8-112">This command removes an node named 'Node_1' in the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="ec7f8-113">변수</span><span class="sxs-lookup"><span data-stu-id="ec7f8-113">PARAMETERS</span></span>

### <span data-ttu-id="ec7f8-114">-확인</span><span class="sxs-lookup"><span data-stu-id="ec7f8-114">-Confirm</span></span>
<span data-ttu-id="ec7f8-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7f8-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec7f8-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ec7f8-116">-DataFactoryName</span></span>
<span data-ttu-id="ec7f8-117">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec7f8-117">The data factory name.</span></span>

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

### <span data-ttu-id="ec7f8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ec7f8-118">-Force</span></span>
<span data-ttu-id="ec7f8-119">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7f8-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ec7f8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec7f8-120">-InputObject</span></span>
<span data-ttu-id="ec7f8-121">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ec7f8-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="ec7f8-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="ec7f8-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="ec7f8-123">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec7f8-123">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec7f8-124">-NodeName</span><span class="sxs-lookup"><span data-stu-id="ec7f8-124">-NodeName</span></span>
<span data-ttu-id="ec7f8-125">통합 런타임 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec7f8-125">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec7f8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec7f8-126">-ResourceGroupName</span></span>
<span data-ttu-id="ec7f8-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec7f8-127">The resource group name.</span></span>

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

### <span data-ttu-id="ec7f8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec7f8-128">-ResourceId</span></span>
<span data-ttu-id="ec7f8-129">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ec7f8-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ec7f8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec7f8-130">-WhatIf</span></span>
<span data-ttu-id="ec7f8-131">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ec7f8-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ec7f8-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec7f8-132">-DefaultProfile</span></span>
<span data-ttu-id="ec7f8-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec7f8-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec7f8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec7f8-134">CommonParameters</span></span>
<span data-ttu-id="ec7f8-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7f8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec7f8-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec7f8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec7f8-137">입력</span><span class="sxs-lookup"><span data-stu-id="ec7f8-137">INPUTS</span></span>

### <span data-ttu-id="ec7f8-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ec7f8-138">System.String</span></span>
<span data-ttu-id="ec7f8-139">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="ec7f8-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ec7f8-140">출력</span><span class="sxs-lookup"><span data-stu-id="ec7f8-140">OUTPUTS</span></span>

### <span data-ttu-id="ec7f8-141">System. 개체</span><span class="sxs-lookup"><span data-stu-id="ec7f8-141">System.Object</span></span>

## <span data-ttu-id="ec7f8-142">상속자</span><span class="sxs-lookup"><span data-stu-id="ec7f8-142">NOTES</span></span>

## <span data-ttu-id="ec7f8-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec7f8-143">RELATED LINKS</span></span>

