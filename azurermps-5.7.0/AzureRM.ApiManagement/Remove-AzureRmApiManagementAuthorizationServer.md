---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: c9133c7a2924b4151afd01f257fe6b54a9eeb00d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536863"
---
# <span data-ttu-id="10ac4-101">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="10ac4-101">Remove-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="10ac4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10ac4-102">SYNOPSIS</span></span>
<span data-ttu-id="10ac4-103">권한 부여 서버를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="10ac4-103">Removes an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10ac4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="10ac4-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10ac4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="10ac4-105">DESCRIPTION</span></span>
<span data-ttu-id="10ac4-106">**AzureRmApiManagementAuthorizationServer** Cmdlet은 Azure API Management 권한 부여 서버를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="10ac4-106">The **Remove-AzureRmApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="10ac4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="10ac4-107">EXAMPLES</span></span>

## <span data-ttu-id="10ac4-108">변수</span><span class="sxs-lookup"><span data-stu-id="10ac4-108">PARAMETERS</span></span>

### <span data-ttu-id="10ac4-109">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="10ac4-109">-Context</span></span>
<span data-ttu-id="10ac4-110">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10ac4-110">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="10ac4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10ac4-111">-DefaultProfile</span></span>
<span data-ttu-id="10ac4-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="10ac4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="10ac4-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10ac4-113">-PassThru</span></span>
<span data-ttu-id="10ac4-114">passthru</span><span class="sxs-lookup"><span data-stu-id="10ac4-114">passthru</span></span>

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

### <span data-ttu-id="10ac4-115">-ServerId</span><span class="sxs-lookup"><span data-stu-id="10ac4-115">-ServerId</span></span>
<span data-ttu-id="10ac4-116">제거할 인증 서버의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10ac4-116">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="10ac4-117">-확인</span><span class="sxs-lookup"><span data-stu-id="10ac4-117">-Confirm</span></span>
<span data-ttu-id="10ac4-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="10ac4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10ac4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10ac4-119">-WhatIf</span></span>
<span data-ttu-id="10ac4-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="10ac4-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10ac4-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10ac4-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10ac4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10ac4-122">CommonParameters</span></span>
<span data-ttu-id="10ac4-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="10ac4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10ac4-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10ac4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10ac4-125">입력</span><span class="sxs-lookup"><span data-stu-id="10ac4-125">INPUTS</span></span>

### <span data-ttu-id="10ac4-126">않아야</span><span class="sxs-lookup"><span data-stu-id="10ac4-126">None</span></span>
<span data-ttu-id="10ac4-127">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10ac4-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="10ac4-128">출력</span><span class="sxs-lookup"><span data-stu-id="10ac4-128">OUTPUTS</span></span>

### <span data-ttu-id="10ac4-129">나타내는</span><span class="sxs-lookup"><span data-stu-id="10ac4-129">Boolean</span></span>

## <span data-ttu-id="10ac4-130">상속자</span><span class="sxs-lookup"><span data-stu-id="10ac4-130">NOTES</span></span>

## <span data-ttu-id="10ac4-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10ac4-131">RELATED LINKS</span></span>

[<span data-ttu-id="10ac4-132">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="10ac4-132">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="10ac4-133">새로운 AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="10ac4-133">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="10ac4-134">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="10ac4-134">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


