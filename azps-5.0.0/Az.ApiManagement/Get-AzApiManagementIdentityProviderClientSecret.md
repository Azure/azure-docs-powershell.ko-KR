---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
ms.openlocfilehash: d75d385bc158e0855601d3432dff79b2e4339f2f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307649"
---
# <span data-ttu-id="3d08d-101">Get-AzApiManagementIdentityProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="3d08d-101">Get-AzApiManagementIdentityProviderClientSecret</span></span>

## <span data-ttu-id="3d08d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d08d-102">SYNOPSIS</span></span>
<span data-ttu-id="3d08d-103">Id 공급자 클라이언트 비밀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3d08d-103">Get the identity provider client secret.</span></span>

## <span data-ttu-id="3d08d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3d08d-104">SYNTAX</span></span>

```
Get-AzApiManagementIdentityProviderClientSecret -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d08d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3d08d-105">DESCRIPTION</span></span>
<span data-ttu-id="3d08d-106">Id 공급자 클라이언트 비밀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3d08d-106">Get the identity provider client secret.</span></span>

## <span data-ttu-id="3d08d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3d08d-107">EXAMPLES</span></span>

### <span data-ttu-id="3d08d-108">예제 1: AAD 형식 Id 공급자의 클라이언트 비밀 가져오기</span><span class="sxs-lookup"><span data-stu-id="3d08d-108">Example 1: Get the client secret of AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProviderClientSecret -Context $apimContext -Type Aad
```

<span data-ttu-id="3d08d-109">Azure Active Directory의 Id 공급자 구성에 대 한 클라이언트 암호를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3d08d-109">Gets the client secret of the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="3d08d-110">변수</span><span class="sxs-lookup"><span data-stu-id="3d08d-110">PARAMETERS</span></span>

### <span data-ttu-id="3d08d-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="3d08d-111">-Context</span></span>
<span data-ttu-id="3d08d-112">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="3d08d-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3d08d-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="3d08d-113">This parameter is required.</span></span>

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

### <span data-ttu-id="3d08d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d08d-114">-DefaultProfile</span></span>
<span data-ttu-id="3d08d-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3d08d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d08d-116">-Type</span><span class="sxs-lookup"><span data-stu-id="3d08d-116">-Type</span></span>
<span data-ttu-id="3d08d-117">Id 공급자의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="3d08d-117">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="3d08d-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="3d08d-118">This parameter is required.</span></span>

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

### <span data-ttu-id="3d08d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d08d-119">CommonParameters</span></span>
<span data-ttu-id="3d08d-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d08d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d08d-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3d08d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d08d-122">입력</span><span class="sxs-lookup"><span data-stu-id="3d08d-122">INPUTS</span></span>

### <span data-ttu-id="3d08d-123">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3d08d-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3d08d-124">ApiManagement. ServiceManagement. \ PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="3d08d-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="3d08d-125">출력</span><span class="sxs-lookup"><span data-stu-id="3d08d-125">OUTPUTS</span></span>

### <span data-ttu-id="3d08d-126">ApiManagement. ServiceManagement. \ PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="3d08d-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="3d08d-127">상속자</span><span class="sxs-lookup"><span data-stu-id="3d08d-127">NOTES</span></span>

## <span data-ttu-id="3d08d-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d08d-128">RELATED LINKS</span></span>
