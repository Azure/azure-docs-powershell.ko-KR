---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
ms.openlocfilehash: e653053264baaa343b474f534f30915d725e5553
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990607"
---
# <span data-ttu-id="da6d4-101">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="da6d4-101">Get-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="da6d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da6d4-102">SYNOPSIS</span></span>
<span data-ttu-id="da6d4-103">API의 모든 API 개정에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="da6d4-103">Gets details of all the API Revisions of an API</span></span>

## <span data-ttu-id="da6d4-104">구문</span><span class="sxs-lookup"><span data-stu-id="da6d4-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da6d4-105">설명</span><span class="sxs-lookup"><span data-stu-id="da6d4-105">DESCRIPTION</span></span>
<span data-ttu-id="da6d4-106">**Get-AzApiManagementApiRevision** cmdlet은 API의 모든 개정에 대한 세부 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="da6d4-106">The **Get-AzApiManagementApiRevision** cmdlet gets the details of all revisions of an API</span></span>

## <span data-ttu-id="da6d4-107">예제</span><span class="sxs-lookup"><span data-stu-id="da6d4-107">EXAMPLES</span></span>

### <span data-ttu-id="da6d4-108">예제 1: API의 모든 API 개정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="da6d4-108">Example 1: Get all API Revisions of an API</span></span>
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

<span data-ttu-id="da6d4-109">이 명령은 특정 ApiManagement 컨텍스트에 대해 지정된 API의 모든 API 개정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="da6d4-109">This command gets all of the API revision of specified API for particular ApiManagement Context.</span></span>

## <span data-ttu-id="da6d4-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="da6d4-110">PARAMETERS</span></span>

### <span data-ttu-id="da6d4-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="da6d4-111">-ApiId</span></span>
<span data-ttu-id="da6d4-112">나열하려는 개정된 API 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="da6d4-112">API identifier whose revisions we want to list.</span></span>
<span data-ttu-id="da6d4-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="da6d4-113">This parameter is required.</span></span>

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

### <span data-ttu-id="da6d4-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="da6d4-114">-ApiRevision</span></span>
<span data-ttu-id="da6d4-115">특정 Api 개정의 개정 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="da6d4-115">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="da6d4-116">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="da6d4-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="da6d4-117">-Context</span><span class="sxs-lookup"><span data-stu-id="da6d4-117">-Context</span></span>
<span data-ttu-id="da6d4-118">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="da6d4-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="da6d4-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="da6d4-119">This parameter is required.</span></span>

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

### <span data-ttu-id="da6d4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da6d4-120">-DefaultProfile</span></span>
<span data-ttu-id="da6d4-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="da6d4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da6d4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da6d4-122">CommonParameters</span></span>
<span data-ttu-id="da6d4-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="da6d4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da6d4-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da6d4-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da6d4-125">입력</span><span class="sxs-lookup"><span data-stu-id="da6d4-125">INPUTS</span></span>

### <span data-ttu-id="da6d4-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="da6d4-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="da6d4-127">System.String</span><span class="sxs-lookup"><span data-stu-id="da6d4-127">System.String</span></span>

## <span data-ttu-id="da6d4-128">출력</span><span class="sxs-lookup"><span data-stu-id="da6d4-128">OUTPUTS</span></span>

### <span data-ttu-id="da6d4-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="da6d4-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span></span>

## <span data-ttu-id="da6d4-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="da6d4-130">NOTES</span></span>

## <span data-ttu-id="da6d4-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da6d4-131">RELATED LINKS</span></span>
