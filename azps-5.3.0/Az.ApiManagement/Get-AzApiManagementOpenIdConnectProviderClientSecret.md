---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
ms.openlocfilehash: dcc66b6d28157ff9d5551e2fdf0cab18f7727828
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494442"
---
# <span data-ttu-id="09d35-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="09d35-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span></span>

## <span data-ttu-id="09d35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09d35-102">SYNOPSIS</span></span>
<span data-ttu-id="09d35-103">OpenID Connect 공급자 클라이언트 비밀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="09d35-103">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="09d35-104">구문</span><span class="sxs-lookup"><span data-stu-id="09d35-104">SYNTAX</span></span>

```
Get-AzApiManagementOpenIdConnectProviderClientSecret -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09d35-105">설명</span><span class="sxs-lookup"><span data-stu-id="09d35-105">DESCRIPTION</span></span>
<span data-ttu-id="09d35-106">OpenID Connect 공급자 클라이언트 비밀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="09d35-106">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="09d35-107">예제</span><span class="sxs-lookup"><span data-stu-id="09d35-107">EXAMPLES</span></span>

### <span data-ttu-id="09d35-108">예제 1: ID를 사용하여 공급자 클라이언트 비밀을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="09d35-108">Example 1: Get a provider client secret by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProviderClientSecret -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="09d35-109">이 명령은 ID OICProvider01이 있는 공급자의 클라이언트 비밀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="09d35-109">This command gets a client secret of the provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="09d35-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09d35-110">PARAMETERS</span></span>

### <span data-ttu-id="09d35-111">-Context</span><span class="sxs-lookup"><span data-stu-id="09d35-111">-Context</span></span>
<span data-ttu-id="09d35-112">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="09d35-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="09d35-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="09d35-113">This parameter is required.</span></span>

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

### <span data-ttu-id="09d35-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09d35-114">-DefaultProfile</span></span>
<span data-ttu-id="09d35-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="09d35-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09d35-116">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="09d35-116">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="09d35-117">OpenID Connect 공급자의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="09d35-117">Identifier of a OpenID Connect Provider.</span></span>
<span data-ttu-id="09d35-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="09d35-118">This parameter is required.</span></span>

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

### <span data-ttu-id="09d35-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09d35-119">CommonParameters</span></span>
<span data-ttu-id="09d35-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="09d35-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09d35-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="09d35-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09d35-122">입력</span><span class="sxs-lookup"><span data-stu-id="09d35-122">INPUTS</span></span>

### <span data-ttu-id="09d35-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="09d35-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="09d35-124">System.String</span><span class="sxs-lookup"><span data-stu-id="09d35-124">System.String</span></span>

## <span data-ttu-id="09d35-125">출력</span><span class="sxs-lookup"><span data-stu-id="09d35-125">OUTPUTS</span></span>

### <span data-ttu-id="09d35-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="09d35-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="09d35-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="09d35-127">NOTES</span></span>

## <span data-ttu-id="09d35-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="09d35-128">RELATED LINKS</span></span>
