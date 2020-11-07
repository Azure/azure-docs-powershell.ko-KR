---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: 2a7a4d602b8e316377496af8ccb9c119338a5c99
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689122"
---
# <span data-ttu-id="0938a-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="0938a-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="0938a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0938a-102">SYNOPSIS</span></span>
<span data-ttu-id="0938a-103">사용자에 대 한 SSO URL을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0938a-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="0938a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0938a-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0938a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0938a-105">DESCRIPTION</span></span>
<span data-ttu-id="0938a-106">**AzApiManagementUserSsoUrl** cmdlet은 사용자의 SSO (single SIGN-ON) URL을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0938a-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="0938a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0938a-107">EXAMPLES</span></span>

### <span data-ttu-id="0938a-108">예제 1: 사용자의 SSO URL 가져오기</span><span class="sxs-lookup"><span data-stu-id="0938a-108">Example 1: Get a user's SSO URL</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="0938a-109">이 명령은 사용자의 SSO URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0938a-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="0938a-110">변수</span><span class="sxs-lookup"><span data-stu-id="0938a-110">PARAMETERS</span></span>

### <span data-ttu-id="0938a-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="0938a-111">-Context</span></span>
<span data-ttu-id="0938a-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0938a-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="0938a-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="0938a-113">This parameter is required.</span></span>

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

### <span data-ttu-id="0938a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0938a-114">-DefaultProfile</span></span>
<span data-ttu-id="0938a-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0938a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0938a-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="0938a-116">-UserId</span></span>
<span data-ttu-id="0938a-117">사용자 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0938a-117">Specifies a user ID.</span></span>
<span data-ttu-id="0938a-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="0938a-118">This parameter is required.</span></span>

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

### <span data-ttu-id="0938a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0938a-119">CommonParameters</span></span>
<span data-ttu-id="0938a-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0938a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0938a-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0938a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0938a-122">입력</span><span class="sxs-lookup"><span data-stu-id="0938a-122">INPUTS</span></span>

### <span data-ttu-id="0938a-123">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0938a-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0938a-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0938a-124">System.String</span></span>

## <span data-ttu-id="0938a-125">출력</span><span class="sxs-lookup"><span data-stu-id="0938a-125">OUTPUTS</span></span>

### <span data-ttu-id="0938a-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0938a-126">System.String</span></span>

## <span data-ttu-id="0938a-127">상속자</span><span class="sxs-lookup"><span data-stu-id="0938a-127">NOTES</span></span>

## <span data-ttu-id="0938a-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0938a-128">RELATED LINKS</span></span>

[<span data-ttu-id="0938a-129">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0938a-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


