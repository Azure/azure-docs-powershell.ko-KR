---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: c914c49aeb4f2a763a09c5b513bcbe7809110b05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536843"
---
# <span data-ttu-id="16c80-101">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="16c80-101">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="16c80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16c80-102">SYNOPSIS</span></span>
<span data-ttu-id="16c80-103">OpenID Connect provider를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c80-103">Modifies an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16c80-104">구문과</span><span class="sxs-lookup"><span data-stu-id="16c80-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>]
 [-ClientSecret <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16c80-105">설명은</span><span class="sxs-lookup"><span data-stu-id="16c80-105">DESCRIPTION</span></span>
<span data-ttu-id="16c80-106">**Set-AzureRmApiManagementOpenIdConnectProvider** Cmdlet은 Azure API Management의 OpenID Connect 공급자를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c80-106">The **Set-AzureRmApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="16c80-107">예제의</span><span class="sxs-lookup"><span data-stu-id="16c80-107">EXAMPLES</span></span>

### <span data-ttu-id="16c80-108">예제 1: 공급자에 대 한 클라이언트 비밀 변경</span><span class="sxs-lookup"><span data-stu-id="16c80-108">Example 1: Change the client secret for a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="16c80-109">이 명령은 ID OICProvicer01 인 공급자를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c80-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="16c80-110">명령은 공급자에 대 한 클라이언트 비밀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c80-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="16c80-111">변수</span><span class="sxs-lookup"><span data-stu-id="16c80-111">PARAMETERS</span></span>

### <span data-ttu-id="16c80-112">-ClientId</span><span class="sxs-lookup"><span data-stu-id="16c80-112">-ClientId</span></span>
<span data-ttu-id="16c80-113">개발자 콘솔의 클라이언트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c80-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="16c80-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="16c80-114">-ClientSecret</span></span>
<span data-ttu-id="16c80-115">개발자 콘솔의 클라이언트 비밀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c80-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="16c80-116">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="16c80-116">-Context</span></span>
<span data-ttu-id="16c80-117">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c80-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="16c80-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16c80-118">-DefaultProfile</span></span>
<span data-ttu-id="16c80-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16c80-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="16c80-120">-설명</span><span class="sxs-lookup"><span data-stu-id="16c80-120">-Description</span></span>
<span data-ttu-id="16c80-121">설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c80-121">Specifies a description.</span></span>

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

### <span data-ttu-id="16c80-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="16c80-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="16c80-123">공급자의 메타 데이터 끝점 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c80-123">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="16c80-124">-이름</span><span class="sxs-lookup"><span data-stu-id="16c80-124">-Name</span></span>
<span data-ttu-id="16c80-125">공급자에 대 한 친숙 한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c80-125">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="16c80-126">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="16c80-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="16c80-127">이 cmdlet이 수정 하는 공급자에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c80-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="16c80-128">ID를 지정 하지 않으면이 cmdlet이 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c80-128">If you do not specify an ID, this cmdlet generates one.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16c80-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16c80-129">-PassThru</span></span>
<span data-ttu-id="16c80-130">이 cmdlet이이 cmdlet이 수정 하는 **PsApiManagementOpenIdConnectProvider** 를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="16c80-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="16c80-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c80-131">CommonParameters</span></span>
<span data-ttu-id="16c80-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c80-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c80-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16c80-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c80-134">입력</span><span class="sxs-lookup"><span data-stu-id="16c80-134">INPUTS</span></span>

### <span data-ttu-id="16c80-135">않아야</span><span class="sxs-lookup"><span data-stu-id="16c80-135">None</span></span>
<span data-ttu-id="16c80-136">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16c80-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="16c80-137">출력</span><span class="sxs-lookup"><span data-stu-id="16c80-137">OUTPUTS</span></span>

### <span data-ttu-id="16c80-138">ApiManagement. ServiceManagement. \ PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="16c80-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="16c80-139">상속자</span><span class="sxs-lookup"><span data-stu-id="16c80-139">NOTES</span></span>

## <span data-ttu-id="16c80-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16c80-140">RELATED LINKS</span></span>

[<span data-ttu-id="16c80-141">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="16c80-141">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="16c80-142">새로운 AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="16c80-142">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="16c80-143">제거-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="16c80-143">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)


