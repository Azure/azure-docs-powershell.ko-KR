---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: f890236907ea0a717245d9345be276a6ccf04b8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531871"
---
# <span data-ttu-id="0eebc-101">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0eebc-101">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="0eebc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0eebc-102">SYNOPSIS</span></span>
<span data-ttu-id="0eebc-103">OpenID Connect provider를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eebc-103">Modifies an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0eebc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0eebc-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>]
 [-ClientSecret <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0eebc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0eebc-105">DESCRIPTION</span></span>
<span data-ttu-id="0eebc-106">**Set-AzureRmApiManagementOpenIdConnectProvider** Cmdlet은 Azure API Management의 OpenID Connect 공급자를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eebc-106">The **Set-AzureRmApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="0eebc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0eebc-107">EXAMPLES</span></span>

### <span data-ttu-id="0eebc-108">예제 1: 공급자에 대 한 클라이언트 비밀 변경</span><span class="sxs-lookup"><span data-stu-id="0eebc-108">Example 1: Change the client secret for a provider</span></span>
```
PS C:\>Set-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="0eebc-109">이 명령은 ID OICProvicer01 인 공급자를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eebc-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="0eebc-110">명령은 공급자에 대 한 클라이언트 비밀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eebc-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="0eebc-111">변수</span><span class="sxs-lookup"><span data-stu-id="0eebc-111">PARAMETERS</span></span>

### <span data-ttu-id="0eebc-112">-ClientId</span><span class="sxs-lookup"><span data-stu-id="0eebc-112">-ClientId</span></span>
<span data-ttu-id="0eebc-113">개발자 콘솔의 클라이언트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eebc-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="0eebc-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="0eebc-114">-ClientSecret</span></span>
<span data-ttu-id="0eebc-115">개발자 콘솔의 클라이언트 비밀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eebc-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="0eebc-116">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="0eebc-116">-Context</span></span>
<span data-ttu-id="0eebc-117">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eebc-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0eebc-118">-설명</span><span class="sxs-lookup"><span data-stu-id="0eebc-118">-Description</span></span>
<span data-ttu-id="0eebc-119">설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eebc-119">Specifies a description.</span></span>

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

### <span data-ttu-id="0eebc-120">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="0eebc-120">-MetadataEndpointUri</span></span>
<span data-ttu-id="0eebc-121">공급자의 메타 데이터 끝점 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eebc-121">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="0eebc-122">-이름</span><span class="sxs-lookup"><span data-stu-id="0eebc-122">-Name</span></span>
<span data-ttu-id="0eebc-123">공급자에 대 한 친숙 한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eebc-123">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="0eebc-124">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="0eebc-124">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="0eebc-125">이 cmdlet이 수정 하는 공급자에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eebc-125">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="0eebc-126">ID를 지정 하지 않으면이 cmdlet이 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eebc-126">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="0eebc-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0eebc-127">-PassThru</span></span>
<span data-ttu-id="0eebc-128">이 cmdlet이이 cmdlet이 수정 하는 **PsApiManagementOpenIdConnectProvider** 를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0eebc-128">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0eebc-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eebc-129">-DefaultProfile</span></span>
<span data-ttu-id="0eebc-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0eebc-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eebc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eebc-131">CommonParameters</span></span>
<span data-ttu-id="0eebc-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eebc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eebc-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0eebc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eebc-134">입력</span><span class="sxs-lookup"><span data-stu-id="0eebc-134">INPUTS</span></span>

## <span data-ttu-id="0eebc-135">출력</span><span class="sxs-lookup"><span data-stu-id="0eebc-135">OUTPUTS</span></span>

### <span data-ttu-id="0eebc-136">ApiManagement. ServiceManagement. \ PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0eebc-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="0eebc-137">상속자</span><span class="sxs-lookup"><span data-stu-id="0eebc-137">NOTES</span></span>

## <span data-ttu-id="0eebc-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0eebc-138">RELATED LINKS</span></span>

[<span data-ttu-id="0eebc-139">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0eebc-139">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="0eebc-140">새로운 AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0eebc-140">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="0eebc-141">제거-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0eebc-141">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)


