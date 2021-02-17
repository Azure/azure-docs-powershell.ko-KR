---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 4f9e917f17037e5f47b52501007da5556bde1187
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401082"
---
# <span data-ttu-id="b35db-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b35db-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="b35db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b35db-102">SYNOPSIS</span></span>
<span data-ttu-id="b35db-103">API 릴리스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b35db-103">Get the API Release.</span></span>

## <span data-ttu-id="b35db-104">구문</span><span class="sxs-lookup"><span data-stu-id="b35db-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b35db-105">설명</span><span class="sxs-lookup"><span data-stu-id="b35db-105">DESCRIPTION</span></span>
<span data-ttu-id="b35db-106">**Get-AzApiManagementApiRelease** cmdlet은 Azure API Management API의 하나 이상의 릴리스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b35db-106">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="b35db-107">예제</span><span class="sxs-lookup"><span data-stu-id="b35db-107">EXAMPLES</span></span>

### <span data-ttu-id="b35db-108">예제 1: API의 모든 릴리스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b35db-108">Example 1: Get all releases of the API</span></span>
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
ServiceName       : contos
```

<span data-ttu-id="b35db-109">이 명령은 지정된 컨텍스트에 대한 `echo-api` API의 모든 릴리스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b35db-109">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="b35db-110">예제 2: 특정 API 릴리스의 릴리스 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="b35db-110">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contos/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402
                    e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contos
```

<span data-ttu-id="b35db-111">이 명령은 지정된 releaseId를 사용하여 특정 API의 릴리스 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b35db-111">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="b35db-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b35db-112">PARAMETERS</span></span>

### <span data-ttu-id="b35db-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b35db-113">-ApiId</span></span>
<span data-ttu-id="b35db-114">검색할 API 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b35db-114">API identifier to look for.</span></span>
<span data-ttu-id="b35db-115">지정된 경우 ID로 API를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b35db-115">If specified will try to get the API by the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b35db-116">-Context</span><span class="sxs-lookup"><span data-stu-id="b35db-116">-Context</span></span>
<span data-ttu-id="b35db-117">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="b35db-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b35db-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="b35db-118">This parameter is required.</span></span>

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

### <span data-ttu-id="b35db-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b35db-119">-DefaultProfile</span></span>
<span data-ttu-id="b35db-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b35db-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b35db-121">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="b35db-121">-ReleaseId</span></span>
<span data-ttu-id="b35db-122">릴리스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b35db-122">The identifier of the Release.</span></span>

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

### <span data-ttu-id="b35db-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b35db-123">CommonParameters</span></span>
<span data-ttu-id="b35db-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b35db-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b35db-125">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b35db-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b35db-126">입력</span><span class="sxs-lookup"><span data-stu-id="b35db-126">INPUTS</span></span>

### <span data-ttu-id="b35db-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b35db-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b35db-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b35db-128">System.String</span></span>

## <span data-ttu-id="b35db-129">출력</span><span class="sxs-lookup"><span data-stu-id="b35db-129">OUTPUTS</span></span>

### <span data-ttu-id="b35db-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b35db-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="b35db-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b35db-131">NOTES</span></span>

## <span data-ttu-id="b35db-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b35db-132">RELATED LINKS</span></span>

[<span data-ttu-id="b35db-133">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b35db-133">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="b35db-134">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b35db-134">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="b35db-135">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b35db-135">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)