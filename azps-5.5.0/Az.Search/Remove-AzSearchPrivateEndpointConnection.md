---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: 341edce877666d56a78064f1e13dc7b7af9b26a1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205944"
---
# <span data-ttu-id="32193-101">Remove-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="32193-101">Remove-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="32193-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32193-102">SYNOPSIS</span></span>
<span data-ttu-id="32193-103">Azure Cognitive Search 서비스에서 개인 엔드포인트 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="32193-103">Remove the private endpoint connection from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="32193-104">구문</span><span class="sxs-lookup"><span data-stu-id="32193-104">SYNTAX</span></span>

### <span data-ttu-id="32193-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="32193-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32193-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32193-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection -ParentObject <PSSearchService> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32193-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32193-107">InputObjectParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection -InputObject <PSPrivateEndpointConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32193-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="32193-108">ResourceIdParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32193-109">설명</span><span class="sxs-lookup"><span data-stu-id="32193-109">DESCRIPTION</span></span>
<span data-ttu-id="32193-110">**Remove-AzSearchPrivateEndpointConnection은** Azure Cognitive Search 서비스에서 개인 엔드포인트 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="32193-110">The **Remove-AzSearchPrivateEndpointConnection** removes the private endpoint connection from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="32193-111">예제</span><span class="sxs-lookup"><span data-stu-id="32193-111">EXAMPLES</span></span>

### <span data-ttu-id="32193-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="32193-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266
```

<span data-ttu-id="32193-113">이 예제에서는 이름으로 검색 서비스에서 개인 엔드포인트 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="32193-113">This example removes a private endpoint connection from the search service by name.</span></span>

## <span data-ttu-id="32193-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32193-114">PARAMETERS</span></span>

### <span data-ttu-id="32193-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32193-115">-DefaultProfile</span></span>
<span data-ttu-id="32193-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="32193-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32193-117">-Force</span><span class="sxs-lookup"><span data-stu-id="32193-117">-Force</span></span>
<span data-ttu-id="32193-118">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="32193-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="32193-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32193-119">-InputObject</span></span>
<span data-ttu-id="32193-120">개인 엔드포인트 연결 입력 개체</span><span class="sxs-lookup"><span data-stu-id="32193-120">Private endpoint connection input object</span></span>

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

### <span data-ttu-id="32193-121">-Name</span><span class="sxs-lookup"><span data-stu-id="32193-121">-Name</span></span>
<span data-ttu-id="32193-122">Azure Cognitive Search 서비스 개인 엔드포인트 연결 이름</span><span class="sxs-lookup"><span data-stu-id="32193-122">Azure Cognitive Search Service private endpoint connection name</span></span>

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

### <span data-ttu-id="32193-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="32193-123">-ParentObject</span></span>
<span data-ttu-id="32193-124">Azure Cognitive Search 서비스 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="32193-124">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="32193-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32193-125">-PassThru</span></span>
<span data-ttu-id="32193-126">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="32193-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="32193-127">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="32193-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="32193-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32193-128">-ResourceGroupName</span></span>
<span data-ttu-id="32193-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32193-129">Resource Group name.</span></span>

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

### <span data-ttu-id="32193-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32193-130">-ResourceId</span></span>
<span data-ttu-id="32193-131">개인 링크 서비스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="32193-131">Private link service resource id</span></span>

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

### <span data-ttu-id="32193-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="32193-132">-ServiceName</span></span>
<span data-ttu-id="32193-133">Azure Cognitive Search 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32193-133">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="32193-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32193-134">-Confirm</span></span>
<span data-ttu-id="32193-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="32193-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32193-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32193-136">-WhatIf</span></span>
<span data-ttu-id="32193-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="32193-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32193-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="32193-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32193-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32193-139">CommonParameters</span></span>
<span data-ttu-id="32193-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="32193-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32193-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="32193-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32193-142">입력</span><span class="sxs-lookup"><span data-stu-id="32193-142">INPUTS</span></span>

### <span data-ttu-id="32193-143">없음</span><span class="sxs-lookup"><span data-stu-id="32193-143">None</span></span>

## <span data-ttu-id="32193-144">출력</span><span class="sxs-lookup"><span data-stu-id="32193-144">OUTPUTS</span></span>

### <span data-ttu-id="32193-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="32193-145">System.Boolean</span></span>

## <span data-ttu-id="32193-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="32193-146">NOTES</span></span>

## <span data-ttu-id="32193-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32193-147">RELATED LINKS</span></span>

[<span data-ttu-id="32193-148">Get-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="32193-148">Get-AzSearchPrivateEndpointConnection.md</span></span>](./Get-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="32193-149">Set-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="32193-149">Set-AzSearchPrivateEndpointConnection.md</span></span>](./Set-AzSearchPrivateEndpointConnection.md)