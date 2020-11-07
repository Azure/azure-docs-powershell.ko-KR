---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 16fea88f5a5a1ad8a0e39f62b26d918ca7a64dbd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689157"
---
# <span data-ttu-id="cc909-101">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="cc909-101">Get-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="cc909-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc909-102">SYNOPSIS</span></span>
<span data-ttu-id="cc909-103">API 버전 집합에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="cc909-103">Get the details of the API Version Sets</span></span>

## <span data-ttu-id="cc909-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cc909-104">SYNTAX</span></span>

```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc909-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cc909-105">DESCRIPTION</span></span>
<span data-ttu-id="cc909-106">**AzApiManagementApiVersionSet** CMDLET은 api Management 컨텍스트에서 구성 된 Api 버전 집합의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cc909-106">The **Get-AzApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="cc909-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cc909-107">EXAMPLES</span></span>

### <span data-ttu-id="cc909-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="cc909-108">Example 1</span></span>

### <span data-ttu-id="cc909-109">예제 1: 모든 API 버전 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="cc909-109">Example 1: Get all API Version Sets</span></span>
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

<span data-ttu-id="cc909-110">이 명령은 지정 된 컨텍스트에 대 한 모든 API 버전 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cc909-110">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="cc909-111">예제 2: ID로 설정 된 API 버전 가져오기</span><span class="sxs-lookup"><span data-stu-id="cc909-111">Example 2: Get a API Version Set by ID</span></span>
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

<span data-ttu-id="cc909-112">이 명령은 지정 된 ID를 갖는 API 버전 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cc909-112">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="cc909-113">변수</span><span class="sxs-lookup"><span data-stu-id="cc909-113">PARAMETERS</span></span>

### <span data-ttu-id="cc909-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="cc909-114">-ApiVersionSetId</span></span>
<span data-ttu-id="cc909-115">찾을 API 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="cc909-115">API identifier to look for.</span></span>
<span data-ttu-id="cc909-116">지정 된 경우 Id로 API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cc909-116">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="cc909-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="cc909-117">-Context</span></span>
<span data-ttu-id="cc909-118">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="cc909-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="cc909-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="cc909-119">This parameter is required.</span></span>

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

### <span data-ttu-id="cc909-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc909-120">-DefaultProfile</span></span>
<span data-ttu-id="cc909-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cc909-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc909-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc909-122">CommonParameters</span></span>
<span data-ttu-id="cc909-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc909-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc909-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc909-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc909-125">입력</span><span class="sxs-lookup"><span data-stu-id="cc909-125">INPUTS</span></span>

### <span data-ttu-id="cc909-126">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cc909-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cc909-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cc909-127">System.String</span></span>

## <span data-ttu-id="cc909-128">출력</span><span class="sxs-lookup"><span data-stu-id="cc909-128">OUTPUTS</span></span>

### <span data-ttu-id="cc909-129">ApiManagement. ServiceManagement. \ PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="cc909-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="cc909-130">상속자</span><span class="sxs-lookup"><span data-stu-id="cc909-130">NOTES</span></span>

## <span data-ttu-id="cc909-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cc909-131">RELATED LINKS</span></span>

[<span data-ttu-id="cc909-132">새로운 AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="cc909-132">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="cc909-133">제거-AzApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="cc909-133">Remove-AzApiManagementApiSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="cc909-134">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="cc909-134">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiSet.md)
