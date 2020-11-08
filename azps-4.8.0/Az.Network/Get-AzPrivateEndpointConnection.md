---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 30b156a7adc972d06e514dd3d8d27c40f41194df
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204514"
---
# <span data-ttu-id="4fcc8-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4fcc8-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="4fcc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fcc8-102">SYNOPSIS</span></span>
<span data-ttu-id="4fcc8-103">개인 끝점 연결 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4fcc8-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="4fcc8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4fcc8-104">SYNTAX</span></span>

### <span data-ttu-id="4fcc8-105">ByPrivateLinkResourceId (기본값)</span><span class="sxs-lookup"><span data-stu-id="4fcc8-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fcc8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4fcc8-106">ByResourceId</span></span>
```
Get-AzPrivateEndpointConnection -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fcc8-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="4fcc8-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection -ServiceName <String> -ResourceGroupName <String>
[-Name <String>] [-PrivateLinkResourceType <String>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fcc8-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4fcc8-108">DESCRIPTION</span></span>
<span data-ttu-id="4fcc8-109">**Get-AzPrivateEndpointConnection** cmdlet은 개인 끝점 연결 리소스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fcc8-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="4fcc8-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4fcc8-110">EXAMPLES</span></span>

### <span data-ttu-id="4fcc8-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4fcc8-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="4fcc8-112">이 예제에서는 모든 개인 끝점 연결이 Mysql 이라는 sql server에 속하는 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fcc8-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="4fcc8-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="4fcc8-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="4fcc8-114">이 예제에서는 MyPrivateEndpointConnection1 라는 개인 끝점 연결을 MyPrivateLinkService 이라는 사설 링크 서비스에 속함이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4fcc8-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="4fcc8-115">변수</span><span class="sxs-lookup"><span data-stu-id="4fcc8-115">PARAMETERS</span></span>

### <span data-ttu-id="4fcc8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fcc8-116">-DefaultProfile</span></span>
<span data-ttu-id="4fcc8-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4fcc8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fcc8-118">-이름</span><span class="sxs-lookup"><span data-stu-id="4fcc8-118">-Name</span></span>
<span data-ttu-id="4fcc8-119">개인 끝점 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4fcc8-119">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fcc8-120">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="4fcc8-120">-PrivateLinkResourceId</span></span>
<span data-ttu-id="4fcc8-121">개인 끝점 연결이 속한 개인 링크 리소스의 Azure resource manager id입니다.</span><span class="sxs-lookup"><span data-stu-id="4fcc8-121">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPrivateLinkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fcc8-122">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="4fcc8-122">-PrivateLinkResourceType</span></span>
<span data-ttu-id="4fcc8-123">개인 링크 리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="4fcc8-123">The private link resource type.</span></span>

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

### <span data-ttu-id="4fcc8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fcc8-124">-ResourceGroupName</span></span>
<span data-ttu-id="4fcc8-125">개인 끝점 연결의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4fcc8-125">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="4fcc8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fcc8-126">-ResourceId</span></span>
<span data-ttu-id="4fcc8-127">개인 끝점 연결의 Azure resource manager id입니다.</span><span class="sxs-lookup"><span data-stu-id="4fcc8-127">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="4fcc8-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4fcc8-128">-ServiceName</span></span>
<span data-ttu-id="4fcc8-129">개인 끝점 연결이 속한 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4fcc8-129">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="4fcc8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fcc8-130">CommonParameters</span></span>
<span data-ttu-id="4fcc8-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fcc8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fcc8-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4fcc8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fcc8-133">입력</span><span class="sxs-lookup"><span data-stu-id="4fcc8-133">INPUTS</span></span>

### <span data-ttu-id="4fcc8-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4fcc8-134">System.String</span></span>

## <span data-ttu-id="4fcc8-135">출력</span><span class="sxs-lookup"><span data-stu-id="4fcc8-135">OUTPUTS</span></span>

### <span data-ttu-id="4fcc8-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="4fcc8-136">System.Boolean</span></span>

## <span data-ttu-id="4fcc8-137">상속자</span><span class="sxs-lookup"><span data-stu-id="4fcc8-137">NOTES</span></span>

## <span data-ttu-id="4fcc8-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4fcc8-138">RELATED LINKS</span></span>

[<span data-ttu-id="4fcc8-139">승인-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4fcc8-139">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="4fcc8-140">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4fcc8-140">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="4fcc8-141">제거-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4fcc8-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="4fcc8-142">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4fcc8-142">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
