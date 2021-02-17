---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 5b7c06e9ed75cf973a3b9e375ff888477b9a96d7
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400980"
---
# <span data-ttu-id="1be98-101">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1be98-101">Get-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="1be98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1be98-102">SYNOPSIS</span></span>
<span data-ttu-id="1be98-103">API 버전 집합의 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="1be98-103">Get the details of the API Version Sets</span></span>

## <span data-ttu-id="1be98-104">구문</span><span class="sxs-lookup"><span data-stu-id="1be98-104">SYNTAX</span></span>

```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1be98-105">설명</span><span class="sxs-lookup"><span data-stu-id="1be98-105">DESCRIPTION</span></span>
<span data-ttu-id="1be98-106">**Get-AzApiManagementApiVersionSet** cmdlet은 API Management 컨텍스트에 구성된 API 버전 집합의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1be98-106">The **Get-AzApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="1be98-107">예제</span><span class="sxs-lookup"><span data-stu-id="1be98-107">EXAMPLES</span></span>

### <span data-ttu-id="1be98-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1be98-108">Example 1</span></span>

### <span data-ttu-id="1be98-109">예제 1: 모든 API 버전 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1be98-109">Example 1: Get all API Version Sets</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiVersionSet -Context $ApiMgmtContext

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

<span data-ttu-id="1be98-110">이 명령은 지정된 컨텍스트에 대한 모든 API 버전 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1be98-110">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="1be98-111">예제 2: ID로 API 버전 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1be98-111">Example 2: Get a API Version Set by ID</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId $ApiVersionSetId

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

<span data-ttu-id="1be98-112">이 명령은 지정된 ID로 API 버전 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1be98-112">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="1be98-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1be98-113">PARAMETERS</span></span>

### <span data-ttu-id="1be98-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="1be98-114">-ApiVersionSetId</span></span>
<span data-ttu-id="1be98-115">검색할 API 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="1be98-115">API identifier to look for.</span></span>
<span data-ttu-id="1be98-116">지정된 경우 ID로 API를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1be98-116">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="1be98-117">-Context</span><span class="sxs-lookup"><span data-stu-id="1be98-117">-Context</span></span>
<span data-ttu-id="1be98-118">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="1be98-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1be98-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="1be98-119">This parameter is required.</span></span>

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

### <span data-ttu-id="1be98-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1be98-120">-DefaultProfile</span></span>
<span data-ttu-id="1be98-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1be98-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1be98-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1be98-122">CommonParameters</span></span>
<span data-ttu-id="1be98-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1be98-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1be98-124">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1be98-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1be98-125">입력</span><span class="sxs-lookup"><span data-stu-id="1be98-125">INPUTS</span></span>

### <span data-ttu-id="1be98-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1be98-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1be98-127">System.String</span><span class="sxs-lookup"><span data-stu-id="1be98-127">System.String</span></span>

## <span data-ttu-id="1be98-128">출력</span><span class="sxs-lookup"><span data-stu-id="1be98-128">OUTPUTS</span></span>

### <span data-ttu-id="1be98-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1be98-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="1be98-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1be98-130">NOTES</span></span>

## <span data-ttu-id="1be98-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1be98-131">RELATED LINKS</span></span>

[<span data-ttu-id="1be98-132">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1be98-132">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="1be98-133">Remove-AzApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="1be98-133">Remove-AzApiManagementApiSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="1be98-134">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1be98-134">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
