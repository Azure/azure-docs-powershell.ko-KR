---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
ms.openlocfilehash: 8b6f27191ee92240a8dc9e5e8289fda72db856ab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340125"
---
# <span data-ttu-id="683a6-101">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="683a6-101">Get-AzApiManagementApi</span></span>

## <span data-ttu-id="683a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="683a6-102">SYNOPSIS</span></span>
<span data-ttu-id="683a6-103">API를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="683a6-103">Gets an API.</span></span>

## <span data-ttu-id="683a6-104">구문</span><span class="sxs-lookup"><span data-stu-id="683a6-104">SYNTAX</span></span>

### <span data-ttu-id="683a6-105">GetAllApis(기본값)</span><span class="sxs-lookup"><span data-stu-id="683a6-105">GetAllApis (Default)</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="683a6-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="683a6-106">GetByApiId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="683a6-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="683a6-107">GetByName</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="683a6-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="683a6-108">GetByProductId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="683a6-109">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="683a6-109">GetByGatewayId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="683a6-110">설명</span><span class="sxs-lookup"><span data-stu-id="683a6-110">DESCRIPTION</span></span>
<span data-ttu-id="683a6-111">**Get-AzApiManagementApi** cmdlet은 하나 이상의 Azure API Management API를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="683a6-111">The **Get-AzApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="683a6-112">예제</span><span class="sxs-lookup"><span data-stu-id="683a6-112">EXAMPLES</span></span>

### <span data-ttu-id="683a6-113">예제 1: 모든 관리 API를 얻게</span><span class="sxs-lookup"><span data-stu-id="683a6-113">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="683a6-114">이 명령은 지정된 컨텍스트에 대한 모든 API를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="683a6-114">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="683a6-115">예제 2: ID로 관리 API를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="683a6-115">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="683a6-116">이 명령은 지정된 ID로 API를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="683a6-116">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="683a6-117">예제 3: 이름으로 관리 API를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="683a6-117">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="683a6-118">이 명령은 지정된 이름의 API를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="683a6-118">This command gets the API with the specified name.</span></span>

### <span data-ttu-id="683a6-119">예제 4: GatewayId로 관리 API를 얻게</span><span class="sxs-lookup"><span data-stu-id="683a6-119">Example 4: Get a management API by GatewayId</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -GatewayId "g01"
```

<span data-ttu-id="683a6-120">이 명령은 지정된 GatewayId에 대한 API를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="683a6-120">This command gets the API for the specified GatewayId.</span></span>

## <span data-ttu-id="683a6-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="683a6-121">PARAMETERS</span></span>

### <span data-ttu-id="683a6-122">-ApiId</span><span class="sxs-lookup"><span data-stu-id="683a6-122">-ApiId</span></span>
<span data-ttu-id="683a6-123">얻을 API의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="683a6-123">Specifies the ID of the API to get.</span></span>

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

### <span data-ttu-id="683a6-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="683a6-124">-ApiRevision</span></span>
<span data-ttu-id="683a6-125">특정 API 개정의 개정 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="683a6-125">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="683a6-126">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="683a6-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="683a6-127">-Context</span><span class="sxs-lookup"><span data-stu-id="683a6-127">-Context</span></span>
<span data-ttu-id="683a6-128">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="683a6-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="683a6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="683a6-129">-DefaultProfile</span></span>
<span data-ttu-id="683a6-130">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="683a6-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="683a6-131">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="683a6-131">-GatewayId</span></span>
<span data-ttu-id="683a6-132">지정된 경우 모든 게이트웨이 API를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="683a6-132">If specified will try to get all Gateway APIs.</span></span>

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

### <span data-ttu-id="683a6-133">-Name</span><span class="sxs-lookup"><span data-stu-id="683a6-133">-Name</span></span>
<span data-ttu-id="683a6-134">얻을 API의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="683a6-134">Specifies the name of the API to get.</span></span>

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

### <span data-ttu-id="683a6-135">-ProductId</span><span class="sxs-lookup"><span data-stu-id="683a6-135">-ProductId</span></span>
<span data-ttu-id="683a6-136">API를 얻을 제품의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="683a6-136">Specifies the ID of the product for which to get the API.</span></span>

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

### <span data-ttu-id="683a6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="683a6-137">CommonParameters</span></span>
<span data-ttu-id="683a6-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="683a6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="683a6-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="683a6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="683a6-140">입력</span><span class="sxs-lookup"><span data-stu-id="683a6-140">INPUTS</span></span>

### <span data-ttu-id="683a6-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="683a6-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="683a6-142">System.String</span><span class="sxs-lookup"><span data-stu-id="683a6-142">System.String</span></span>

## <span data-ttu-id="683a6-143">출력</span><span class="sxs-lookup"><span data-stu-id="683a6-143">OUTPUTS</span></span>

### <span data-ttu-id="683a6-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="683a6-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="683a6-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="683a6-145">NOTES</span></span>

## <span data-ttu-id="683a6-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="683a6-146">RELATED LINKS</span></span>

[<span data-ttu-id="683a6-147">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="683a6-147">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="683a6-148">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="683a6-148">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="683a6-149">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="683a6-149">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="683a6-150">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="683a6-150">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="683a6-151">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="683a6-151">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


