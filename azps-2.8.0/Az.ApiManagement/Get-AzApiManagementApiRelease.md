---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 19395960d3a0026b7a14c4ca8232c18d511af989
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698127"
---
# <span data-ttu-id="bba99-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="bba99-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="bba99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bba99-102">SYNOPSIS</span></span>
<span data-ttu-id="bba99-103">API 릴리스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bba99-103">Get the API Release.</span></span>

## <span data-ttu-id="bba99-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bba99-104">SYNTAX</span></span>

### <span data-ttu-id="bba99-105">ContextParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="bba99-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bba99-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bba99-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiRelease -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bba99-107">설명은</span><span class="sxs-lookup"><span data-stu-id="bba99-107">DESCRIPTION</span></span>
<span data-ttu-id="bba99-108">**AzApiManagementApiRelease** cmdlet은 하나 이상의 Azure API Management api 릴리스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bba99-108">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="bba99-109">예제의</span><span class="sxs-lookup"><span data-stu-id="bba99-109">EXAMPLES</span></span>

### <span data-ttu-id="bba99-110">예제 1: API의 모든 릴리스 가져오기</span><span class="sxs-lookup"><span data-stu-id="bba99-110">Example 1: Get all releases of the API</span></span>
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

<span data-ttu-id="bba99-111">이 명령은 `echo-api` 지정 된 컨텍스트에 대 한 API의 모든 릴리스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bba99-111">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="bba99-112">예제 2: 특정 API 릴리스의 릴리스 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="bba99-112">Example 2: Get the release information of the particular API release</span></span>
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

<span data-ttu-id="bba99-113">이 명령은 지정 된 releaseId의 특정 API에 대 한 릴리스 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bba99-113">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="bba99-114">변수</span><span class="sxs-lookup"><span data-stu-id="bba99-114">PARAMETERS</span></span>

### <span data-ttu-id="bba99-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="bba99-115">-ApiId</span></span>
<span data-ttu-id="bba99-116">찾을 API 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="bba99-116">API identifier to look for.</span></span>
<span data-ttu-id="bba99-117">지정 된 경우 Id로 API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bba99-117">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="bba99-118">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="bba99-118">-Context</span></span>
<span data-ttu-id="bba99-119">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="bba99-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="bba99-120">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="bba99-120">This parameter is required.</span></span>

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

### <span data-ttu-id="bba99-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bba99-121">-DefaultProfile</span></span>
<span data-ttu-id="bba99-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bba99-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bba99-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="bba99-123">-ReleaseId</span></span>
<span data-ttu-id="bba99-124">릴리스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="bba99-124">The identifier of the Release.</span></span>

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

### <span data-ttu-id="bba99-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bba99-125">-ResourceId</span></span>
<span data-ttu-id="bba99-126">Api 릴리스의 Arm 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="bba99-126">Arm Resource Identifier of a Api Release.</span></span> <span data-ttu-id="bba99-127">지정 된 경우 식별자를 기준으로 api 릴리스를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bba99-127">If specified will try to find api release by the identifier.</span></span> <span data-ttu-id="bba99-128">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="bba99-128">This parameter is required.</span></span>

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

### <span data-ttu-id="bba99-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bba99-129">CommonParameters</span></span>
<span data-ttu-id="bba99-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bba99-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bba99-131">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bba99-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bba99-132">입력</span><span class="sxs-lookup"><span data-stu-id="bba99-132">INPUTS</span></span>

### <span data-ttu-id="bba99-133">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bba99-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bba99-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bba99-134">System.String</span></span>

## <span data-ttu-id="bba99-135">출력</span><span class="sxs-lookup"><span data-stu-id="bba99-135">OUTPUTS</span></span>

### <span data-ttu-id="bba99-136">ApiManagement. ServiceManagement. \ PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="bba99-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="bba99-137">상속자</span><span class="sxs-lookup"><span data-stu-id="bba99-137">NOTES</span></span>

## <span data-ttu-id="bba99-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bba99-138">RELATED LINKS</span></span>

[<span data-ttu-id="bba99-139">새로운 AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="bba99-139">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="bba99-140">제거-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="bba99-140">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="bba99-141">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="bba99-141">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)