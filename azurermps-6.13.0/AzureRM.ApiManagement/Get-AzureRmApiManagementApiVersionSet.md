---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: 60a811aaa097ccc95f8dd57fa105ba4b1388b060
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531516"
---
# <span data-ttu-id="f6d16-101">Get-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f6d16-101">Get-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="f6d16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6d16-102">SYNOPSIS</span></span>
<span data-ttu-id="f6d16-103">API 버전 집합에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="f6d16-103">Get the details of the API Version Sets</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6d16-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f6d16-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6d16-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f6d16-105">DESCRIPTION</span></span>
<span data-ttu-id="f6d16-106">**AzureRmApiManagementApiVersionSet** CMDLET은 api Management 컨텍스트에서 구성 된 Api 버전 집합의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f6d16-106">The **Get-AzureRmApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="f6d16-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f6d16-107">EXAMPLES</span></span>

### <span data-ttu-id="f6d16-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f6d16-108">Example 1</span></span>

### <span data-ttu-id="f6d16-109">예제 1: 모든 API 버전 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="f6d16-109">Example 1: Get all API Version Sets</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiVersionSet -Context $ApiMgmtContext

ApiVersionSetId   : a93316c8-8b88-46cc-8260-380789a5d598
Description       :
VersionQueryName  :
VersionHeaderName :
DisplayName       : Echo API
VersioningScheme  : Segment
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/a916c8-8b88-46cc-8260-380789a5d598
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso

ApiVersionSetId   : 4cbdfa34-25f3-4a93-a9b6-76b6eade7562
Description       :
VersionQueryName  : api-version
VersionHeaderName :
DisplayName       : getproduct old
VersioningScheme  : Query
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/4cbdfa34-25f3-4a93-a9b6-76b6eade7562
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso


ApiVersionSetId   : 8c441e0e-a0cd-47d8-8d88-f944a83b41bd
Description       :
VersionQueryName  :
VersionHeaderName : Api-Version
DisplayName       : ordersapi
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/8c441e0e-a0cd-47d8-8d88-f944a83b41bd
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="f6d16-110">이 명령은 지정 된 컨텍스트에 대 한 모든 API 버전 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f6d16-110">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="f6d16-111">예제 2: ID로 설정 된 API 버전 가져오기</span><span class="sxs-lookup"><span data-stu-id="f6d16-111">Example 2: Get a API Version Set by ID</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId $ApiVersionSetId

ApiVersionSetId   : 8c441e0e-a0cd-47d8-8d88-f944a83b41bd
Description       :
VersionQueryName  :
VersionHeaderName : Api-Version
DisplayName       : ordersapi
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/8c441e0e-a0cd-47d8-8d88-f944a83b41bd
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="f6d16-112">이 명령은 지정 된 ID를 갖는 API 버전 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f6d16-112">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="f6d16-113">변수</span><span class="sxs-lookup"><span data-stu-id="f6d16-113">PARAMETERS</span></span>

### <span data-ttu-id="f6d16-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="f6d16-114">-ApiVersionSetId</span></span>
<span data-ttu-id="f6d16-115">찾을 API 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="f6d16-115">API identifier to look for.</span></span>
<span data-ttu-id="f6d16-116">지정 된 경우 Id로 API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f6d16-116">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="f6d16-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="f6d16-117">-Context</span></span>
<span data-ttu-id="f6d16-118">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="f6d16-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f6d16-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="f6d16-119">This parameter is required.</span></span>

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

### <span data-ttu-id="f6d16-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6d16-120">-DefaultProfile</span></span>
<span data-ttu-id="f6d16-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f6d16-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6d16-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6d16-122">CommonParameters</span></span>
<span data-ttu-id="f6d16-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6d16-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6d16-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6d16-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6d16-125">입력</span><span class="sxs-lookup"><span data-stu-id="f6d16-125">INPUTS</span></span>

### <span data-ttu-id="f6d16-126">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f6d16-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f6d16-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f6d16-127">System.String</span></span>

## <span data-ttu-id="f6d16-128">출력</span><span class="sxs-lookup"><span data-stu-id="f6d16-128">OUTPUTS</span></span>

### <span data-ttu-id="f6d16-129">ApiManagement. ServiceManagement. \ PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f6d16-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="f6d16-130">상속자</span><span class="sxs-lookup"><span data-stu-id="f6d16-130">NOTES</span></span>

## <span data-ttu-id="f6d16-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f6d16-131">RELATED LINKS</span></span>

[<span data-ttu-id="f6d16-132">새로운 AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f6d16-132">New-AzureRmApiManagementApiVersionSet</span></span>](./New-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="f6d16-133">제거-AzureRmApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="f6d16-133">Remove-AzureRmApiManagementApiSet</span></span>](./Remove-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="f6d16-134">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f6d16-134">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiSet.md)