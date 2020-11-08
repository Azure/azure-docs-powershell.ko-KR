---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/deny-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
ms.openlocfilehash: 159b320b24ff1e9ab1b4c71e6c374931ecfeffdd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056238"
---
# <span data-ttu-id="0ae31-101">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0ae31-101">Deny-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="0ae31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ae31-102">SYNOPSIS</span></span>
<span data-ttu-id="0ae31-103">개인 끝점 연결을 거부 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae31-103">denies a private endpoint connection.</span></span>

## <span data-ttu-id="0ae31-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0ae31-104">SYNTAX</span></span>

### <span data-ttu-id="0ae31-105">ByResourceId (기본값)</span><span class="sxs-lookup"><span data-stu-id="0ae31-105">ByResourceId (Default)</span></span>
```
Deny-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ae31-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="0ae31-106">ByResource</span></span>
```
Deny-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
[-PrivateLinkResourceType <string>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ae31-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0ae31-107">DESCRIPTION</span></span>
<span data-ttu-id="0ae31-108">**Deny-AzPrivateEndpointConnection** cmdlet은 개인 끝점 연결을 거부 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae31-108">The **Deny-AzPrivateEndpointConnection** cmdlet denies a private endpoint connection.</span></span>

## <span data-ttu-id="0ae31-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0ae31-109">EXAMPLES</span></span>

### <span data-ttu-id="0ae31-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="0ae31-110">Example 1</span></span>
```
Deny-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="0ae31-111">이 예제에서는 개인 끝점 연결을 거부 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae31-111">This example denies a private endpoint connection.</span></span>

## <span data-ttu-id="0ae31-112">변수</span><span class="sxs-lookup"><span data-stu-id="0ae31-112">PARAMETERS</span></span>

### <span data-ttu-id="0ae31-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ae31-113">-DefaultProfile</span></span>
<span data-ttu-id="0ae31-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae31-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ae31-115">-설명</span><span class="sxs-lookup"><span data-stu-id="0ae31-115">-Description</span></span>
<span data-ttu-id="0ae31-116">작업의 이유입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae31-116">The reason of action.</span></span>

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

### <span data-ttu-id="0ae31-117">-이름</span><span class="sxs-lookup"><span data-stu-id="0ae31-117">-Name</span></span>
<span data-ttu-id="0ae31-118">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae31-118">The resource name.</span></span>

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

### <span data-ttu-id="0ae31-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="0ae31-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="0ae31-120">개인 링크 리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae31-120">The private link resource type.</span></span>

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

### <span data-ttu-id="0ae31-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ae31-121">-ResourceGroupName</span></span>
<span data-ttu-id="0ae31-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae31-122">The resource group name.</span></span>

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

### <span data-ttu-id="0ae31-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ae31-123">-ResourceId</span></span>
<span data-ttu-id="0ae31-124">개인 끝점 연결의 Azure resource manager id입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae31-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="0ae31-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0ae31-125">-ServiceName</span></span>
<span data-ttu-id="0ae31-126">개인 끝점 연결이 속한 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae31-126">The name of service that private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="0ae31-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ae31-127">CommonParameters</span></span>
<span data-ttu-id="0ae31-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae31-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ae31-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0ae31-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ae31-130">입력</span><span class="sxs-lookup"><span data-stu-id="0ae31-130">INPUTS</span></span>

### <span data-ttu-id="0ae31-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0ae31-131">System.String</span></span>

## <span data-ttu-id="0ae31-132">출력</span><span class="sxs-lookup"><span data-stu-id="0ae31-132">OUTPUTS</span></span>

### <span data-ttu-id="0ae31-133">PSPrivateLinkService에 대 한.</span><span class="sxs-lookup"><span data-stu-id="0ae31-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="0ae31-134">상속자</span><span class="sxs-lookup"><span data-stu-id="0ae31-134">NOTES</span></span>

## <span data-ttu-id="0ae31-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ae31-135">RELATED LINKS</span></span>

[<span data-ttu-id="0ae31-136">승인-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0ae31-136">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="0ae31-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0ae31-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="0ae31-138">제거-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0ae31-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="0ae31-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0ae31-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)