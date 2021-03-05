---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: b4c89a1f0da5e4ce07d9d2174fce031365e09cb4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979072"
---
# <span data-ttu-id="968f1-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="968f1-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="968f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="968f1-102">SYNOPSIS</span></span>
<span data-ttu-id="968f1-103">사용자에 대한 SSO URL을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="968f1-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="968f1-104">구문</span><span class="sxs-lookup"><span data-stu-id="968f1-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="968f1-105">설명</span><span class="sxs-lookup"><span data-stu-id="968f1-105">DESCRIPTION</span></span>
<span data-ttu-id="968f1-106">**Get-AzApiManagementUserSsoUrl** cmdlet은 사용자에 대한 SSO(Single Sign-On) URL을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="968f1-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="968f1-107">예제</span><span class="sxs-lookup"><span data-stu-id="968f1-107">EXAMPLES</span></span>

### <span data-ttu-id="968f1-108">예제 1: 사용자의 SSO URL을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="968f1-108">Example 1: Get a user's SSO URL</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="968f1-109">이 명령은 사용자의 SSO URL을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="968f1-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="968f1-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="968f1-110">PARAMETERS</span></span>

### <span data-ttu-id="968f1-111">-Context</span><span class="sxs-lookup"><span data-stu-id="968f1-111">-Context</span></span>
<span data-ttu-id="968f1-112">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="968f1-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="968f1-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="968f1-113">This parameter is required.</span></span>

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

### <span data-ttu-id="968f1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="968f1-114">-DefaultProfile</span></span>
<span data-ttu-id="968f1-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="968f1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="968f1-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="968f1-116">-UserId</span></span>
<span data-ttu-id="968f1-117">사용자 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="968f1-117">Specifies a user ID.</span></span>
<span data-ttu-id="968f1-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="968f1-118">This parameter is required.</span></span>

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

### <span data-ttu-id="968f1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="968f1-119">CommonParameters</span></span>
<span data-ttu-id="968f1-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="968f1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="968f1-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="968f1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="968f1-122">입력</span><span class="sxs-lookup"><span data-stu-id="968f1-122">INPUTS</span></span>

### <span data-ttu-id="968f1-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="968f1-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="968f1-124">System.String</span><span class="sxs-lookup"><span data-stu-id="968f1-124">System.String</span></span>

## <span data-ttu-id="968f1-125">출력</span><span class="sxs-lookup"><span data-stu-id="968f1-125">OUTPUTS</span></span>

### <span data-ttu-id="968f1-126">System.String</span><span class="sxs-lookup"><span data-stu-id="968f1-126">System.String</span></span>

## <span data-ttu-id="968f1-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="968f1-127">NOTES</span></span>

## <span data-ttu-id="968f1-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="968f1-128">RELATED LINKS</span></span>

[<span data-ttu-id="968f1-129">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="968f1-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


