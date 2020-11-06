---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
ms.openlocfilehash: 435e167b713934962daf0cf27fc0d844caee8dcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527155"
---
# <span data-ttu-id="21a84-101">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="21a84-101">Get-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="21a84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21a84-102">SYNOPSIS</span></span>
<span data-ttu-id="21a84-103">API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="21a84-103">Gets an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21a84-104">구문과</span><span class="sxs-lookup"><span data-stu-id="21a84-104">SYNTAX</span></span>

### <span data-ttu-id="21a84-105">GetAllApis (기본값)</span><span class="sxs-lookup"><span data-stu-id="21a84-105">GetAllApis (Default)</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="21a84-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="21a84-106">GetByApiId</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21a84-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="21a84-107">GetByName</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21a84-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="21a84-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21a84-109">설명은</span><span class="sxs-lookup"><span data-stu-id="21a84-109">DESCRIPTION</span></span>
<span data-ttu-id="21a84-110">**AzureRmApiManagementApi** cmdlet은 하나 이상의 Azure API 관리 api를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="21a84-110">The **Get-AzureRmApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="21a84-111">예제의</span><span class="sxs-lookup"><span data-stu-id="21a84-111">EXAMPLES</span></span>

### <span data-ttu-id="21a84-112">예제 1: 모든 관리 Api 가져오기</span><span class="sxs-lookup"><span data-stu-id="21a84-112">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="21a84-113">이 명령은 지정 된 컨텍스트에 대 한 모든 Api를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="21a84-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="21a84-114">예제 2: ID로 관리 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="21a84-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="21a84-115">이 명령은 지정 된 ID의 API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="21a84-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="21a84-116">예제 3: 이름별로 관리 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="21a84-116">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="21a84-117">이 명령은 지정 된 이름의 API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="21a84-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="21a84-118">변수</span><span class="sxs-lookup"><span data-stu-id="21a84-118">PARAMETERS</span></span>

### <span data-ttu-id="21a84-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="21a84-119">-ApiId</span></span>
<span data-ttu-id="21a84-120">가져올 API의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21a84-120">Specifies the ID of the API to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByApiId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21a84-121">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="21a84-121">-Context</span></span>
<span data-ttu-id="21a84-122">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21a84-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21a84-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21a84-123">-DefaultProfile</span></span>
<span data-ttu-id="21a84-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="21a84-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21a84-125">-이름</span><span class="sxs-lookup"><span data-stu-id="21a84-125">-Name</span></span>
<span data-ttu-id="21a84-126">가져올 API의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21a84-126">Specifies the name of the API to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21a84-127">-ProductId</span><span class="sxs-lookup"><span data-stu-id="21a84-127">-ProductId</span></span>
<span data-ttu-id="21a84-128">API를 가져올 제품의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21a84-128">Specifies the ID of the product for which to get the API.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21a84-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21a84-129">CommonParameters</span></span>
<span data-ttu-id="21a84-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="21a84-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21a84-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21a84-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21a84-132">입력</span><span class="sxs-lookup"><span data-stu-id="21a84-132">INPUTS</span></span>

### <span data-ttu-id="21a84-133">않아야</span><span class="sxs-lookup"><span data-stu-id="21a84-133">None</span></span>
<span data-ttu-id="21a84-134">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="21a84-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="21a84-135">출력</span><span class="sxs-lookup"><span data-stu-id="21a84-135">OUTPUTS</span></span>

### <span data-ttu-id="21a84-136">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="21a84-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="21a84-137">지정 된 ApiManagement 서비스의 Api에 대 한 세부 정보</span><span class="sxs-lookup"><span data-stu-id="21a84-137">The details of the Api in a given ApiManagement service</span></span>

### <span data-ttu-id="21a84-138">IList를<ApiManagement> ServiceManagement. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="21a84-138">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi></span></span>
<span data-ttu-id="21a84-139">지정 된 ApiManagement 서비스의 Api 목록</span><span class="sxs-lookup"><span data-stu-id="21a84-139">The list of Apis in a given ApiManagement service</span></span>

## <span data-ttu-id="21a84-140">상속자</span><span class="sxs-lookup"><span data-stu-id="21a84-140">NOTES</span></span>

## <span data-ttu-id="21a84-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="21a84-141">RELATED LINKS</span></span>

[<span data-ttu-id="21a84-142">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="21a84-142">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="21a84-143">가져오기-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="21a84-143">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="21a84-144">새로운 AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="21a84-144">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="21a84-145">제거-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="21a84-145">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="21a84-146">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="21a84-146">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


