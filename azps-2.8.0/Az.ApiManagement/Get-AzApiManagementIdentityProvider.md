---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: f3692383f5fc93c0d76951f6dcaeb409ae3ee0f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698108"
---
# <span data-ttu-id="05bc5-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="05bc5-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="05bc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05bc5-102">SYNOPSIS</span></span>
<span data-ttu-id="05bc5-103">Id 공급자 구성 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="05bc5-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="05bc5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="05bc5-104">SYNTAX</span></span>

### <span data-ttu-id="05bc5-105">AllIdentityProviders (기본값)</span><span class="sxs-lookup"><span data-stu-id="05bc5-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05bc5-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="05bc5-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05bc5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="05bc5-107">DESCRIPTION</span></span>
<span data-ttu-id="05bc5-108">Id 공급자 구성 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="05bc5-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="05bc5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="05bc5-109">EXAMPLES</span></span>

### <span data-ttu-id="05bc5-110">예제 1: 모든 Id 공급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="05bc5-110">Example 1: Get all Identity Providers</span></span>

```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="05bc5-111">서비스에서 모든 id 공급자 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="05bc5-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="05bc5-112">AAD 형식 Id 공급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="05bc5-112">Get the AAD Type Identity Provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext -Type Aad
```

<span data-ttu-id="05bc5-113">Azure Active Directory의 Id 공급자 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="05bc5-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="05bc5-114">변수</span><span class="sxs-lookup"><span data-stu-id="05bc5-114">PARAMETERS</span></span>

### <span data-ttu-id="05bc5-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="05bc5-115">-Context</span></span>
<span data-ttu-id="05bc5-116">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="05bc5-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="05bc5-117">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="05bc5-117">This parameter is required.</span></span>

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

### <span data-ttu-id="05bc5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05bc5-118">-DefaultProfile</span></span>
<span data-ttu-id="05bc5-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="05bc5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05bc5-120">-Type</span><span class="sxs-lookup"><span data-stu-id="05bc5-120">-Type</span></span>
<span data-ttu-id="05bc5-121">Id 공급자의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="05bc5-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="05bc5-122">지정 된 경우 식별자를 사용 하 여 id 공급자 구성을 찾으려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="05bc5-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="05bc5-123">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="05bc5-123">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05bc5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05bc5-124">CommonParameters</span></span>
<span data-ttu-id="05bc5-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="05bc5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05bc5-126">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="05bc5-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05bc5-127">입력</span><span class="sxs-lookup"><span data-stu-id="05bc5-127">INPUTS</span></span>

### <span data-ttu-id="05bc5-128">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="05bc5-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="05bc5-129">ApiManagement. ServiceManagement. \ PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="05bc5-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="05bc5-130">출력</span><span class="sxs-lookup"><span data-stu-id="05bc5-130">OUTPUTS</span></span>

### <span data-ttu-id="05bc5-131">ApiManagement. ServiceManagement. \ PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="05bc5-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="05bc5-132">상속자</span><span class="sxs-lookup"><span data-stu-id="05bc5-132">NOTES</span></span>

## <span data-ttu-id="05bc5-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05bc5-133">RELATED LINKS</span></span>
