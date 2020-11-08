---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 2b87f3b0716c95f27a78c2a0f59168f133ade015
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041947"
---
# <span data-ttu-id="392fd-101">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="392fd-101">Get-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="392fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="392fd-102">SYNOPSIS</span></span>
<span data-ttu-id="392fd-103">API 버전 집합에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="392fd-103">Get the details of the API Version Sets</span></span>

## <span data-ttu-id="392fd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="392fd-104">SYNTAX</span></span>

### <span data-ttu-id="392fd-105">ContextParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="392fd-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="392fd-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="392fd-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="392fd-107">설명은</span><span class="sxs-lookup"><span data-stu-id="392fd-107">DESCRIPTION</span></span>
<span data-ttu-id="392fd-108">**AzApiManagementApiVersionSet** CMDLET은 api Management 컨텍스트에서 구성 된 Api 버전 집합의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="392fd-108">The **Get-AzApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="392fd-109">예제의</span><span class="sxs-lookup"><span data-stu-id="392fd-109">EXAMPLES</span></span>

### <span data-ttu-id="392fd-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="392fd-110">Example 1</span></span>

### <span data-ttu-id="392fd-111">예제 1: 모든 API 버전 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="392fd-111">Example 1: Get all API Version Sets</span></span>
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

<span data-ttu-id="392fd-112">이 명령은 지정 된 컨텍스트에 대 한 모든 API 버전 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="392fd-112">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="392fd-113">예제 2: ID로 설정 된 API 버전 가져오기</span><span class="sxs-lookup"><span data-stu-id="392fd-113">Example 2: Get a API Version Set by ID</span></span>
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

<span data-ttu-id="392fd-114">이 명령은 지정 된 ID를 갖는 API 버전 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="392fd-114">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="392fd-115">변수</span><span class="sxs-lookup"><span data-stu-id="392fd-115">PARAMETERS</span></span>

### <span data-ttu-id="392fd-116">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="392fd-116">-ApiVersionSetId</span></span>
<span data-ttu-id="392fd-117">찾을 API 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="392fd-117">API identifier to look for.</span></span>
<span data-ttu-id="392fd-118">지정 된 경우 Id로 API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="392fd-118">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="392fd-119">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="392fd-119">-Context</span></span>
<span data-ttu-id="392fd-120">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="392fd-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="392fd-121">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="392fd-121">This parameter is required.</span></span>

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

### <span data-ttu-id="392fd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="392fd-122">-DefaultProfile</span></span>
<span data-ttu-id="392fd-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="392fd-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="392fd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="392fd-124">-ResourceId</span></span>
<span data-ttu-id="392fd-125">ApiVersionSet의 Arm 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="392fd-125">Arm Resource Identifier of the ApiVersionSet.</span></span> <span data-ttu-id="392fd-126">지정 된 경우 식별자에서 설정한 apiVersionSet을 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="392fd-126">If specified will try to find apiVersionSet by the identifier.</span></span> <span data-ttu-id="392fd-127">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="392fd-127">This parameter is required.</span></span>

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

### <span data-ttu-id="392fd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="392fd-128">CommonParameters</span></span>
<span data-ttu-id="392fd-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="392fd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="392fd-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="392fd-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="392fd-131">입력</span><span class="sxs-lookup"><span data-stu-id="392fd-131">INPUTS</span></span>

### <span data-ttu-id="392fd-132">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="392fd-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="392fd-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="392fd-133">System.String</span></span>

## <span data-ttu-id="392fd-134">출력</span><span class="sxs-lookup"><span data-stu-id="392fd-134">OUTPUTS</span></span>

### <span data-ttu-id="392fd-135">ApiManagement. ServiceManagement. \ PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="392fd-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="392fd-136">상속자</span><span class="sxs-lookup"><span data-stu-id="392fd-136">NOTES</span></span>

## <span data-ttu-id="392fd-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="392fd-137">RELATED LINKS</span></span>

[<span data-ttu-id="392fd-138">새로운 AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="392fd-138">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="392fd-139">제거-AzApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="392fd-139">Remove-AzApiManagementApiSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="392fd-140">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="392fd-140">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiSet.md)
