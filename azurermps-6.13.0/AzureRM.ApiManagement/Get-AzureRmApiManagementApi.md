---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
ms.openlocfilehash: d84efcf68885e6d2e39ae15944c5f60298044ab7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526411"
---
# <span data-ttu-id="cd9d3-101">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cd9d3-101">Get-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="cd9d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd9d3-102">SYNOPSIS</span></span>
<span data-ttu-id="cd9d3-103">API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cd9d3-103">Gets an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd9d3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cd9d3-104">SYNTAX</span></span>

### <span data-ttu-id="cd9d3-105">GetAllApis (기본값)</span><span class="sxs-lookup"><span data-stu-id="cd9d3-105">GetAllApis (Default)</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cd9d3-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="cd9d3-106">GetByApiId</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd9d3-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="cd9d3-107">GetByName</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd9d3-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="cd9d3-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd9d3-109">설명은</span><span class="sxs-lookup"><span data-stu-id="cd9d3-109">DESCRIPTION</span></span>
<span data-ttu-id="cd9d3-110">**AzureRmApiManagementApi** cmdlet은 하나 이상의 Azure API 관리 api를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cd9d3-110">The **Get-AzureRmApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="cd9d3-111">예제의</span><span class="sxs-lookup"><span data-stu-id="cd9d3-111">EXAMPLES</span></span>

### <span data-ttu-id="cd9d3-112">예제 1: 모든 관리 Api 가져오기</span><span class="sxs-lookup"><span data-stu-id="cd9d3-112">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="cd9d3-113">이 명령은 지정 된 컨텍스트에 대 한 모든 Api를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cd9d3-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="cd9d3-114">예제 2: ID로 관리 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="cd9d3-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="cd9d3-115">이 명령은 지정 된 ID의 API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cd9d3-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="cd9d3-116">예제 3: 이름별로 관리 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="cd9d3-116">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="cd9d3-117">이 명령은 지정 된 이름의 API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cd9d3-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="cd9d3-118">변수</span><span class="sxs-lookup"><span data-stu-id="cd9d3-118">PARAMETERS</span></span>

### <span data-ttu-id="cd9d3-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="cd9d3-119">-ApiId</span></span>
<span data-ttu-id="cd9d3-120">가져올 API의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd9d3-120">Specifies the ID of the API to get.</span></span>

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

### <span data-ttu-id="cd9d3-121">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="cd9d3-121">-ApiRevision</span></span>
<span data-ttu-id="cd9d3-122">특정 Api 개정판의 수정 버전 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="cd9d3-122">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="cd9d3-123">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="cd9d3-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="cd9d3-124">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="cd9d3-124">-Context</span></span>
<span data-ttu-id="cd9d3-125">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd9d3-125">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd9d3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd9d3-126">-DefaultProfile</span></span>
<span data-ttu-id="cd9d3-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cd9d3-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd9d3-128">-이름</span><span class="sxs-lookup"><span data-stu-id="cd9d3-128">-Name</span></span>
<span data-ttu-id="cd9d3-129">가져올 API의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd9d3-129">Specifies the name of the API to get.</span></span>

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

### <span data-ttu-id="cd9d3-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="cd9d3-130">-ProductId</span></span>
<span data-ttu-id="cd9d3-131">API를 가져올 제품의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd9d3-131">Specifies the ID of the product for which to get the API.</span></span>

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

### <span data-ttu-id="cd9d3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd9d3-132">CommonParameters</span></span>
<span data-ttu-id="cd9d3-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd9d3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd9d3-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd9d3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd9d3-135">입력</span><span class="sxs-lookup"><span data-stu-id="cd9d3-135">INPUTS</span></span>

### <span data-ttu-id="cd9d3-136">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cd9d3-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cd9d3-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cd9d3-137">System.String</span></span>

## <span data-ttu-id="cd9d3-138">출력</span><span class="sxs-lookup"><span data-stu-id="cd9d3-138">OUTPUTS</span></span>

### <span data-ttu-id="cd9d3-139">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cd9d3-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="cd9d3-140">상속자</span><span class="sxs-lookup"><span data-stu-id="cd9d3-140">NOTES</span></span>

## <span data-ttu-id="cd9d3-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd9d3-141">RELATED LINKS</span></span>

[<span data-ttu-id="cd9d3-142">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cd9d3-142">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="cd9d3-143">가져오기-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cd9d3-143">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="cd9d3-144">새로운 AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cd9d3-144">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="cd9d3-145">제거-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cd9d3-145">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="cd9d3-146">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cd9d3-146">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


