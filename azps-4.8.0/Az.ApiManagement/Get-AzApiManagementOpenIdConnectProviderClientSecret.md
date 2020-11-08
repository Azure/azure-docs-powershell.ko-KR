---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
ms.openlocfilehash: dcc66b6d28157ff9d5551e2fdf0cab18f7727828
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048018"
---
# <span data-ttu-id="5e8d3-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="5e8d3-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span></span>

## <span data-ttu-id="5e8d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e8d3-102">SYNOPSIS</span></span>
<span data-ttu-id="5e8d3-103">OpenID Connect provider 클라이언트 비밀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5e8d3-103">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="5e8d3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5e8d3-104">SYNTAX</span></span>

```
Get-AzApiManagementOpenIdConnectProviderClientSecret -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e8d3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5e8d3-105">DESCRIPTION</span></span>
<span data-ttu-id="5e8d3-106">OpenID Connect provider 클라이언트 비밀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5e8d3-106">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="5e8d3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5e8d3-107">EXAMPLES</span></span>

### <span data-ttu-id="5e8d3-108">예제 1: ID를 사용 하 여 공급자 클라이언트 암호 가져오기</span><span class="sxs-lookup"><span data-stu-id="5e8d3-108">Example 1: Get a provider client secret by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProviderClientSecret -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="5e8d3-109">이 명령은 ID OICProvider01 인 공급자의 클라이언트 비밀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5e8d3-109">This command gets a client secret of the provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="5e8d3-110">변수</span><span class="sxs-lookup"><span data-stu-id="5e8d3-110">PARAMETERS</span></span>

### <span data-ttu-id="5e8d3-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="5e8d3-111">-Context</span></span>
<span data-ttu-id="5e8d3-112">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="5e8d3-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5e8d3-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="5e8d3-113">This parameter is required.</span></span>

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

### <span data-ttu-id="5e8d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e8d3-114">-DefaultProfile</span></span>
<span data-ttu-id="5e8d3-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5e8d3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e8d3-116">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="5e8d3-116">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="5e8d3-117">OpenID Connect Provider의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5e8d3-117">Identifier of a OpenID Connect Provider.</span></span>
<span data-ttu-id="5e8d3-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="5e8d3-118">This parameter is required.</span></span>

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

### <span data-ttu-id="5e8d3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e8d3-119">CommonParameters</span></span>
<span data-ttu-id="5e8d3-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e8d3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e8d3-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5e8d3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e8d3-122">입력</span><span class="sxs-lookup"><span data-stu-id="5e8d3-122">INPUTS</span></span>

### <span data-ttu-id="5e8d3-123">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5e8d3-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5e8d3-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5e8d3-124">System.String</span></span>

## <span data-ttu-id="5e8d3-125">출력</span><span class="sxs-lookup"><span data-stu-id="5e8d3-125">OUTPUTS</span></span>

### <span data-ttu-id="5e8d3-126">ApiManagement. ServiceManagement. \ PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="5e8d3-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="5e8d3-127">상속자</span><span class="sxs-lookup"><span data-stu-id="5e8d3-127">NOTES</span></span>

## <span data-ttu-id="5e8d3-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5e8d3-128">RELATED LINKS</span></span>
