---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: fe320af601fad9d905471525b1a418c12c355f63
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869337"
---
# <span data-ttu-id="5fc9a-101">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5fc9a-101">Set-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="5fc9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fc9a-102">SYNOPSIS</span></span>
<span data-ttu-id="5fc9a-103">OpenID Connect provider를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-103">Modifies an OpenID Connect provider.</span></span>

## <span data-ttu-id="5fc9a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5fc9a-104">SYNTAX</span></span>

```
Set-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>] [-ClientSecret <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fc9a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5fc9a-105">DESCRIPTION</span></span>
<span data-ttu-id="5fc9a-106">**Set-AzApiManagementOpenIdConnectProvider** Cmdlet은 Azure API Management의 OpenID Connect 공급자를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-106">The **Set-AzApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="5fc9a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5fc9a-107">EXAMPLES</span></span>

### <span data-ttu-id="5fc9a-108">예제 1: 공급자에 대 한 클라이언트 비밀 변경</span><span class="sxs-lookup"><span data-stu-id="5fc9a-108">Example 1: Change the client secret for a provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="5fc9a-109">이 명령은 ID OICProvicer01 인 공급자를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="5fc9a-110">명령은 공급자에 대 한 클라이언트 비밀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="5fc9a-111">변수</span><span class="sxs-lookup"><span data-stu-id="5fc9a-111">PARAMETERS</span></span>

### <span data-ttu-id="5fc9a-112">-ClientId</span><span class="sxs-lookup"><span data-stu-id="5fc9a-112">-ClientId</span></span>
<span data-ttu-id="5fc9a-113">개발자 콘솔의 클라이언트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-113">Specifies the client ID of the developer console.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fc9a-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="5fc9a-114">-ClientSecret</span></span>
<span data-ttu-id="5fc9a-115">개발자 콘솔의 클라이언트 비밀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-115">Specifies the client secret of the developer console.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fc9a-116">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="5fc9a-116">-Context</span></span>
<span data-ttu-id="5fc9a-117">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5fc9a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fc9a-118">-DefaultProfile</span></span>
<span data-ttu-id="5fc9a-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fc9a-120">-설명</span><span class="sxs-lookup"><span data-stu-id="5fc9a-120">-Description</span></span>
<span data-ttu-id="5fc9a-121">설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-121">Specifies a description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fc9a-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="5fc9a-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="5fc9a-123">공급자의 메타 데이터 끝점 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-123">Specifies a metadata endpoint URI of the provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fc9a-124">-이름</span><span class="sxs-lookup"><span data-stu-id="5fc9a-124">-Name</span></span>
<span data-ttu-id="5fc9a-125">공급자에 대 한 친숙 한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-125">Specifies a friendly name for the provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fc9a-126">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="5fc9a-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="5fc9a-127">이 cmdlet이 수정 하는 공급자에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="5fc9a-128">ID를 지정 하지 않으면이 cmdlet이 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-128">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="5fc9a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5fc9a-129">-PassThru</span></span>
<span data-ttu-id="5fc9a-130">이 cmdlet이이 cmdlet이 수정 하는 **PsApiManagementOpenIdConnectProvider** 를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fc9a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fc9a-131">CommonParameters</span></span>
<span data-ttu-id="5fc9a-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fc9a-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fc9a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fc9a-134">입력</span><span class="sxs-lookup"><span data-stu-id="5fc9a-134">INPUTS</span></span>

### <span data-ttu-id="5fc9a-135">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5fc9a-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5fc9a-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5fc9a-136">System.String</span></span>

### <span data-ttu-id="5fc9a-137">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5fc9a-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5fc9a-138">출력</span><span class="sxs-lookup"><span data-stu-id="5fc9a-138">OUTPUTS</span></span>

### <span data-ttu-id="5fc9a-139">ApiManagement. ServiceManagement. \ PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5fc9a-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="5fc9a-140">상속자</span><span class="sxs-lookup"><span data-stu-id="5fc9a-140">NOTES</span></span>

## <span data-ttu-id="5fc9a-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5fc9a-141">RELATED LINKS</span></span>

[<span data-ttu-id="5fc9a-142">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5fc9a-142">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="5fc9a-143">새로운 AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5fc9a-143">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="5fc9a-144">제거-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5fc9a-144">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)


