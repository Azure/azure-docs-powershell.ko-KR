---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 7a3c418c5f55aa70b23972e5cd51065557335866
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340113"
---
# <span data-ttu-id="bb2ea-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="bb2ea-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="bb2ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb2ea-102">SYNOPSIS</span></span>
<span data-ttu-id="bb2ea-103">API 릴리스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bb2ea-103">Get the API Release.</span></span>

## <span data-ttu-id="bb2ea-104">구문</span><span class="sxs-lookup"><span data-stu-id="bb2ea-104">SYNTAX</span></span>

### <span data-ttu-id="bb2ea-105">ContextParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="bb2ea-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb2ea-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb2ea-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiRelease -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb2ea-107">설명</span><span class="sxs-lookup"><span data-stu-id="bb2ea-107">DESCRIPTION</span></span>
<span data-ttu-id="bb2ea-108">**Get-AzApiManagementApiRelease** cmdlet은 Azure API Management API의 하나 이상의 릴리스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bb2ea-108">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="bb2ea-109">예제</span><span class="sxs-lookup"><span data-stu-id="bb2ea-109">EXAMPLES</span></span>

### <span data-ttu-id="bb2ea-110">예제 1: API의 모든 릴리스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bb2ea-110">Example 1: Get all releases of the API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="bb2ea-111">이 명령은 지정된 컨텍스트에 대한 `echo-api` API의 모든 릴리스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bb2ea-111">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="bb2ea-112">예제 2: 특정 API 릴리스의 릴리스 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="bb2ea-112">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402
                    e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="bb2ea-113">이 명령은 지정된 releaseId를 사용하여 특정 API의 릴리스 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bb2ea-113">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="bb2ea-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb2ea-114">PARAMETERS</span></span>

### <span data-ttu-id="bb2ea-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="bb2ea-115">-ApiId</span></span>
<span data-ttu-id="bb2ea-116">검색할 API 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="bb2ea-116">API identifier to look for.</span></span>
<span data-ttu-id="bb2ea-117">지정된 경우 ID로 API를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bb2ea-117">If specified will try to get the API by the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb2ea-118">-Context</span><span class="sxs-lookup"><span data-stu-id="bb2ea-118">-Context</span></span>
<span data-ttu-id="bb2ea-119">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="bb2ea-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="bb2ea-120">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="bb2ea-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb2ea-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb2ea-121">-DefaultProfile</span></span>
<span data-ttu-id="bb2ea-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bb2ea-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb2ea-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="bb2ea-123">-ReleaseId</span></span>
<span data-ttu-id="bb2ea-124">릴리스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="bb2ea-124">The identifier of the Release.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb2ea-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb2ea-125">-ResourceId</span></span>
<span data-ttu-id="bb2ea-126">Api 릴리스의 Arm 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="bb2ea-126">Arm Resource Identifier of a Api Release.</span></span> <span data-ttu-id="bb2ea-127">지정된 경우 식별자에 의해 API 릴리스를 찾으려고 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="bb2ea-127">If specified will try to find api release by the identifier.</span></span> <span data-ttu-id="bb2ea-128">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="bb2ea-128">This parameter is required.</span></span>

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

### <span data-ttu-id="bb2ea-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb2ea-129">CommonParameters</span></span>
<span data-ttu-id="bb2ea-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bb2ea-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb2ea-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bb2ea-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb2ea-132">입력</span><span class="sxs-lookup"><span data-stu-id="bb2ea-132">INPUTS</span></span>

### <span data-ttu-id="bb2ea-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bb2ea-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bb2ea-134">System.String</span><span class="sxs-lookup"><span data-stu-id="bb2ea-134">System.String</span></span>

## <span data-ttu-id="bb2ea-135">출력</span><span class="sxs-lookup"><span data-stu-id="bb2ea-135">OUTPUTS</span></span>

### <span data-ttu-id="bb2ea-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="bb2ea-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="bb2ea-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bb2ea-137">NOTES</span></span>

## <span data-ttu-id="bb2ea-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb2ea-138">RELATED LINKS</span></span>

[<span data-ttu-id="bb2ea-139">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="bb2ea-139">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="bb2ea-140">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="bb2ea-140">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="bb2ea-141">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="bb2ea-141">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)