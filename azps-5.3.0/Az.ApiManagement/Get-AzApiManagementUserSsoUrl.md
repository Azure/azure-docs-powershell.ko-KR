---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: be30497c444d90b9239b5dc3dcd351fbe9a63f0b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494415"
---
# <span data-ttu-id="2dbc5-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="2dbc5-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="2dbc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dbc5-102">SYNOPSIS</span></span>
<span data-ttu-id="2dbc5-103">사용자에 대한 SSO URL을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="2dbc5-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="2dbc5-104">구문</span><span class="sxs-lookup"><span data-stu-id="2dbc5-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2dbc5-105">설명</span><span class="sxs-lookup"><span data-stu-id="2dbc5-105">DESCRIPTION</span></span>
<span data-ttu-id="2dbc5-106">**Get-AzApiManagementUserSsoUrl** cmdlet은 사용자에 대한 SSO(Single Sign-On) URL을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="2dbc5-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="2dbc5-107">예제</span><span class="sxs-lookup"><span data-stu-id="2dbc5-107">EXAMPLES</span></span>

### <span data-ttu-id="2dbc5-108">예제 1: 사용자의 SSO URL을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="2dbc5-108">Example 1: Get a user's SSO URL</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="2dbc5-109">이 명령은 사용자의 SSO URL을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2dbc5-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="2dbc5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2dbc5-110">PARAMETERS</span></span>

### <span data-ttu-id="2dbc5-111">-Context</span><span class="sxs-lookup"><span data-stu-id="2dbc5-111">-Context</span></span>
<span data-ttu-id="2dbc5-112">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="2dbc5-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="2dbc5-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="2dbc5-113">This parameter is required.</span></span>

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

### <span data-ttu-id="2dbc5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dbc5-114">-DefaultProfile</span></span>
<span data-ttu-id="2dbc5-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2dbc5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2dbc5-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="2dbc5-116">-UserId</span></span>
<span data-ttu-id="2dbc5-117">사용자 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2dbc5-117">Specifies a user ID.</span></span>
<span data-ttu-id="2dbc5-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="2dbc5-118">This parameter is required.</span></span>

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

### <span data-ttu-id="2dbc5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dbc5-119">CommonParameters</span></span>
<span data-ttu-id="2dbc5-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2dbc5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dbc5-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2dbc5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dbc5-122">입력</span><span class="sxs-lookup"><span data-stu-id="2dbc5-122">INPUTS</span></span>

### <span data-ttu-id="2dbc5-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2dbc5-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2dbc5-124">System.String</span><span class="sxs-lookup"><span data-stu-id="2dbc5-124">System.String</span></span>

## <span data-ttu-id="2dbc5-125">출력</span><span class="sxs-lookup"><span data-stu-id="2dbc5-125">OUTPUTS</span></span>

### <span data-ttu-id="2dbc5-126">System.String</span><span class="sxs-lookup"><span data-stu-id="2dbc5-126">System.String</span></span>

## <span data-ttu-id="2dbc5-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2dbc5-127">NOTES</span></span>

## <span data-ttu-id="2dbc5-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2dbc5-128">RELATED LINKS</span></span>

[<span data-ttu-id="2dbc5-129">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="2dbc5-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


