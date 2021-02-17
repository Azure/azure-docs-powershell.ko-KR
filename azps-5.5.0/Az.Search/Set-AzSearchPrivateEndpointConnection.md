---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: eda4cb403381bd41f7be471b91b2cbba3a6d2ad3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205920"
---
# <span data-ttu-id="f5774-101">Set-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f5774-101">Set-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="f5774-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5774-102">SYNOPSIS</span></span>
<span data-ttu-id="f5774-103">개인 엔드포인트 연결을 Azure Cognitive Search 서비스에 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f5774-103">Update the private endpoint connection to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="f5774-104">구문</span><span class="sxs-lookup"><span data-stu-id="f5774-104">SYNTAX</span></span>

### <span data-ttu-id="f5774-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f5774-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5774-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5774-106">ParentObjectParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection -ParentObject <PSSearchService> [-Name] <String>
 -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5774-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5774-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection [-ResourceId] <String> -Status <PSPrivateLinkServiceConnectionStatus>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5774-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5774-108">InputObjectParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 -InputObject <PSPrivateEndpointConnection> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5774-109">설명</span><span class="sxs-lookup"><span data-stu-id="f5774-109">DESCRIPTION</span></span>
<span data-ttu-id="f5774-110">**Set-AzSearchPrivateEndpointConnection은** 개인 엔드포인트 연결을 Azure Cognitive Search 서비스에 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f5774-110">The **Set-AzSearchPrivateEndpointConnection** updates the private endpoint connection to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="f5774-111">예제</span><span class="sxs-lookup"><span data-stu-id="f5774-111">EXAMPLES</span></span>

### <span data-ttu-id="f5774-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="f5774-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266 -Status Rejected  -Description "Rejected" | ConvertTo-Json

{
  "Name": "arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateEndpointConnections/arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "PrivateEndpoint": {
    "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann2/providers/Microsoft.Network/privateEndpoints/arjagann-test-cuseuap-pe"
  },
  "PrivateLinkServiceConnectionState": {
    "Status": 2,
    "Description": "Rejected",
    "ActionsRequired": "None"
  }
}
```

<span data-ttu-id="f5774-113">이 예제에서는 Azure Cognitive Search 서비스의 개인 엔드포인트 연결 상태를 "거부"로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f5774-113">This example updates a private endpoint connection's status of the Azure Cognitive Search service to be "Rejected".</span></span>

## <span data-ttu-id="f5774-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5774-114">PARAMETERS</span></span>

### <span data-ttu-id="f5774-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5774-115">-DefaultProfile</span></span>
<span data-ttu-id="f5774-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5774-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5774-117">-Description</span><span class="sxs-lookup"><span data-stu-id="f5774-117">-Description</span></span>
<span data-ttu-id="f5774-118">개인 엔드포인트 연결 설명</span><span class="sxs-lookup"><span data-stu-id="f5774-118">Private endpoint connection description</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5774-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5774-119">-InputObject</span></span>
<span data-ttu-id="f5774-120">개인 엔드포인트 연결 입력 개체</span><span class="sxs-lookup"><span data-stu-id="f5774-120">Private endpoint connection input object</span></span>

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

### <span data-ttu-id="f5774-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f5774-121">-Name</span></span>
<span data-ttu-id="f5774-122">Azure Cognitive Search 서비스 개인 엔드포인트 연결 이름</span><span class="sxs-lookup"><span data-stu-id="f5774-122">Azure Cognitive Search Service private endpoint connection name</span></span>

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

### <span data-ttu-id="f5774-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f5774-123">-ParentObject</span></span>
<span data-ttu-id="f5774-124">Azure Cognitive Search 서비스 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f5774-124">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="f5774-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5774-125">-ResourceGroupName</span></span>
<span data-ttu-id="f5774-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5774-126">Resource Group name.</span></span>

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

### <span data-ttu-id="f5774-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5774-127">-ResourceId</span></span>
<span data-ttu-id="f5774-128">개인 링크 서비스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="f5774-128">Private link service resource id</span></span>

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

### <span data-ttu-id="f5774-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f5774-129">-ServiceName</span></span>
<span data-ttu-id="f5774-130">Azure Cognitive Search 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5774-130">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="f5774-131">-Status</span><span class="sxs-lookup"><span data-stu-id="f5774-131">-Status</span></span>
<span data-ttu-id="f5774-132">개인 링크 서비스 연결 상태</span><span class="sxs-lookup"><span data-stu-id="f5774-132">Private link service connection status</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSPrivateLinkServiceConnectionStatus
Parameter Sets: (All)
Aliases:
Accepted values: Pending, Approved, Rejected, Disconnected

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5774-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5774-133">-Confirm</span></span>
<span data-ttu-id="f5774-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f5774-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5774-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5774-135">-WhatIf</span></span>
<span data-ttu-id="f5774-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f5774-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5774-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f5774-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5774-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5774-138">CommonParameters</span></span>
<span data-ttu-id="f5774-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f5774-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5774-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f5774-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5774-141">입력</span><span class="sxs-lookup"><span data-stu-id="f5774-141">INPUTS</span></span>

### <span data-ttu-id="f5774-142">System.String</span><span class="sxs-lookup"><span data-stu-id="f5774-142">System.String</span></span>

## <span data-ttu-id="f5774-143">출력</span><span class="sxs-lookup"><span data-stu-id="f5774-143">OUTPUTS</span></span>

### <span data-ttu-id="f5774-144">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f5774-144">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span></span>

## <span data-ttu-id="f5774-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f5774-145">NOTES</span></span>

## <span data-ttu-id="f5774-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5774-146">RELATED LINKS</span></span>

[<span data-ttu-id="f5774-147">Get-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="f5774-147">Get-AzSearchPrivateEndpointConnection.md</span></span>](./Get-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="f5774-148">Remove-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="f5774-148">Remove-AzSearchPrivateEndpointConnection.md</span></span>](./Remove-AzSearchPrivateEndpointConnection.md)
