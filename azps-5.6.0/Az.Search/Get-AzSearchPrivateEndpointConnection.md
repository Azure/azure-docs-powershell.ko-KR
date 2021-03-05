---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/get-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: 0ed07bed894d31be68b8fd4b71605e94b19171ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999787"
---
# <span data-ttu-id="55a80-101">Get-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="55a80-101">Get-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="55a80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55a80-102">SYNOPSIS</span></span>
<span data-ttu-id="55a80-103">Azure Cognitive Search 서비스에 대한 개인 엔드포인트 연결을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="55a80-103">Gets private endpoint connection(s) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="55a80-104">구문</span><span class="sxs-lookup"><span data-stu-id="55a80-104">SYNTAX</span></span>

### <span data-ttu-id="55a80-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="55a80-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55a80-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55a80-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ParentObject] <PSSearchService> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55a80-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55a80-107">ResourceIdParameterSet</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55a80-108">설명</span><span class="sxs-lookup"><span data-stu-id="55a80-108">DESCRIPTION</span></span>
<span data-ttu-id="55a80-109">**Get-AzSearchPrivateEndpointConnection** cmdlet은 Azure Cognitive Search 서비스에 대한 개인 엔드포인트 연결을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="55a80-109">The **Get-AzSearchPrivateEndpointConnection** cmdlet gets the private endpoint connection(s) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="55a80-110">예제</span><span class="sxs-lookup"><span data-stu-id="55a80-110">EXAMPLES</span></span>

### <span data-ttu-id="55a80-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="55a80-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap

Name                                                          Id
----                                                          --
arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266 /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateEndpointConnections/arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266
```

<span data-ttu-id="55a80-112">이 예제에서는 Azure Cognitive Search 서비스에 대한 모든 개인 엔드포인트 연결을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="55a80-112">The example gets all the private endpoint connections to the Azure Cognitive Search service.</span></span>

### <span data-ttu-id="55a80-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="55a80-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266  | ConvertTo-Json

{
  "Name": "arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateEndpointConnections/arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "PrivateEndpoint": {
    "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann2/providers/Microsoft.Network/privateEndpoints/arjagann-test-cuseuap-pe"
  },
  "PrivateLinkServiceConnectionState": {
    "Status": 1,
    "Description": "Auto-approved",
    "ActionsRequired": "None"
  }
}
```

<span data-ttu-id="55a80-114">이 예제에서는 이름별 특정 개인 엔드포인트 연결(읽기 용이성을 위해 JSON으로 변환)을 Azure Cognitive Search 서비스로 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="55a80-114">The example gets a specific private endpoint connection by name (converted to JSON for ease of reading) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="55a80-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="55a80-115">PARAMETERS</span></span>

### <span data-ttu-id="55a80-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55a80-116">-DefaultProfile</span></span>
<span data-ttu-id="55a80-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="55a80-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55a80-118">-Name</span><span class="sxs-lookup"><span data-stu-id="55a80-118">-Name</span></span>
<span data-ttu-id="55a80-119">Azure Cognitive Search Service 개인 엔드포인트 연결 이름</span><span class="sxs-lookup"><span data-stu-id="55a80-119">Azure Cognitive Search Service private endpoint connection name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55a80-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="55a80-120">-ParentObject</span></span>
<span data-ttu-id="55a80-121">Azure Cognitive Search Service 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="55a80-121">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55a80-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55a80-122">-ResourceGroupName</span></span>
<span data-ttu-id="55a80-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55a80-123">Resource Group name.</span></span>

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

### <span data-ttu-id="55a80-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55a80-124">-ResourceId</span></span>
<span data-ttu-id="55a80-125">개인 링크 서비스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="55a80-125">Private link service resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55a80-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="55a80-126">-ServiceName</span></span>
<span data-ttu-id="55a80-127">Azure Cognitive Search Service 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55a80-127">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="55a80-128">-확인</span><span class="sxs-lookup"><span data-stu-id="55a80-128">-Confirm</span></span>
<span data-ttu-id="55a80-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="55a80-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55a80-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55a80-130">-WhatIf</span></span>
<span data-ttu-id="55a80-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="55a80-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55a80-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="55a80-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55a80-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55a80-133">CommonParameters</span></span>
<span data-ttu-id="55a80-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="55a80-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55a80-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55a80-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55a80-136">입력</span><span class="sxs-lookup"><span data-stu-id="55a80-136">INPUTS</span></span>

### <span data-ttu-id="55a80-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="55a80-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="55a80-138">System.String</span><span class="sxs-lookup"><span data-stu-id="55a80-138">System.String</span></span>

## <span data-ttu-id="55a80-139">출력</span><span class="sxs-lookup"><span data-stu-id="55a80-139">OUTPUTS</span></span>

### <span data-ttu-id="55a80-140">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="55a80-140">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span></span>

## <span data-ttu-id="55a80-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="55a80-141">NOTES</span></span>

## <span data-ttu-id="55a80-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="55a80-142">RELATED LINKS</span></span>

[<span data-ttu-id="55a80-143">Remove-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="55a80-143">Remove-AzSearchPrivateEndpointConnection.md</span></span>](./Remove-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="55a80-144">Set-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="55a80-144">Set-AzSearchPrivateEndpointConnection.md</span></span>](./Set-AzSearchPrivateEndpointConnection.md)
