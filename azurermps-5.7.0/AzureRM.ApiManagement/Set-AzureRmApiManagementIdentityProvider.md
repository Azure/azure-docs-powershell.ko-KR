---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: e45ec5a3d49bf82ab945a3ef3b41362a1e1e2bd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536848"
---
# <span data-ttu-id="d37e6-101">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="d37e6-101">Set-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="d37e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d37e6-102">SYNOPSIS</span></span>
<span data-ttu-id="d37e6-103">기존 Id 공급자의 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d37e6-103">Updates the Configuration of an existing Identity Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d37e6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d37e6-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d37e6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d37e6-105">DESCRIPTION</span></span>
<span data-ttu-id="d37e6-106">기존 Id 공급자의 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d37e6-106">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="d37e6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d37e6-107">EXAMPLES</span></span>

### <span data-ttu-id="d37e6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d37e6-108">Example 1</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Set-AzureRmApiManagementIdentityProvider -Context $apimContext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="d37e6-109">Cmdlet은 Facebook Id 공급자의 클라이언트 비밀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d37e6-109">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="d37e6-110">변수</span><span class="sxs-lookup"><span data-stu-id="d37e6-110">PARAMETERS</span></span>

### <span data-ttu-id="d37e6-111">-AllowedTenants 넌 트</span><span class="sxs-lookup"><span data-stu-id="d37e6-111">-AllowedTenants</span></span>
<span data-ttu-id="d37e6-112">허용 되는 Azure Active Directory 테 넌 트 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="d37e6-112">List of allowed Azure Active Directory Tenants.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d37e6-113">-ClientId</span><span class="sxs-lookup"><span data-stu-id="d37e6-113">-ClientId</span></span>
<span data-ttu-id="d37e6-114">외부 Id 공급자의 응용 프로그램에 대 한 클라이언트 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="d37e6-114">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="d37e6-115">Facebook 로그인의 앱 ID, Google 로그인의 클라이언트 ID, Microsoft의 앱 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d37e6-115">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d37e6-116">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="d37e6-116">-ClientSecret</span></span>
<span data-ttu-id="d37e6-117">로그인 요청을 인증 하는 데 사용 되는 외부 Id 공급자에 해당 하는 응용 프로그램의 클라이언트 비밀입니다.</span><span class="sxs-lookup"><span data-stu-id="d37e6-117">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="d37e6-118">예를 들어 Facebook 로그인에 대 한 앱 비밀, Google 로그인의 API 키, Microsoft의 공개 키입니다.</span><span class="sxs-lookup"><span data-stu-id="d37e6-118">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d37e6-119">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="d37e6-119">-Context</span></span>
<span data-ttu-id="d37e6-120">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="d37e6-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d37e6-121">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="d37e6-121">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d37e6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d37e6-122">-DefaultProfile</span></span>
<span data-ttu-id="d37e6-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d37e6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37e6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d37e6-124">-PassThru</span></span>
<span data-ttu-id="d37e6-125">이 cmdlet이이 cmdlet이 수정 하는  **PsApiManagementIdentityProvider** 를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d37e6-125">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d37e6-126">-Type</span><span class="sxs-lookup"><span data-stu-id="d37e6-126">-Type</span></span>
<span data-ttu-id="d37e6-127">기존 Id 공급자의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d37e6-127">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="d37e6-128">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="d37e6-128">This parameter is required.</span></span>

```yaml
Type: PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d37e6-129">-확인</span><span class="sxs-lookup"><span data-stu-id="d37e6-129">-Confirm</span></span>
<span data-ttu-id="d37e6-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d37e6-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37e6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d37e6-131">-WhatIf</span></span>
<span data-ttu-id="d37e6-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d37e6-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d37e6-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d37e6-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37e6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d37e6-134">CommonParameters</span></span>
<span data-ttu-id="d37e6-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d37e6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d37e6-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d37e6-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d37e6-137">입력</span><span class="sxs-lookup"><span data-stu-id="d37e6-137">INPUTS</span></span>

### <span data-ttu-id="d37e6-138">않아야</span><span class="sxs-lookup"><span data-stu-id="d37e6-138">None</span></span>
<span data-ttu-id="d37e6-139">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d37e6-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d37e6-140">출력</span><span class="sxs-lookup"><span data-stu-id="d37e6-140">OUTPUTS</span></span>

### <span data-ttu-id="d37e6-141">ApiManagement. ServiceManagement. \ PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="d37e6-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="d37e6-142">상속자</span><span class="sxs-lookup"><span data-stu-id="d37e6-142">NOTES</span></span>

## <span data-ttu-id="d37e6-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d37e6-143">RELATED LINKS</span></span>

[<span data-ttu-id="d37e6-144">새로운 AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="d37e6-144">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="d37e6-145">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="d37e6-145">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="d37e6-146">제거-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="d37e6-146">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)
