---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
ms.openlocfilehash: 8b6f27191ee92240a8dc9e5e8289fda72db856ab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307673"
---
# <span data-ttu-id="da58c-101">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="da58c-101">Get-AzApiManagementApi</span></span>

## <span data-ttu-id="da58c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da58c-102">SYNOPSIS</span></span>
<span data-ttu-id="da58c-103">API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="da58c-103">Gets an API.</span></span>

## <span data-ttu-id="da58c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="da58c-104">SYNTAX</span></span>

### <span data-ttu-id="da58c-105">GetAllApis (기본값)</span><span class="sxs-lookup"><span data-stu-id="da58c-105">GetAllApis (Default)</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da58c-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="da58c-106">GetByApiId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da58c-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="da58c-107">GetByName</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da58c-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="da58c-108">GetByProductId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da58c-109">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="da58c-109">GetByGatewayId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da58c-110">설명은</span><span class="sxs-lookup"><span data-stu-id="da58c-110">DESCRIPTION</span></span>
<span data-ttu-id="da58c-111">**AzApiManagementApi** cmdlet은 하나 이상의 Azure API 관리 api를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="da58c-111">The **Get-AzApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="da58c-112">예제의</span><span class="sxs-lookup"><span data-stu-id="da58c-112">EXAMPLES</span></span>

### <span data-ttu-id="da58c-113">예제 1: 모든 관리 Api 가져오기</span><span class="sxs-lookup"><span data-stu-id="da58c-113">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="da58c-114">이 명령은 지정 된 컨텍스트에 대 한 모든 Api를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="da58c-114">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="da58c-115">예제 2: ID로 관리 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="da58c-115">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="da58c-116">이 명령은 지정 된 ID의 API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="da58c-116">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="da58c-117">예제 3: 이름별로 관리 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="da58c-117">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="da58c-118">이 명령은 지정 된 이름의 API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="da58c-118">This command gets the API with the specified name.</span></span>

### <span data-ttu-id="da58c-119">예제 4: GatewayId로 관리 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="da58c-119">Example 4: Get a management API by GatewayId</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -GatewayId "g01"
```

<span data-ttu-id="da58c-120">이 명령은 지정 된 GatewayId에 대 한 API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="da58c-120">This command gets the API for the specified GatewayId.</span></span>

## <span data-ttu-id="da58c-121">변수</span><span class="sxs-lookup"><span data-stu-id="da58c-121">PARAMETERS</span></span>

### <span data-ttu-id="da58c-122">-ApiId</span><span class="sxs-lookup"><span data-stu-id="da58c-122">-ApiId</span></span>
<span data-ttu-id="da58c-123">가져올 API의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da58c-123">Specifies the ID of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da58c-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="da58c-124">-ApiRevision</span></span>
<span data-ttu-id="da58c-125">특정 Api 개정판의 수정 버전 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="da58c-125">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="da58c-126">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="da58c-126">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da58c-127">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="da58c-127">-Context</span></span>
<span data-ttu-id="da58c-128">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da58c-128">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da58c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da58c-129">-DefaultProfile</span></span>
<span data-ttu-id="da58c-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="da58c-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da58c-131">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="da58c-131">-GatewayId</span></span>
<span data-ttu-id="da58c-132">지정 된 경우 모든 게이트웨이 Api 가져오기를 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="da58c-132">If specified will try to get all Gateway APIs.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da58c-133">-이름</span><span class="sxs-lookup"><span data-stu-id="da58c-133">-Name</span></span>
<span data-ttu-id="da58c-134">가져올 API의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da58c-134">Specifies the name of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da58c-135">-ProductId</span><span class="sxs-lookup"><span data-stu-id="da58c-135">-ProductId</span></span>
<span data-ttu-id="da58c-136">API를 가져올 제품의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da58c-136">Specifies the ID of the product for which to get the API.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da58c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da58c-137">CommonParameters</span></span>
<span data-ttu-id="da58c-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="da58c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da58c-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="da58c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da58c-140">입력</span><span class="sxs-lookup"><span data-stu-id="da58c-140">INPUTS</span></span>

### <span data-ttu-id="da58c-141">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="da58c-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="da58c-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="da58c-142">System.String</span></span>

## <span data-ttu-id="da58c-143">출력</span><span class="sxs-lookup"><span data-stu-id="da58c-143">OUTPUTS</span></span>

### <span data-ttu-id="da58c-144">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="da58c-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="da58c-145">상속자</span><span class="sxs-lookup"><span data-stu-id="da58c-145">NOTES</span></span>

## <span data-ttu-id="da58c-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da58c-146">RELATED LINKS</span></span>

[<span data-ttu-id="da58c-147">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="da58c-147">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="da58c-148">가져오기-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="da58c-148">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="da58c-149">새로운 AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="da58c-149">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="da58c-150">제거-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="da58c-150">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="da58c-151">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="da58c-151">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


