---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 2e18be1721f68a0e1223bf45b9ca2e637c05a378
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531515"
---
# <span data-ttu-id="76953-101">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="76953-101">Get-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="76953-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76953-102">SYNOPSIS</span></span>
<span data-ttu-id="76953-103">API 관리 권한 부여 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76953-103">Gets an API Management authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76953-104">구문과</span><span class="sxs-lookup"><span data-stu-id="76953-104">SYNTAX</span></span>

### <span data-ttu-id="76953-105">GetAllAuthorizationServers (기본값)</span><span class="sxs-lookup"><span data-stu-id="76953-105">GetAllAuthorizationServers (Default)</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76953-106">GetByServerId</span><span class="sxs-lookup"><span data-stu-id="76953-106">GetByServerId</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76953-107">설명은</span><span class="sxs-lookup"><span data-stu-id="76953-107">DESCRIPTION</span></span>
<span data-ttu-id="76953-108">**AzureRmApiManagementAuthorizationServer** cmdlet은 모든 Azure API Management 권한 부여 서버 또는 지정 된 권한 부여 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76953-108">The **Get-AzureRmApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="76953-109">예제의</span><span class="sxs-lookup"><span data-stu-id="76953-109">EXAMPLES</span></span>

### <span data-ttu-id="76953-110">예제 1: 모든 권한 부여 서버 가져오기</span><span class="sxs-lookup"><span data-stu-id="76953-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext
```

<span data-ttu-id="76953-111">이 명령은 모든 API Management 권한 부여 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76953-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="76953-112">예제 2: 지정 된 권한 부여 서버 가져오기</span><span class="sxs-lookup"><span data-stu-id="76953-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="76953-113">이 명령은 지정 된 권한 부여 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76953-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="76953-114">변수</span><span class="sxs-lookup"><span data-stu-id="76953-114">PARAMETERS</span></span>

### <span data-ttu-id="76953-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="76953-115">-Context</span></span>

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

### <span data-ttu-id="76953-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76953-116">-DefaultProfile</span></span>
<span data-ttu-id="76953-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="76953-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76953-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="76953-118">-ServerId</span></span>
```yaml
Type: System.String
Parameter Sets: GetByServerId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76953-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76953-119">CommonParameters</span></span>
<span data-ttu-id="76953-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="76953-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76953-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76953-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76953-122">입력</span><span class="sxs-lookup"><span data-stu-id="76953-122">INPUTS</span></span>

### <span data-ttu-id="76953-123">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="76953-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="76953-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="76953-124">System.String</span></span>

## <span data-ttu-id="76953-125">출력</span><span class="sxs-lookup"><span data-stu-id="76953-125">OUTPUTS</span></span>

### <span data-ttu-id="76953-126">ApiManagement. ServiceManagement. \ PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="76953-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="76953-127">상속자</span><span class="sxs-lookup"><span data-stu-id="76953-127">NOTES</span></span>

## <span data-ttu-id="76953-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="76953-128">RELATED LINKS</span></span>

[<span data-ttu-id="76953-129">새로운 AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="76953-129">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="76953-130">제거-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="76953-130">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="76953-131">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="76953-131">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


