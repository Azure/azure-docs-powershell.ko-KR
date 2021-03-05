---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/remove-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: 98b5f30bfe3a829d276c435c9beef71cf8a2f7de
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986631"
---
# <span data-ttu-id="c1c5f-101">Remove-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c1c5f-101">Remove-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="c1c5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1c5f-102">SYNOPSIS</span></span>
<span data-ttu-id="c1c5f-103">Azure Cognitive Search 서비스에서 개인 엔드포인트 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c1c5f-103">Remove the private endpoint connection from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="c1c5f-104">구문</span><span class="sxs-lookup"><span data-stu-id="c1c5f-104">SYNTAX</span></span>

### <span data-ttu-id="c1c5f-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c1c5f-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1c5f-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1c5f-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection -ParentObject <PSSearchService> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1c5f-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1c5f-107">InputObjectParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection -InputObject <PSPrivateEndpointConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1c5f-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1c5f-108">ResourceIdParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1c5f-109">설명</span><span class="sxs-lookup"><span data-stu-id="c1c5f-109">DESCRIPTION</span></span>
<span data-ttu-id="c1c5f-110">**Remove-AzSearchPrivateEndpointConnection은** Azure Cognitive Search 서비스에서 개인 엔드포인트 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c1c5f-110">The **Remove-AzSearchPrivateEndpointConnection** removes the private endpoint connection from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="c1c5f-111">예제</span><span class="sxs-lookup"><span data-stu-id="c1c5f-111">EXAMPLES</span></span>

### <span data-ttu-id="c1c5f-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="c1c5f-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266
```

<span data-ttu-id="c1c5f-113">이 예제에서는 이름으로 검색 서비스에서 개인 엔드포인트 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c1c5f-113">This example removes a private endpoint connection from the search service by name.</span></span>

## <span data-ttu-id="c1c5f-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c1c5f-114">PARAMETERS</span></span>

### <span data-ttu-id="c1c5f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1c5f-115">-DefaultProfile</span></span>
<span data-ttu-id="c1c5f-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c1c5f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1c5f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c1c5f-117">-Force</span></span>
<span data-ttu-id="c1c5f-118">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1c5f-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c1c5f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1c5f-119">-InputObject</span></span>
<span data-ttu-id="c1c5f-120">개인 엔드포인트 연결 입력 개체</span><span class="sxs-lookup"><span data-stu-id="c1c5f-120">Private endpoint connection input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1c5f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c1c5f-121">-Name</span></span>
<span data-ttu-id="c1c5f-122">Azure Cognitive Search Service 개인 엔드포인트 연결 이름</span><span class="sxs-lookup"><span data-stu-id="c1c5f-122">Azure Cognitive Search Service private endpoint connection name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1c5f-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c1c5f-123">-ParentObject</span></span>
<span data-ttu-id="c1c5f-124">Azure Cognitive Search Service 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c1c5f-124">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1c5f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1c5f-125">-PassThru</span></span>
<span data-ttu-id="c1c5f-126">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1c5f-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="c1c5f-127">이 스위치가 지정되어 있는 경우 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c1c5f-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="c1c5f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1c5f-128">-ResourceGroupName</span></span>
<span data-ttu-id="c1c5f-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c1c5f-129">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1c5f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1c5f-130">-ResourceId</span></span>
<span data-ttu-id="c1c5f-131">개인 링크 서비스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="c1c5f-131">Private link service resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1c5f-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c1c5f-132">-ServiceName</span></span>
<span data-ttu-id="c1c5f-133">Azure Cognitive Search Service 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c1c5f-133">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1c5f-134">-확인</span><span class="sxs-lookup"><span data-stu-id="c1c5f-134">-Confirm</span></span>
<span data-ttu-id="c1c5f-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1c5f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1c5f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1c5f-136">-WhatIf</span></span>
<span data-ttu-id="c1c5f-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c1c5f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1c5f-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1c5f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1c5f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1c5f-139">CommonParameters</span></span>
<span data-ttu-id="c1c5f-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c1c5f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1c5f-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1c5f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1c5f-142">입력</span><span class="sxs-lookup"><span data-stu-id="c1c5f-142">INPUTS</span></span>

### <span data-ttu-id="c1c5f-143">없음</span><span class="sxs-lookup"><span data-stu-id="c1c5f-143">None</span></span>

## <span data-ttu-id="c1c5f-144">출력</span><span class="sxs-lookup"><span data-stu-id="c1c5f-144">OUTPUTS</span></span>

### <span data-ttu-id="c1c5f-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c1c5f-145">System.Boolean</span></span>

## <span data-ttu-id="c1c5f-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c1c5f-146">NOTES</span></span>

## <span data-ttu-id="c1c5f-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c1c5f-147">RELATED LINKS</span></span>

[<span data-ttu-id="c1c5f-148">Get-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="c1c5f-148">Get-AzSearchPrivateEndpointConnection.md</span></span>](./Get-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="c1c5f-149">Set-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="c1c5f-149">Set-AzSearchPrivateEndpointConnection.md</span></span>](./Set-AzSearchPrivateEndpointConnection.md)