---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 651ef4c0c44b7e3269eb300dcfa098c39415f77d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703288"
---
# <span data-ttu-id="8be41-101">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="8be41-101">Get-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="8be41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8be41-102">SYNOPSIS</span></span>
<span data-ttu-id="8be41-103">API 관리 권한 부여 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8be41-103">Gets an API Management authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8be41-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8be41-104">SYNTAX</span></span>

### <span data-ttu-id="8be41-105">GetAllAuthorizationServers (기본값)</span><span class="sxs-lookup"><span data-stu-id="8be41-105">GetAllAuthorizationServers (Default)</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8be41-106">GetByServerId</span><span class="sxs-lookup"><span data-stu-id="8be41-106">GetByServerId</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8be41-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8be41-107">DESCRIPTION</span></span>
<span data-ttu-id="8be41-108">**AzureRmApiManagementAuthorizationServer** cmdlet은 모든 Azure API Management 권한 부여 서버 또는 지정 된 권한 부여 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8be41-108">The **Get-AzureRmApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="8be41-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8be41-109">EXAMPLES</span></span>

### <span data-ttu-id="8be41-110">예제 1: 모든 권한 부여 서버 가져오기</span><span class="sxs-lookup"><span data-stu-id="8be41-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext
```

<span data-ttu-id="8be41-111">이 명령은 모든 API Management 권한 부여 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8be41-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="8be41-112">예제 2: 지정 된 권한 부여 서버 가져오기</span><span class="sxs-lookup"><span data-stu-id="8be41-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="8be41-113">이 명령은 지정 된 권한 부여 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8be41-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="8be41-114">변수</span><span class="sxs-lookup"><span data-stu-id="8be41-114">PARAMETERS</span></span>

### <span data-ttu-id="8be41-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="8be41-115">-Context</span></span>
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

### <span data-ttu-id="8be41-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8be41-116">-DefaultProfile</span></span>
<span data-ttu-id="8be41-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8be41-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="8be41-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="8be41-118">-ServerId</span></span>
```yaml
Type: String
Parameter Sets: GetByServerId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8be41-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8be41-119">CommonParameters</span></span>
<span data-ttu-id="8be41-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8be41-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8be41-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8be41-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8be41-122">입력</span><span class="sxs-lookup"><span data-stu-id="8be41-122">INPUTS</span></span>

### <span data-ttu-id="8be41-123">않아야</span><span class="sxs-lookup"><span data-stu-id="8be41-123">None</span></span>
<span data-ttu-id="8be41-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8be41-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8be41-125">출력</span><span class="sxs-lookup"><span data-stu-id="8be41-125">OUTPUTS</span></span>

### <span data-ttu-id="8be41-126">ApiManagement. ServiceManagement. \ PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="8be41-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>
<span data-ttu-id="8be41-127">지정 된 Api Management 서비스의 인증 서버에 대 한 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="8be41-127">The details of the Authorization Server in a given Api Management service.</span></span>

### <span data-ttu-id="8be41-128">IList를<ApiManagement> ServiceManagement. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="8be41-128">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer></span></span>
<span data-ttu-id="8be41-129">지정 된 Api Management 서비스의 권한 부여 서버 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="8be41-129">The list of Authorization Server in a given Api Management service.</span></span>

## <span data-ttu-id="8be41-130">상속자</span><span class="sxs-lookup"><span data-stu-id="8be41-130">NOTES</span></span>

## <span data-ttu-id="8be41-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8be41-131">RELATED LINKS</span></span>

[<span data-ttu-id="8be41-132">새로운 AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="8be41-132">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="8be41-133">제거-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="8be41-133">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="8be41-134">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="8be41-134">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


