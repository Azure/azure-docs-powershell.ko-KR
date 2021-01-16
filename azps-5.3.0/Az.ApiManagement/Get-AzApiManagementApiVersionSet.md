---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
ms.openlocfilehash: e6b9122481e5e506fc02a13a61b7ebeb71372e96
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494473"
---
# <span data-ttu-id="75f1d-101">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="75f1d-101">Get-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="75f1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75f1d-102">SYNOPSIS</span></span>
<span data-ttu-id="75f1d-103">API 버전 집합의 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="75f1d-103">Get the details of the API Version Sets</span></span>

## <span data-ttu-id="75f1d-104">구문</span><span class="sxs-lookup"><span data-stu-id="75f1d-104">SYNTAX</span></span>

### <span data-ttu-id="75f1d-105">ContextParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="75f1d-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75f1d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75f1d-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75f1d-107">설명</span><span class="sxs-lookup"><span data-stu-id="75f1d-107">DESCRIPTION</span></span>
<span data-ttu-id="75f1d-108">**Get-AzApiManagementApiVersionSet** cmdlet은 API Management 컨텍스트에 구성된 API 버전 집합의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="75f1d-108">The **Get-AzApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="75f1d-109">예제</span><span class="sxs-lookup"><span data-stu-id="75f1d-109">EXAMPLES</span></span>

### <span data-ttu-id="75f1d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="75f1d-110">Example 1</span></span>

### <span data-ttu-id="75f1d-111">예제 2: 모든 API 버전 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="75f1d-111">Example 2: Get all API Version Sets</span></span>
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

<span data-ttu-id="75f1d-112">이 명령은 지정된 컨텍스트에 대한 모든 API 버전 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="75f1d-112">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="75f1d-113">예제 3: ID로 API 버전 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="75f1d-113">Example 3: Get a API Version Set by ID</span></span>
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

<span data-ttu-id="75f1d-114">이 명령은 지정된 ID로 API 버전 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="75f1d-114">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="75f1d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75f1d-115">PARAMETERS</span></span>

### <span data-ttu-id="75f1d-116">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="75f1d-116">-ApiVersionSetId</span></span>
<span data-ttu-id="75f1d-117">검색할 API 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="75f1d-117">API identifier to look for.</span></span>
<span data-ttu-id="75f1d-118">지정된 경우 ID로 API를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="75f1d-118">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="75f1d-119">-Context</span><span class="sxs-lookup"><span data-stu-id="75f1d-119">-Context</span></span>
<span data-ttu-id="75f1d-120">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="75f1d-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="75f1d-121">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="75f1d-121">This parameter is required.</span></span>

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

### <span data-ttu-id="75f1d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75f1d-122">-DefaultProfile</span></span>
<span data-ttu-id="75f1d-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="75f1d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75f1d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75f1d-124">-ResourceId</span></span>
<span data-ttu-id="75f1d-125">ApiVersionSet의 Arm 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="75f1d-125">Arm Resource Identifier of the ApiVersionSet.</span></span> <span data-ttu-id="75f1d-126">지정된 경우 식별자에 의해 apiVersionSet을 찾으려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="75f1d-126">If specified will try to find apiVersionSet by the identifier.</span></span> <span data-ttu-id="75f1d-127">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="75f1d-127">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75f1d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75f1d-128">CommonParameters</span></span>
<span data-ttu-id="75f1d-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="75f1d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75f1d-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="75f1d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75f1d-131">입력</span><span class="sxs-lookup"><span data-stu-id="75f1d-131">INPUTS</span></span>

### <span data-ttu-id="75f1d-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="75f1d-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="75f1d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="75f1d-133">System.String</span></span>

## <span data-ttu-id="75f1d-134">출력</span><span class="sxs-lookup"><span data-stu-id="75f1d-134">OUTPUTS</span></span>

### <span data-ttu-id="75f1d-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="75f1d-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="75f1d-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="75f1d-136">NOTES</span></span>

## <span data-ttu-id="75f1d-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75f1d-137">RELATED LINKS</span></span>

[<span data-ttu-id="75f1d-138">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="75f1d-138">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="75f1d-139">Remove-AzApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="75f1d-139">Remove-AzApiManagementApiSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="75f1d-140">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="75f1d-140">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
