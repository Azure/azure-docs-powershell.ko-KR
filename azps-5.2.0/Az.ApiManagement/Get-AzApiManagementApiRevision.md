---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
ms.openlocfilehash: 16c108d4f62d9bcc44176fce7ede9a7e56d98687
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366164"
---
# <span data-ttu-id="45eeb-101">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="45eeb-101">Get-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="45eeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45eeb-102">SYNOPSIS</span></span>
<span data-ttu-id="45eeb-103">API의 모든 API 개정에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="45eeb-103">Gets details of all the API Revisions of an API</span></span>

## <span data-ttu-id="45eeb-104">구문</span><span class="sxs-lookup"><span data-stu-id="45eeb-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45eeb-105">설명</span><span class="sxs-lookup"><span data-stu-id="45eeb-105">DESCRIPTION</span></span>
<span data-ttu-id="45eeb-106">**Get-AzApiManagementApiRevision** cmdlet은 API의 모든 개정에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="45eeb-106">The **Get-AzApiManagementApiRevision** cmdlet gets the details of all revisions of an API</span></span>

## <span data-ttu-id="45eeb-107">예제</span><span class="sxs-lookup"><span data-stu-id="45eeb-107">EXAMPLES</span></span>

### <span data-ttu-id="45eeb-108">예제 1: API의 모든 API 개정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="45eeb-108">Example 1: Get all API Revisions of an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "5adf6fbf0faadf3ad8558065"

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

<span data-ttu-id="45eeb-109">이 명령은 특정 ApiManagement 컨텍스트에 대해 지정된 API의 모든 API 개정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="45eeb-109">This command gets all of the API revision of specified API for particular ApiManagement Context.</span></span>

## <span data-ttu-id="45eeb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45eeb-110">PARAMETERS</span></span>

### <span data-ttu-id="45eeb-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="45eeb-111">-ApiId</span></span>
<span data-ttu-id="45eeb-112">나열하려는 개정이 있는 API 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="45eeb-112">API identifier whose revisions we want to list.</span></span>
<span data-ttu-id="45eeb-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="45eeb-113">This parameter is required.</span></span>

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

### <span data-ttu-id="45eeb-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="45eeb-114">-ApiRevision</span></span>
<span data-ttu-id="45eeb-115">특정 API 개정의 개정 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="45eeb-115">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="45eeb-116">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="45eeb-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="45eeb-117">-Context</span><span class="sxs-lookup"><span data-stu-id="45eeb-117">-Context</span></span>
<span data-ttu-id="45eeb-118">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="45eeb-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="45eeb-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="45eeb-119">This parameter is required.</span></span>

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

### <span data-ttu-id="45eeb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45eeb-120">-DefaultProfile</span></span>
<span data-ttu-id="45eeb-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="45eeb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45eeb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45eeb-122">CommonParameters</span></span>
<span data-ttu-id="45eeb-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="45eeb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45eeb-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="45eeb-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45eeb-125">입력</span><span class="sxs-lookup"><span data-stu-id="45eeb-125">INPUTS</span></span>

### <span data-ttu-id="45eeb-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="45eeb-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="45eeb-127">System.String</span><span class="sxs-lookup"><span data-stu-id="45eeb-127">System.String</span></span>

## <span data-ttu-id="45eeb-128">출력</span><span class="sxs-lookup"><span data-stu-id="45eeb-128">OUTPUTS</span></span>

### <span data-ttu-id="45eeb-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="45eeb-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span></span>

## <span data-ttu-id="45eeb-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="45eeb-130">NOTES</span></span>

## <span data-ttu-id="45eeb-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="45eeb-131">RELATED LINKS</span></span>
