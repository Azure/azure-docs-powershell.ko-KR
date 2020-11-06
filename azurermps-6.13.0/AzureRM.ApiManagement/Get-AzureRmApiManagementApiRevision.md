---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: f57a95e97c0ec74e7e45338e15a028feab60849b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531518"
---
# <span data-ttu-id="d1400-101">Get-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="d1400-101">Get-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="d1400-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1400-102">SYNOPSIS</span></span>
<span data-ttu-id="d1400-103">API의 모든 API 수정 내용에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1400-103">Gets details of all the API Revisions of an API</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1400-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d1400-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1400-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d1400-105">DESCRIPTION</span></span>
<span data-ttu-id="d1400-106">**AzureRmApiManagementApiRevision** CMDLET은 API의 모든 수정 내용에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1400-106">The **Get-AzureRmApiManagementApiRevision** cmdlet gets the details of all revisions of an API</span></span>

## <span data-ttu-id="d1400-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d1400-107">EXAMPLES</span></span>

### <span data-ttu-id="d1400-108">예제 1: API의 모든 API 수정 내용 가져오기</span><span class="sxs-lookup"><span data-stu-id="d1400-108">Example 1: Get all API Revisions of an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiRevision -Context $ApiMgmtContext -ApiId "5adf6fbf0faadf3ad8558065"

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=3
ApiRevision     : 3
CreatedDateTime : 4/26/2018 10:57:42 PM
UpdatedDateTime : 4/26/2018 10:57:42 PM
Description     : ddsds
PrivateUrl      : /httpbin/v1;rev=3
IsOnline        : True
IsCurrent       : False

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=2
ApiRevision     : 2
CreatedDateTime : 4/26/2018 10:57:33 PM
UpdatedDateTime : 4/26/2018 10:57:33 PM
Description     : AA
PrivateUrl      : /httpbin/v1
IsOnline        : True
IsCurrent       : True

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=1
ApiRevision     : 1
CreatedDateTime : 4/24/2018 5:56:17 PM
UpdatedDateTime : 5/9/2018 9:29:06 PM
Description     :
PrivateUrl      : /httpbin/v1;rev=1
IsOnline        : True
IsCurrent       : False
```

<span data-ttu-id="d1400-109">이 명령은 특정 ApiManagement 컨텍스트에 대해 지정 된 API의 모든 API 수정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1400-109">This command gets all of the API revision of specified API for particular ApiManagement Context.</span></span>

## <span data-ttu-id="d1400-110">변수</span><span class="sxs-lookup"><span data-stu-id="d1400-110">PARAMETERS</span></span>

### <span data-ttu-id="d1400-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d1400-111">-ApiId</span></span>
<span data-ttu-id="d1400-112">해당 수정 내용을 나열 하려는 API 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d1400-112">API identifier whose revisions we want to list.</span></span>
<span data-ttu-id="d1400-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="d1400-113">This parameter is required.</span></span>

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

### <span data-ttu-id="d1400-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="d1400-114">-ApiRevision</span></span>
<span data-ttu-id="d1400-115">특정 Api 개정판의 수정 버전 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d1400-115">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="d1400-116">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="d1400-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="d1400-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="d1400-117">-Context</span></span>
<span data-ttu-id="d1400-118">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="d1400-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d1400-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="d1400-119">This parameter is required.</span></span>

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

### <span data-ttu-id="d1400-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1400-120">-DefaultProfile</span></span>
<span data-ttu-id="d1400-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1400-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1400-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1400-122">CommonParameters</span></span>
<span data-ttu-id="d1400-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1400-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1400-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1400-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1400-125">입력</span><span class="sxs-lookup"><span data-stu-id="d1400-125">INPUTS</span></span>

### <span data-ttu-id="d1400-126">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d1400-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d1400-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d1400-127">System.String</span></span>

## <span data-ttu-id="d1400-128">출력</span><span class="sxs-lookup"><span data-stu-id="d1400-128">OUTPUTS</span></span>

### <span data-ttu-id="d1400-129">ApiManagement. ServiceManagement. \ PsApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="d1400-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span></span>

## <span data-ttu-id="d1400-130">상속자</span><span class="sxs-lookup"><span data-stu-id="d1400-130">NOTES</span></span>

## <span data-ttu-id="d1400-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1400-131">RELATED LINKS</span></span>
