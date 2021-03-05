---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementopenidconnectproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
ms.openlocfilehash: 0c6757b32a81c689b4b9bbc3397fdd52c19ae4bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014363"
---
# <span data-ttu-id="ad493-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="ad493-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span></span>

## <span data-ttu-id="ad493-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad493-102">SYNOPSIS</span></span>
<span data-ttu-id="ad493-103">OpenID Connect 공급자 클라이언트 비밀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ad493-103">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="ad493-104">구문</span><span class="sxs-lookup"><span data-stu-id="ad493-104">SYNTAX</span></span>

```
Get-AzApiManagementOpenIdConnectProviderClientSecret -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad493-105">설명</span><span class="sxs-lookup"><span data-stu-id="ad493-105">DESCRIPTION</span></span>
<span data-ttu-id="ad493-106">OpenID Connect 공급자 클라이언트 비밀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ad493-106">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="ad493-107">예제</span><span class="sxs-lookup"><span data-stu-id="ad493-107">EXAMPLES</span></span>

### <span data-ttu-id="ad493-108">예제 1: ID를 사용하여 공급자 클라이언트 비밀을 얻다</span><span class="sxs-lookup"><span data-stu-id="ad493-108">Example 1: Get a provider client secret by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProviderClientSecret -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="ad493-109">이 명령은 ID OICProvider01이 있는 공급자의 클라이언트 비밀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ad493-109">This command gets a client secret of the provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="ad493-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ad493-110">PARAMETERS</span></span>

### <span data-ttu-id="ad493-111">-Context</span><span class="sxs-lookup"><span data-stu-id="ad493-111">-Context</span></span>
<span data-ttu-id="ad493-112">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="ad493-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ad493-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="ad493-113">This parameter is required.</span></span>

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

### <span data-ttu-id="ad493-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad493-114">-DefaultProfile</span></span>
<span data-ttu-id="ad493-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ad493-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad493-116">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="ad493-116">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="ad493-117">OpenID Connect 공급자의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="ad493-117">Identifier of a OpenID Connect Provider.</span></span>
<span data-ttu-id="ad493-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="ad493-118">This parameter is required.</span></span>

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

### <span data-ttu-id="ad493-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad493-119">CommonParameters</span></span>
<span data-ttu-id="ad493-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ad493-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad493-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad493-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad493-122">입력</span><span class="sxs-lookup"><span data-stu-id="ad493-122">INPUTS</span></span>

### <span data-ttu-id="ad493-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ad493-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ad493-124">System.String</span><span class="sxs-lookup"><span data-stu-id="ad493-124">System.String</span></span>

## <span data-ttu-id="ad493-125">출력</span><span class="sxs-lookup"><span data-stu-id="ad493-125">OUTPUTS</span></span>

### <span data-ttu-id="ad493-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="ad493-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="ad493-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ad493-127">NOTES</span></span>

## <span data-ttu-id="ad493-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad493-128">RELATED LINKS</span></span>
