---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
ms.openlocfilehash: a87c75058e3ebfb1ae7d14e729fdc9280cdccb9c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689163"
---
# <span data-ttu-id="345bc-101">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="345bc-101">Get-AzApiManagementApi</span></span>

## <span data-ttu-id="345bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="345bc-102">SYNOPSIS</span></span>
<span data-ttu-id="345bc-103">API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="345bc-103">Gets an API.</span></span>

## <span data-ttu-id="345bc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="345bc-104">SYNTAX</span></span>

### <span data-ttu-id="345bc-105">GetAllApis (기본값)</span><span class="sxs-lookup"><span data-stu-id="345bc-105">GetAllApis (Default)</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="345bc-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="345bc-106">GetByApiId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="345bc-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="345bc-107">GetByName</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="345bc-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="345bc-108">GetByProductId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="345bc-109">설명은</span><span class="sxs-lookup"><span data-stu-id="345bc-109">DESCRIPTION</span></span>
<span data-ttu-id="345bc-110">**AzApiManagementApi** cmdlet은 하나 이상의 Azure API 관리 api를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="345bc-110">The **Get-AzApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="345bc-111">예제의</span><span class="sxs-lookup"><span data-stu-id="345bc-111">EXAMPLES</span></span>

### <span data-ttu-id="345bc-112">예제 1: 모든 관리 Api 가져오기</span><span class="sxs-lookup"><span data-stu-id="345bc-112">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="345bc-113">이 명령은 지정 된 컨텍스트에 대 한 모든 Api를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="345bc-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="345bc-114">예제 2: ID로 관리 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="345bc-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="345bc-115">이 명령은 지정 된 ID의 API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="345bc-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="345bc-116">예제 3: 이름별로 관리 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="345bc-116">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="345bc-117">이 명령은 지정 된 이름의 API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="345bc-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="345bc-118">변수</span><span class="sxs-lookup"><span data-stu-id="345bc-118">PARAMETERS</span></span>

### <span data-ttu-id="345bc-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="345bc-119">-ApiId</span></span>
<span data-ttu-id="345bc-120">가져올 API의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="345bc-120">Specifies the ID of the API to get.</span></span>

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

### <span data-ttu-id="345bc-121">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="345bc-121">-ApiRevision</span></span>
<span data-ttu-id="345bc-122">특정 Api 개정판의 수정 버전 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="345bc-122">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="345bc-123">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="345bc-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="345bc-124">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="345bc-124">-Context</span></span>
<span data-ttu-id="345bc-125">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="345bc-125">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="345bc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="345bc-126">-DefaultProfile</span></span>
<span data-ttu-id="345bc-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="345bc-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="345bc-128">-이름</span><span class="sxs-lookup"><span data-stu-id="345bc-128">-Name</span></span>
<span data-ttu-id="345bc-129">가져올 API의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="345bc-129">Specifies the name of the API to get.</span></span>

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

### <span data-ttu-id="345bc-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="345bc-130">-ProductId</span></span>
<span data-ttu-id="345bc-131">API를 가져올 제품의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="345bc-131">Specifies the ID of the product for which to get the API.</span></span>

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

### <span data-ttu-id="345bc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="345bc-132">CommonParameters</span></span>
<span data-ttu-id="345bc-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="345bc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="345bc-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="345bc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="345bc-135">입력</span><span class="sxs-lookup"><span data-stu-id="345bc-135">INPUTS</span></span>

### <span data-ttu-id="345bc-136">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="345bc-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="345bc-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="345bc-137">System.String</span></span>

## <span data-ttu-id="345bc-138">출력</span><span class="sxs-lookup"><span data-stu-id="345bc-138">OUTPUTS</span></span>

### <span data-ttu-id="345bc-139">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="345bc-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="345bc-140">상속자</span><span class="sxs-lookup"><span data-stu-id="345bc-140">NOTES</span></span>

## <span data-ttu-id="345bc-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="345bc-141">RELATED LINKS</span></span>

[<span data-ttu-id="345bc-142">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="345bc-142">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="345bc-143">가져오기-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="345bc-143">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="345bc-144">새로운 AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="345bc-144">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="345bc-145">제거-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="345bc-145">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="345bc-146">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="345bc-146">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


