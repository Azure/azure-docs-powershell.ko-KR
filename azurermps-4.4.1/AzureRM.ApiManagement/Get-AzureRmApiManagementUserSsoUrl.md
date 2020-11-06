---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
ms.openlocfilehash: a13d37100e553d8d56cf5b040a796adabe08b7d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531286"
---
# <span data-ttu-id="92d4a-101">Get-AzureRmApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="92d4a-101">Get-AzureRmApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="92d4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92d4a-102">SYNOPSIS</span></span>
<span data-ttu-id="92d4a-103">사용자에 대 한 SSO URL을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="92d4a-103">Generates an SSO URL for a user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92d4a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="92d4a-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92d4a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="92d4a-105">DESCRIPTION</span></span>
<span data-ttu-id="92d4a-106">**AzureRmApiManagementUserSsoUrl** cmdlet은 사용자의 SSO (single SIGN-ON) URL을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="92d4a-106">The **Get-AzureRmApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="92d4a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="92d4a-107">EXAMPLES</span></span>

### <span data-ttu-id="92d4a-108">예제 1: 사용자의 SSO URL 가져오기</span><span class="sxs-lookup"><span data-stu-id="92d4a-108">Example 1: Get a user's SSO URL</span></span>
```
PS C:\>Get-AzureRmApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="92d4a-109">이 명령은 사용자의 SSO URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="92d4a-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="92d4a-110">변수</span><span class="sxs-lookup"><span data-stu-id="92d4a-110">PARAMETERS</span></span>

### <span data-ttu-id="92d4a-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="92d4a-111">-Context</span></span>
<span data-ttu-id="92d4a-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92d4a-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="92d4a-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="92d4a-113">This parameter is required.</span></span>

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

### <span data-ttu-id="92d4a-114">-UserId</span><span class="sxs-lookup"><span data-stu-id="92d4a-114">-UserId</span></span>
<span data-ttu-id="92d4a-115">사용자 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92d4a-115">Specifies a user ID.</span></span>
<span data-ttu-id="92d4a-116">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="92d4a-116">This parameter is required.</span></span>

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

### <span data-ttu-id="92d4a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92d4a-117">-DefaultProfile</span></span>
<span data-ttu-id="92d4a-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="92d4a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92d4a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92d4a-119">CommonParameters</span></span>
<span data-ttu-id="92d4a-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="92d4a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92d4a-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92d4a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92d4a-122">입력</span><span class="sxs-lookup"><span data-stu-id="92d4a-122">INPUTS</span></span>

## <span data-ttu-id="92d4a-123">출력</span><span class="sxs-lookup"><span data-stu-id="92d4a-123">OUTPUTS</span></span>

### <span data-ttu-id="92d4a-124">이름</span><span class="sxs-lookup"><span data-stu-id="92d4a-124">string</span></span>

## <span data-ttu-id="92d4a-125">상속자</span><span class="sxs-lookup"><span data-stu-id="92d4a-125">NOTES</span></span>

## <span data-ttu-id="92d4a-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="92d4a-126">RELATED LINKS</span></span>

[<span data-ttu-id="92d4a-127">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="92d4a-127">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


