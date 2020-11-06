---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: ee1ac7cda19f2b37ac1313d30075aa9c620bbd54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535359"
---
# <span data-ttu-id="af671-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="af671-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="af671-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af671-102">SYNOPSIS</span></span>
<span data-ttu-id="af671-103">OpenID Connect provider를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="af671-103">Removes an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af671-104">구문과</span><span class="sxs-lookup"><span data-stu-id="af671-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af671-105">설명은</span><span class="sxs-lookup"><span data-stu-id="af671-105">DESCRIPTION</span></span>
<span data-ttu-id="af671-106">**AzureRmApiManagementOpenIdConnectProvider** Cmdlet은 Azure API Management 용 OpenID Connect 공급자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="af671-106">The **Remove-AzureRmApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="af671-107">예제의</span><span class="sxs-lookup"><span data-stu-id="af671-107">EXAMPLES</span></span>

### <span data-ttu-id="af671-108">예제 1: 공급자 제거</span><span class="sxs-lookup"><span data-stu-id="af671-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -PassThru
```

<span data-ttu-id="af671-109">이 명령은 ID OICProvicer01 인 공급자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="af671-109">This command removes a provider that has the ID OICProvicer01.</span></span>

## <span data-ttu-id="af671-110">변수</span><span class="sxs-lookup"><span data-stu-id="af671-110">PARAMETERS</span></span>

### <span data-ttu-id="af671-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="af671-111">-Context</span></span>
<span data-ttu-id="af671-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af671-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="af671-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af671-113">-DefaultProfile</span></span>
<span data-ttu-id="af671-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="af671-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="af671-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="af671-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="af671-116">이 cmdlet이 제거 하는 공급자의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af671-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="af671-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af671-117">-PassThru</span></span>
<span data-ttu-id="af671-118">이 cmdlet이 작업이 성공한 경우 $True 값을 반환 하거나 다른 방법으로 $False 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="af671-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="af671-119">-확인</span><span class="sxs-lookup"><span data-stu-id="af671-119">-Confirm</span></span>
<span data-ttu-id="af671-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="af671-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af671-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af671-121">-WhatIf</span></span>
<span data-ttu-id="af671-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="af671-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af671-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af671-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af671-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af671-124">CommonParameters</span></span>
<span data-ttu-id="af671-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="af671-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af671-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af671-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af671-127">입력</span><span class="sxs-lookup"><span data-stu-id="af671-127">INPUTS</span></span>

### <span data-ttu-id="af671-128">않아야</span><span class="sxs-lookup"><span data-stu-id="af671-128">None</span></span>
<span data-ttu-id="af671-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af671-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="af671-130">출력</span><span class="sxs-lookup"><span data-stu-id="af671-130">OUTPUTS</span></span>

### <span data-ttu-id="af671-131">나타내는</span><span class="sxs-lookup"><span data-stu-id="af671-131">Boolean</span></span>

## <span data-ttu-id="af671-132">상속자</span><span class="sxs-lookup"><span data-stu-id="af671-132">NOTES</span></span>

## <span data-ttu-id="af671-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="af671-133">RELATED LINKS</span></span>

[<span data-ttu-id="af671-134">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="af671-134">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="af671-135">새로운 AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="af671-135">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="af671-136">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="af671-136">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


