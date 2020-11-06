---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
ms.openlocfilehash: 4453b7fc3e13f4de2632c41cea966fdada1d84f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536868"
---
# <span data-ttu-id="71958-101">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="71958-101">New-AzureRmApiManagementBackendCredential</span></span>

## <span data-ttu-id="71958-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71958-102">SYNOPSIS</span></span>
<span data-ttu-id="71958-103">새 백엔드 자격 증명 계약을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="71958-103">Creates a new Backend Credential contract.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71958-104">구문과</span><span class="sxs-lookup"><span data-stu-id="71958-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71958-105">설명은</span><span class="sxs-lookup"><span data-stu-id="71958-105">DESCRIPTION</span></span>
<span data-ttu-id="71958-106">새 백엔드 자격 증명 계약을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="71958-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="71958-107">예제의</span><span class="sxs-lookup"><span data-stu-id="71958-107">EXAMPLES</span></span>

### <span data-ttu-id="71958-108">백 엔드 자격 증명 In-Memory 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="71958-108">Create a Backend Credentials In-Memory Object</span></span>
```
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}
```

<span data-ttu-id="71958-109">백 엔드 자격 증명 계약 만들기</span><span class="sxs-lookup"><span data-stu-id="71958-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="71958-110">변수</span><span class="sxs-lookup"><span data-stu-id="71958-110">PARAMETERS</span></span>

### <span data-ttu-id="71958-111">-AuthorizationHeaderParameter 변수</span><span class="sxs-lookup"><span data-stu-id="71958-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="71958-112">백 엔드에 사용 되는 권한 부여 헤더입니다.</span><span class="sxs-lookup"><span data-stu-id="71958-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="71958-113">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="71958-113">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71958-114">-Authorization헤더 구성표</span><span class="sxs-lookup"><span data-stu-id="71958-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="71958-115">백 엔드에 사용 되는 권한 부여 체계입니다.</span><span class="sxs-lookup"><span data-stu-id="71958-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="71958-116">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="71958-116">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71958-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="71958-117">-CertificateThumbprint</span></span>
<span data-ttu-id="71958-118">클라이언트 인증서 지문.</span><span class="sxs-lookup"><span data-stu-id="71958-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="71958-119">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="71958-119">This parameter is optional.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71958-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71958-120">-DefaultProfile</span></span>
<span data-ttu-id="71958-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="71958-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="71958-122">-헤더</span><span class="sxs-lookup"><span data-stu-id="71958-122">-Header</span></span>
<span data-ttu-id="71958-123">백 엔드가 허용 하는 헤더 매개 변수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="71958-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="71958-124">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="71958-124">This parameter is optional.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71958-125">-쿼리</span><span class="sxs-lookup"><span data-stu-id="71958-125">-Query</span></span>
<span data-ttu-id="71958-126">백 엔드에 의해 허용 된 쿼리 매개 변수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="71958-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="71958-127">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="71958-127">This parameter is optional.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71958-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71958-128">CommonParameters</span></span>
<span data-ttu-id="71958-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="71958-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71958-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71958-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71958-131">입력</span><span class="sxs-lookup"><span data-stu-id="71958-131">INPUTS</span></span>

### <span data-ttu-id="71958-132">않아야</span><span class="sxs-lookup"><span data-stu-id="71958-132">None</span></span>
<span data-ttu-id="71958-133">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71958-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="71958-134">출력</span><span class="sxs-lookup"><span data-stu-id="71958-134">OUTPUTS</span></span>

### <span data-ttu-id="71958-135">ApiManagement. ServiceManagement. \ PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="71958-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="71958-136">상속자</span><span class="sxs-lookup"><span data-stu-id="71958-136">NOTES</span></span>

## <span data-ttu-id="71958-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71958-137">RELATED LINKS</span></span>

[<span data-ttu-id="71958-138">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="71958-138">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="71958-139">새로운 AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="71958-139">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="71958-140">새로운 AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="71958-140">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="71958-141">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="71958-141">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="71958-142">제거-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="71958-142">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
