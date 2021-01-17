---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/deny-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
ms.openlocfilehash: 159b320b24ff1e9ab1b4c71e6c374931ecfeffdd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339993"
---
# <span data-ttu-id="3c983-101">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3c983-101">Deny-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="3c983-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c983-102">SYNOPSIS</span></span>
<span data-ttu-id="3c983-103">개인 엔드포인트 연결을 거부합니다.</span><span class="sxs-lookup"><span data-stu-id="3c983-103">denies a private endpoint connection.</span></span>

## <span data-ttu-id="3c983-104">구문</span><span class="sxs-lookup"><span data-stu-id="3c983-104">SYNTAX</span></span>

### <span data-ttu-id="3c983-105">ByResourceId(기본값)</span><span class="sxs-lookup"><span data-stu-id="3c983-105">ByResourceId (Default)</span></span>
```
Deny-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c983-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="3c983-106">ByResource</span></span>
```
Deny-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
[-PrivateLinkResourceType <string>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c983-107">설명</span><span class="sxs-lookup"><span data-stu-id="3c983-107">DESCRIPTION</span></span>
<span data-ttu-id="3c983-108">**Deny-AzPrivateEndpointConnection** cmdlet은 개인 엔드포인트 연결을 거부합니다.</span><span class="sxs-lookup"><span data-stu-id="3c983-108">The **Deny-AzPrivateEndpointConnection** cmdlet denies a private endpoint connection.</span></span>

## <span data-ttu-id="3c983-109">예제</span><span class="sxs-lookup"><span data-stu-id="3c983-109">EXAMPLES</span></span>

### <span data-ttu-id="3c983-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3c983-110">Example 1</span></span>
```
Deny-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="3c983-111">이 예제에서는 개인 엔드포인트 연결을 거부합니다.</span><span class="sxs-lookup"><span data-stu-id="3c983-111">This example denies a private endpoint connection.</span></span>

## <span data-ttu-id="3c983-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c983-112">PARAMETERS</span></span>

### <span data-ttu-id="3c983-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c983-113">-DefaultProfile</span></span>
<span data-ttu-id="3c983-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3c983-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c983-115">-Description</span><span class="sxs-lookup"><span data-stu-id="3c983-115">-Description</span></span>
<span data-ttu-id="3c983-116">작업 이유입니다.</span><span class="sxs-lookup"><span data-stu-id="3c983-116">The reason of action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c983-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3c983-117">-Name</span></span>
<span data-ttu-id="3c983-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c983-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c983-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="3c983-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="3c983-120">개인 링크 리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="3c983-120">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c983-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c983-121">-ResourceGroupName</span></span>
<span data-ttu-id="3c983-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c983-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c983-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c983-123">-ResourceId</span></span>
<span data-ttu-id="3c983-124">개인 엔드포인트 연결의 Azure Resource Manager ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3c983-124">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c983-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3c983-125">-ServiceName</span></span>
<span data-ttu-id="3c983-126">개인 엔드포인트 연결이 속한 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c983-126">The name of service that private endpoint connection belong to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c983-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c983-127">CommonParameters</span></span>
<span data-ttu-id="3c983-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3c983-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c983-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3c983-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c983-130">입력</span><span class="sxs-lookup"><span data-stu-id="3c983-130">INPUTS</span></span>

### <span data-ttu-id="3c983-131">System.String</span><span class="sxs-lookup"><span data-stu-id="3c983-131">System.String</span></span>

## <span data-ttu-id="3c983-132">출력</span><span class="sxs-lookup"><span data-stu-id="3c983-132">OUTPUTS</span></span>

### <span data-ttu-id="3c983-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3c983-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="3c983-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3c983-134">NOTES</span></span>

## <span data-ttu-id="3c983-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3c983-135">RELATED LINKS</span></span>

[<span data-ttu-id="3c983-136">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3c983-136">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="3c983-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3c983-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="3c983-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3c983-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="3c983-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3c983-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)