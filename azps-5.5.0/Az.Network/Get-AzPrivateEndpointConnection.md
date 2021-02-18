---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 102ee966ae8ed213f1ed00395612061d1b39a3eb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184729"
---
# <span data-ttu-id="f2093-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f2093-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="f2093-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2093-102">SYNOPSIS</span></span>
<span data-ttu-id="f2093-103">개인 엔드포인트 연결 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f2093-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="f2093-104">구문</span><span class="sxs-lookup"><span data-stu-id="f2093-104">SYNTAX</span></span>

### <span data-ttu-id="f2093-105">ByResourceId(기본값)</span><span class="sxs-lookup"><span data-stu-id="f2093-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2093-106">ByPrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="f2093-106">ByPrivateLinkResourceId</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2093-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="f2093-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] [-Name <String>] -ResourceGroupName <String>
 -ServiceName <String> [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2093-108">설명</span><span class="sxs-lookup"><span data-stu-id="f2093-108">DESCRIPTION</span></span>
<span data-ttu-id="f2093-109">**Get-AzPrivateEndpointConnection** cmdlet은 개인 엔드포인트 연결 리소스를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="f2093-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="f2093-110">예제</span><span class="sxs-lookup"><span data-stu-id="f2093-110">EXAMPLES</span></span>

### <span data-ttu-id="f2093-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f2093-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="f2093-112">이 예제에서는 Mysql이라는 SQL Server에 속한 모든 개인 엔드포인트 연결의 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f2093-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="f2093-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="f2093-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="f2093-114">이 예제에서는 MyPrivateEndpointConnection1이라는 개인 엔드포인트 연결을 MyPrivateLinkService라는 개인 링크 서비스에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="f2093-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="f2093-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2093-115">PARAMETERS</span></span>

### <span data-ttu-id="f2093-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2093-116">-DefaultProfile</span></span>
<span data-ttu-id="f2093-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f2093-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2093-118">-Description</span><span class="sxs-lookup"><span data-stu-id="f2093-118">-Description</span></span>
<span data-ttu-id="f2093-119">작업 이유입니다.</span><span class="sxs-lookup"><span data-stu-id="f2093-119">The reason of action.</span></span>

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

### <span data-ttu-id="f2093-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f2093-120">-Name</span></span>
<span data-ttu-id="f2093-121">개인 엔드포인트 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f2093-121">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="f2093-122">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="f2093-122">-PrivateLinkResourceId</span></span>
<span data-ttu-id="f2093-123">개인 엔드포인트 연결이 속한 개인 링크 리소스의 Azure Resource Manager ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f2093-123">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

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

### <span data-ttu-id="f2093-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="f2093-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="f2093-125">개인 링크 리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="f2093-125">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:
Accepted values: 

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2093-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2093-126">-ResourceGroupName</span></span>
<span data-ttu-id="f2093-127">개인 엔드포인트 연결의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f2093-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="f2093-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2093-128">-ResourceId</span></span>
<span data-ttu-id="f2093-129">개인 엔드포인트 연결의 Azure Resource Manager ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f2093-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="f2093-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f2093-130">-ServiceName</span></span>
<span data-ttu-id="f2093-131">개인 엔드포인트 연결이 속한 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f2093-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="f2093-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2093-132">CommonParameters</span></span>
<span data-ttu-id="f2093-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f2093-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2093-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f2093-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2093-135">입력</span><span class="sxs-lookup"><span data-stu-id="f2093-135">INPUTS</span></span>

### <span data-ttu-id="f2093-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f2093-136">System.String</span></span>

## <span data-ttu-id="f2093-137">출력</span><span class="sxs-lookup"><span data-stu-id="f2093-137">OUTPUTS</span></span>

### <span data-ttu-id="f2093-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f2093-138">System.Boolean</span></span>

## <span data-ttu-id="f2093-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f2093-139">NOTES</span></span>

## <span data-ttu-id="f2093-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2093-140">RELATED LINKS</span></span>

[<span data-ttu-id="f2093-141">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f2093-141">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="f2093-142">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f2093-142">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="f2093-143">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f2093-143">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="f2093-144">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f2093-144">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
