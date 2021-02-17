---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: 3500cf71bb09bec4b204acc0bbf56f185f6ff647
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208365"
---
# <span data-ttu-id="1152c-101">Get-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1152c-101">Get-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="1152c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1152c-102">SYNOPSIS</span></span>
<span data-ttu-id="1152c-103">Azure Cognitive Search 서비스에 대한 개인 엔드포인트 연결을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1152c-103">Gets private endpoint connection(s) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="1152c-104">구문</span><span class="sxs-lookup"><span data-stu-id="1152c-104">SYNTAX</span></span>

### <span data-ttu-id="1152c-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1152c-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1152c-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1152c-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ParentObject] <PSSearchService> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1152c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1152c-107">ResourceIdParameterSet</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1152c-108">설명</span><span class="sxs-lookup"><span data-stu-id="1152c-108">DESCRIPTION</span></span>
<span data-ttu-id="1152c-109">**Get-AzSearchPrivateEndpointConnection** cmdlet은 Azure Cognitive Search 서비스에 대한 개인 엔드포인트 연결을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1152c-109">The **Get-AzSearchPrivateEndpointConnection** cmdlet gets the private endpoint connection(s) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="1152c-110">예제</span><span class="sxs-lookup"><span data-stu-id="1152c-110">EXAMPLES</span></span>

### <span data-ttu-id="1152c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="1152c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap

Name                                                          Id
----                                                          --
arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266 /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateEndpointConnections/arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266
```

<span data-ttu-id="1152c-112">이 예제에서는 Azure Cognitive Search 서비스에 대한 모든 개인 엔드포인트 연결을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1152c-112">The example gets all the private endpoint connections to the Azure Cognitive Search service.</span></span>

### <span data-ttu-id="1152c-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="1152c-113">Example 2</span></span>
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

<span data-ttu-id="1152c-114">이 예제에서는 Azure Cognitive Search 서비스로 이름별 특정 개인 엔드포인트 연결을 얻습니다(쉽게 읽을 수 있도록 JSON으로 변환).</span><span class="sxs-lookup"><span data-stu-id="1152c-114">The example gets a specific private endpoint connection by name (converted to JSON for ease of reading) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="1152c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1152c-115">PARAMETERS</span></span>

### <span data-ttu-id="1152c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1152c-116">-DefaultProfile</span></span>
<span data-ttu-id="1152c-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1152c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1152c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1152c-118">-Name</span></span>
<span data-ttu-id="1152c-119">Azure Cognitive Search 서비스 개인 엔드포인트 연결 이름</span><span class="sxs-lookup"><span data-stu-id="1152c-119">Azure Cognitive Search Service private endpoint connection name</span></span>

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

### <span data-ttu-id="1152c-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1152c-120">-ParentObject</span></span>
<span data-ttu-id="1152c-121">Azure Cognitive Search 서비스 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1152c-121">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="1152c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1152c-122">-ResourceGroupName</span></span>
<span data-ttu-id="1152c-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1152c-123">Resource Group name.</span></span>

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

### <span data-ttu-id="1152c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1152c-124">-ResourceId</span></span>
<span data-ttu-id="1152c-125">개인 링크 서비스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="1152c-125">Private link service resource id</span></span>

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

### <span data-ttu-id="1152c-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1152c-126">-ServiceName</span></span>
<span data-ttu-id="1152c-127">Azure Cognitive Search 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1152c-127">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="1152c-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1152c-128">-Confirm</span></span>
<span data-ttu-id="1152c-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1152c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1152c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1152c-130">-WhatIf</span></span>
<span data-ttu-id="1152c-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1152c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1152c-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1152c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1152c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1152c-133">CommonParameters</span></span>
<span data-ttu-id="1152c-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1152c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1152c-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1152c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1152c-136">입력</span><span class="sxs-lookup"><span data-stu-id="1152c-136">INPUTS</span></span>

### <span data-ttu-id="1152c-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="1152c-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="1152c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1152c-138">System.String</span></span>

## <span data-ttu-id="1152c-139">출력</span><span class="sxs-lookup"><span data-stu-id="1152c-139">OUTPUTS</span></span>

### <span data-ttu-id="1152c-140">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1152c-140">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span></span>

## <span data-ttu-id="1152c-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1152c-141">NOTES</span></span>

## <span data-ttu-id="1152c-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1152c-142">RELATED LINKS</span></span>

[<span data-ttu-id="1152c-143">Remove-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="1152c-143">Remove-AzSearchPrivateEndpointConnection.md</span></span>](./Remove-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="1152c-144">Set-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="1152c-144">Set-AzSearchPrivateEndpointConnection.md</span></span>](./Set-AzSearchPrivateEndpointConnection.md)
