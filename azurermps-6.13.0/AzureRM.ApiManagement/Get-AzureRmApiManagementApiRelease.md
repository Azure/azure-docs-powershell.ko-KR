---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: 880d96ba0e9eff053084517452c03ffb018b72a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702128"
---
# <span data-ttu-id="fd86a-101">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="fd86a-101">Get-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="fd86a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd86a-102">SYNOPSIS</span></span>
<span data-ttu-id="fd86a-103">API 릴리스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fd86a-103">Get the API Release.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd86a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fd86a-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd86a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fd86a-105">DESCRIPTION</span></span>
<span data-ttu-id="fd86a-106">**AzureRmApiManagementApiRelease** cmdlet은 하나 이상의 Azure API Management api 릴리스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fd86a-106">The **Get-AzureRmApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="fd86a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fd86a-107">EXAMPLES</span></span>

### <span data-ttu-id="fd86a-108">예제 1: API의 모든 릴리스 가져오기</span><span class="sxs-lookup"><span data-stu-id="fd86a-108">Example 1: Get all releases of the API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contos
```

<span data-ttu-id="fd86a-109">이 명령은 `echo-api` 지정 된 컨텍스트에 대 한 API의 모든 릴리스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fd86a-109">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="fd86a-110">예제 2: 특정 API 릴리스의 릴리스 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="fd86a-110">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
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

<span data-ttu-id="fd86a-111">이 명령은 지정 된 releaseId의 특정 API에 대 한 릴리스 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fd86a-111">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="fd86a-112">변수</span><span class="sxs-lookup"><span data-stu-id="fd86a-112">PARAMETERS</span></span>

### <span data-ttu-id="fd86a-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="fd86a-113">-ApiId</span></span>
<span data-ttu-id="fd86a-114">찾을 API 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="fd86a-114">API identifier to look for.</span></span>
<span data-ttu-id="fd86a-115">지정 된 경우 Id로 API를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fd86a-115">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="fd86a-116">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="fd86a-116">-Context</span></span>
<span data-ttu-id="fd86a-117">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="fd86a-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fd86a-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="fd86a-118">This parameter is required.</span></span>

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

### <span data-ttu-id="fd86a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd86a-119">-DefaultProfile</span></span>
<span data-ttu-id="fd86a-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd86a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd86a-121">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="fd86a-121">-ReleaseId</span></span>
<span data-ttu-id="fd86a-122">릴리스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="fd86a-122">The identifier of the Release.</span></span>

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

### <span data-ttu-id="fd86a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd86a-123">CommonParameters</span></span>
<span data-ttu-id="fd86a-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd86a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd86a-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd86a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd86a-126">입력</span><span class="sxs-lookup"><span data-stu-id="fd86a-126">INPUTS</span></span>

### <span data-ttu-id="fd86a-127">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fd86a-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fd86a-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fd86a-128">System.String</span></span>

## <span data-ttu-id="fd86a-129">출력</span><span class="sxs-lookup"><span data-stu-id="fd86a-129">OUTPUTS</span></span>

### <span data-ttu-id="fd86a-130">ApiManagement. ServiceManagement. \ PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="fd86a-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="fd86a-131">상속자</span><span class="sxs-lookup"><span data-stu-id="fd86a-131">NOTES</span></span>

## <span data-ttu-id="fd86a-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd86a-132">RELATED LINKS</span></span>

[<span data-ttu-id="fd86a-133">새로운 AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="fd86a-133">New-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="fd86a-134">제거-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="fd86a-134">Remove-AzureRmApiManagementApiRelease</span></span>](./Remove-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="fd86a-135">Set-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="fd86a-135">Set-AzureRmApiManagementApiRelease</span></span>](./Set-AzureRmApiManagementApiRelease.md)
