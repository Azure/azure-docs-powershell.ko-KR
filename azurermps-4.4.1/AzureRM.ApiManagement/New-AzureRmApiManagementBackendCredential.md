---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
ms.openlocfilehash: 58f80b6ff1742bfc6360844648d6ad18d12d8389
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531274"
---
# <span data-ttu-id="e95f0-101">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="e95f0-101">New-AzureRmApiManagementBackendCredential</span></span>

## <span data-ttu-id="e95f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e95f0-102">SYNOPSIS</span></span>
<span data-ttu-id="e95f0-103">새 백엔드 자격 증명 계약을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e95f0-103">Creates a new Backend Credential contract.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e95f0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e95f0-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e95f0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e95f0-105">DESCRIPTION</span></span>
<span data-ttu-id="e95f0-106">새 백엔드 자격 증명 계약을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e95f0-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="e95f0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e95f0-107">EXAMPLES</span></span>

### <span data-ttu-id="e95f0-108">백 엔드 자격 증명 In-Memory 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="e95f0-108">Create a Backend Credentials In-Memory Object</span></span>
```
$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}
```

<span data-ttu-id="e95f0-109">백 엔드 자격 증명 계약 만들기</span><span class="sxs-lookup"><span data-stu-id="e95f0-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="e95f0-110">변수</span><span class="sxs-lookup"><span data-stu-id="e95f0-110">PARAMETERS</span></span>

### <span data-ttu-id="e95f0-111">-AuthorizationHeaderParameter 변수</span><span class="sxs-lookup"><span data-stu-id="e95f0-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="e95f0-112">백 엔드에 사용 되는 권한 부여 헤더입니다.</span><span class="sxs-lookup"><span data-stu-id="e95f0-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="e95f0-113">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="e95f0-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e95f0-114">-Authorization헤더 구성표</span><span class="sxs-lookup"><span data-stu-id="e95f0-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="e95f0-115">백 엔드에 사용 되는 권한 부여 체계입니다.</span><span class="sxs-lookup"><span data-stu-id="e95f0-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="e95f0-116">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="e95f0-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e95f0-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="e95f0-117">-CertificateThumbprint</span></span>
<span data-ttu-id="e95f0-118">클라이언트 인증서 지문.</span><span class="sxs-lookup"><span data-stu-id="e95f0-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="e95f0-119">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="e95f0-119">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e95f0-120">-헤더</span><span class="sxs-lookup"><span data-stu-id="e95f0-120">-Header</span></span>
<span data-ttu-id="e95f0-121">백 엔드가 허용 하는 헤더 매개 변수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="e95f0-121">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="e95f0-122">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="e95f0-122">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e95f0-123">-쿼리</span><span class="sxs-lookup"><span data-stu-id="e95f0-123">-Query</span></span>
<span data-ttu-id="e95f0-124">백 엔드에 의해 허용 된 쿼리 매개 변수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="e95f0-124">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="e95f0-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="e95f0-125">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e95f0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e95f0-126">-DefaultProfile</span></span>
<span data-ttu-id="e95f0-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e95f0-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e95f0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e95f0-128">CommonParameters</span></span>
<span data-ttu-id="e95f0-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e95f0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e95f0-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e95f0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e95f0-131">입력</span><span class="sxs-lookup"><span data-stu-id="e95f0-131">INPUTS</span></span>

## <span data-ttu-id="e95f0-132">출력</span><span class="sxs-lookup"><span data-stu-id="e95f0-132">OUTPUTS</span></span>

### <span data-ttu-id="e95f0-133">ApiManagement. ServiceManagement. \ PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="e95f0-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="e95f0-134">상속자</span><span class="sxs-lookup"><span data-stu-id="e95f0-134">NOTES</span></span>

## <span data-ttu-id="e95f0-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e95f0-135">RELATED LINKS</span></span>

[<span data-ttu-id="e95f0-136">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e95f0-136">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="e95f0-137">새로운 AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e95f0-137">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="e95f0-138">새로운 AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="e95f0-138">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="e95f0-139">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e95f0-139">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="e95f0-140">제거-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e95f0-140">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
