---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
ms.openlocfilehash: d75d385bc158e0855601d3432dff79b2e4339f2f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365856"
---
# <span data-ttu-id="d6ea1-101">Get-AzApiManagementIdentityProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="d6ea1-101">Get-AzApiManagementIdentityProviderClientSecret</span></span>

## <span data-ttu-id="d6ea1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6ea1-102">SYNOPSIS</span></span>
<span data-ttu-id="d6ea1-103">ID 공급자 클라이언트 비밀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d6ea1-103">Get the identity provider client secret.</span></span>

## <span data-ttu-id="d6ea1-104">구문</span><span class="sxs-lookup"><span data-stu-id="d6ea1-104">SYNTAX</span></span>

```
Get-AzApiManagementIdentityProviderClientSecret -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6ea1-105">설명</span><span class="sxs-lookup"><span data-stu-id="d6ea1-105">DESCRIPTION</span></span>
<span data-ttu-id="d6ea1-106">ID 공급자 클라이언트 비밀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d6ea1-106">Get the identity provider client secret.</span></span>

## <span data-ttu-id="d6ea1-107">예제</span><span class="sxs-lookup"><span data-stu-id="d6ea1-107">EXAMPLES</span></span>

### <span data-ttu-id="d6ea1-108">예제 1: AAD 형식 ID 공급자의 클라이언트 비밀을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d6ea1-108">Example 1: Get the client secret of AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProviderClientSecret -Context $apimContext -Type Aad
```

<span data-ttu-id="d6ea1-109">Azure Active Directory의 ID 공급자 구성에 대한 클라이언트 비밀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d6ea1-109">Gets the client secret of the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="d6ea1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6ea1-110">PARAMETERS</span></span>

### <span data-ttu-id="d6ea1-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d6ea1-111">-Context</span></span>
<span data-ttu-id="d6ea1-112">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="d6ea1-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d6ea1-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="d6ea1-113">This parameter is required.</span></span>

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

### <span data-ttu-id="d6ea1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6ea1-114">-DefaultProfile</span></span>
<span data-ttu-id="d6ea1-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d6ea1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6ea1-116">-Type</span><span class="sxs-lookup"><span data-stu-id="d6ea1-116">-Type</span></span>
<span data-ttu-id="d6ea1-117">ID 공급자의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d6ea1-117">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="d6ea1-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="d6ea1-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ea1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6ea1-119">CommonParameters</span></span>
<span data-ttu-id="d6ea1-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d6ea1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6ea1-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d6ea1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6ea1-122">입력</span><span class="sxs-lookup"><span data-stu-id="d6ea1-122">INPUTS</span></span>

### <span data-ttu-id="d6ea1-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d6ea1-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d6ea1-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="d6ea1-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="d6ea1-125">출력</span><span class="sxs-lookup"><span data-stu-id="d6ea1-125">OUTPUTS</span></span>

### <span data-ttu-id="d6ea1-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="d6ea1-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="d6ea1-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d6ea1-127">NOTES</span></span>

## <span data-ttu-id="d6ea1-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d6ea1-128">RELATED LINKS</span></span>
