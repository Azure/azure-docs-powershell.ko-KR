---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
ms.openlocfilehash: 485150470bce308d3ab6d1a9a70eabd887abab09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531511"
---
# <span data-ttu-id="7e509-101">Get-AzureRmApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="7e509-101">Get-AzureRmApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="7e509-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e509-102">SYNOPSIS</span></span>
<span data-ttu-id="7e509-103">사용자에 대 한 SSO URL을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e509-103">Generates an SSO URL for a user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e509-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7e509-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e509-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7e509-105">DESCRIPTION</span></span>
<span data-ttu-id="7e509-106">**AzureRmApiManagementUserSsoUrl** cmdlet은 사용자의 SSO (single SIGN-ON) URL을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e509-106">The **Get-AzureRmApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="7e509-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7e509-107">EXAMPLES</span></span>

### <span data-ttu-id="7e509-108">예제 1: 사용자의 SSO URL 가져오기</span><span class="sxs-lookup"><span data-stu-id="7e509-108">Example 1: Get a user's SSO URL</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="7e509-109">이 명령은 사용자의 SSO URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7e509-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="7e509-110">변수</span><span class="sxs-lookup"><span data-stu-id="7e509-110">PARAMETERS</span></span>

### <span data-ttu-id="7e509-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="7e509-111">-Context</span></span>
<span data-ttu-id="7e509-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e509-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="7e509-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="7e509-113">This parameter is required.</span></span>

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

### <span data-ttu-id="7e509-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e509-114">-DefaultProfile</span></span>
<span data-ttu-id="7e509-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7e509-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e509-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="7e509-116">-UserId</span></span>
<span data-ttu-id="7e509-117">사용자 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e509-117">Specifies a user ID.</span></span>
<span data-ttu-id="7e509-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="7e509-118">This parameter is required.</span></span>

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

### <span data-ttu-id="7e509-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e509-119">CommonParameters</span></span>
<span data-ttu-id="7e509-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e509-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e509-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e509-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e509-122">입력</span><span class="sxs-lookup"><span data-stu-id="7e509-122">INPUTS</span></span>

### <span data-ttu-id="7e509-123">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7e509-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7e509-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7e509-124">System.String</span></span>

## <span data-ttu-id="7e509-125">출력</span><span class="sxs-lookup"><span data-stu-id="7e509-125">OUTPUTS</span></span>

### <span data-ttu-id="7e509-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7e509-126">System.String</span></span>

## <span data-ttu-id="7e509-127">상속자</span><span class="sxs-lookup"><span data-stu-id="7e509-127">NOTES</span></span>

## <span data-ttu-id="7e509-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e509-128">RELATED LINKS</span></span>

[<span data-ttu-id="7e509-129">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7e509-129">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


