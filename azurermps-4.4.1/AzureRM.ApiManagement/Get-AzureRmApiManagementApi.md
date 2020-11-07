---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
ms.openlocfilehash: 95784b084f6d106413c65b840dd73f313a47799e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711005"
---
# <span data-ttu-id="eeb25-101">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="eeb25-101">Get-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="eeb25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eeb25-102">SYNOPSIS</span></span>
<span data-ttu-id="eeb25-103">API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eeb25-103">Gets an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eeb25-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eeb25-104">SYNTAX</span></span>

### <span data-ttu-id="eeb25-105">모든 Api (기본값)</span><span class="sxs-lookup"><span data-stu-id="eeb25-105">All APIs (Default)</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eeb25-106">ID로 찾기</span><span class="sxs-lookup"><span data-stu-id="eeb25-106">Find by ID</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eeb25-107">이름으로 찾기</span><span class="sxs-lookup"><span data-stu-id="eeb25-107">Find by Name</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eeb25-108">제품 ID 기준으로 찾기</span><span class="sxs-lookup"><span data-stu-id="eeb25-108">Find by product ID</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eeb25-109">설명은</span><span class="sxs-lookup"><span data-stu-id="eeb25-109">DESCRIPTION</span></span>
<span data-ttu-id="eeb25-110">**AzureRmApiManagementApi** cmdlet은 하나 이상의 Azure API 관리 api를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eeb25-110">The **Get-AzureRmApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="eeb25-111">예제의</span><span class="sxs-lookup"><span data-stu-id="eeb25-111">EXAMPLES</span></span>

### <span data-ttu-id="eeb25-112">예제 1: 모든 관리 Api 가져오기</span><span class="sxs-lookup"><span data-stu-id="eeb25-112">Example 1: Get all management APIs</span></span>
```
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="eeb25-113">이 명령은 지정 된 컨텍스트에 대 한 모든 Api를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eeb25-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="eeb25-114">예제 2: ID로 관리 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="eeb25-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="eeb25-115">이 명령은 지정 된 ID의 API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eeb25-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="eeb25-116">예제 3: 이름별로 관리 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="eeb25-116">Example 3: Get a management API by name</span></span>
```
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="eeb25-117">이 명령은 지정 된 이름의 API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eeb25-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="eeb25-118">변수</span><span class="sxs-lookup"><span data-stu-id="eeb25-118">PARAMETERS</span></span>

### <span data-ttu-id="eeb25-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="eeb25-119">-ApiId</span></span>
<span data-ttu-id="eeb25-120">가져올 API의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eeb25-120">Specifies the ID of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb25-121">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="eeb25-121">-Context</span></span>
<span data-ttu-id="eeb25-122">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eeb25-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="eeb25-123">-이름</span><span class="sxs-lookup"><span data-stu-id="eeb25-123">-Name</span></span>
<span data-ttu-id="eeb25-124">가져올 API의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eeb25-124">Specifies the name of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by Name
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb25-125">-ProductId</span><span class="sxs-lookup"><span data-stu-id="eeb25-125">-ProductId</span></span>
<span data-ttu-id="eeb25-126">API를 가져올 제품의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eeb25-126">Specifies the ID of the product for which to get the API.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by product ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb25-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeb25-127">-DefaultProfile</span></span>
<span data-ttu-id="eeb25-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eeb25-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eeb25-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeb25-129">CommonParameters</span></span>
<span data-ttu-id="eeb25-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eeb25-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeb25-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeb25-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeb25-132">입력</span><span class="sxs-lookup"><span data-stu-id="eeb25-132">INPUTS</span></span>

## <span data-ttu-id="eeb25-133">출력</span><span class="sxs-lookup"><span data-stu-id="eeb25-133">OUTPUTS</span></span>

### <span data-ttu-id="eeb25-134">IList를<ApiManagement> ServiceManagement. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="eeb25-134">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi></span></span>

## <span data-ttu-id="eeb25-135">상속자</span><span class="sxs-lookup"><span data-stu-id="eeb25-135">NOTES</span></span>

## <span data-ttu-id="eeb25-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eeb25-136">RELATED LINKS</span></span>

[<span data-ttu-id="eeb25-137">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="eeb25-137">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="eeb25-138">가져오기-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="eeb25-138">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="eeb25-139">새로운 AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="eeb25-139">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="eeb25-140">제거-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="eeb25-140">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="eeb25-141">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="eeb25-141">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


