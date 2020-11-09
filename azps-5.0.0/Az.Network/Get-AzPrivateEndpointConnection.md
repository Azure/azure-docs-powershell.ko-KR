---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 102ee966ae8ed213f1ed00395612061d1b39a3eb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309613"
---
# <span data-ttu-id="33361-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="33361-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="33361-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33361-102">SYNOPSIS</span></span>
<span data-ttu-id="33361-103">개인 끝점 연결 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="33361-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="33361-104">구문과</span><span class="sxs-lookup"><span data-stu-id="33361-104">SYNTAX</span></span>

### <span data-ttu-id="33361-105">ByResourceId (기본값)</span><span class="sxs-lookup"><span data-stu-id="33361-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33361-106">ByPrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="33361-106">ByPrivateLinkResourceId</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33361-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="33361-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] [-Name <String>] -ResourceGroupName <String>
 -ServiceName <String> [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="33361-108">설명은</span><span class="sxs-lookup"><span data-stu-id="33361-108">DESCRIPTION</span></span>
<span data-ttu-id="33361-109">**Get-AzPrivateEndpointConnection** cmdlet은 개인 끝점 연결 리소스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="33361-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="33361-110">예제의</span><span class="sxs-lookup"><span data-stu-id="33361-110">EXAMPLES</span></span>

### <span data-ttu-id="33361-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="33361-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="33361-112">이 예제에서는 모든 개인 끝점 연결이 Mysql 이라는 sql server에 속하는 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="33361-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="33361-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="33361-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="33361-114">이 예제에서는 MyPrivateEndpointConnection1 라는 개인 끝점 연결을 MyPrivateLinkService 이라는 사설 링크 서비스에 속함이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="33361-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="33361-115">변수</span><span class="sxs-lookup"><span data-stu-id="33361-115">PARAMETERS</span></span>

### <span data-ttu-id="33361-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33361-116">-DefaultProfile</span></span>
<span data-ttu-id="33361-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="33361-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33361-118">-설명</span><span class="sxs-lookup"><span data-stu-id="33361-118">-Description</span></span>
<span data-ttu-id="33361-119">작업의 이유입니다.</span><span class="sxs-lookup"><span data-stu-id="33361-119">The reason of action.</span></span>

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

### <span data-ttu-id="33361-120">-이름</span><span class="sxs-lookup"><span data-stu-id="33361-120">-Name</span></span>
<span data-ttu-id="33361-121">개인 끝점 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33361-121">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="33361-122">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="33361-122">-PrivateLinkResourceId</span></span>
<span data-ttu-id="33361-123">개인 끝점 연결이 속한 개인 링크 리소스의 Azure resource manager id입니다.</span><span class="sxs-lookup"><span data-stu-id="33361-123">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

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

### <span data-ttu-id="33361-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="33361-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="33361-125">개인 링크 리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="33361-125">The private link resource type.</span></span>

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

### <span data-ttu-id="33361-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33361-126">-ResourceGroupName</span></span>
<span data-ttu-id="33361-127">개인 끝점 연결의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33361-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="33361-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33361-128">-ResourceId</span></span>
<span data-ttu-id="33361-129">개인 끝점 연결의 Azure resource manager id입니다.</span><span class="sxs-lookup"><span data-stu-id="33361-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="33361-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="33361-130">-ServiceName</span></span>
<span data-ttu-id="33361-131">개인 끝점 연결이 속한 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33361-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="33361-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33361-132">CommonParameters</span></span>
<span data-ttu-id="33361-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="33361-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33361-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="33361-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33361-135">입력</span><span class="sxs-lookup"><span data-stu-id="33361-135">INPUTS</span></span>

### <span data-ttu-id="33361-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="33361-136">System.String</span></span>

## <span data-ttu-id="33361-137">출력</span><span class="sxs-lookup"><span data-stu-id="33361-137">OUTPUTS</span></span>

### <span data-ttu-id="33361-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="33361-138">System.Boolean</span></span>

## <span data-ttu-id="33361-139">상속자</span><span class="sxs-lookup"><span data-stu-id="33361-139">NOTES</span></span>

## <span data-ttu-id="33361-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33361-140">RELATED LINKS</span></span>

[<span data-ttu-id="33361-141">승인-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="33361-141">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="33361-142">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="33361-142">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="33361-143">제거-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="33361-143">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="33361-144">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="33361-144">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
