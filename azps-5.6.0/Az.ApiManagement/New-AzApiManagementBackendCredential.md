---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: 0d865e2b9e1459f326367a499e30bc37467628cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966859"
---
# <span data-ttu-id="733e5-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="733e5-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="733e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="733e5-102">SYNOPSIS</span></span>
<span data-ttu-id="733e5-103">새 백end 자격 증명 계약을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="733e5-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="733e5-104">구문</span><span class="sxs-lookup"><span data-stu-id="733e5-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="733e5-105">설명</span><span class="sxs-lookup"><span data-stu-id="733e5-105">DESCRIPTION</span></span>
<span data-ttu-id="733e5-106">새 백end 자격 증명 계약을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="733e5-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="733e5-107">예제</span><span class="sxs-lookup"><span data-stu-id="733e5-107">EXAMPLES</span></span>

### <span data-ttu-id="733e5-108">예제 1: 백end 자격 증명 만들기 In-Memory 개체</span><span class="sxs-lookup"><span data-stu-id="733e5-108">Example 1: Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="733e5-109">백end 자격 증명 계약을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="733e5-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="733e5-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="733e5-110">PARAMETERS</span></span>

### <span data-ttu-id="733e5-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="733e5-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="733e5-112">백end에 사용되는 권한 부여 헤더입니다.</span><span class="sxs-lookup"><span data-stu-id="733e5-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="733e5-113">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="733e5-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="733e5-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="733e5-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="733e5-115">백end에 사용되는 권한 부여 체계입니다.</span><span class="sxs-lookup"><span data-stu-id="733e5-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="733e5-116">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="733e5-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="733e5-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="733e5-117">-CertificateThumbprint</span></span>
<span data-ttu-id="733e5-118">클라이언트 인증서 지문입니다.</span><span class="sxs-lookup"><span data-stu-id="733e5-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="733e5-119">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="733e5-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="733e5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="733e5-120">-DefaultProfile</span></span>
<span data-ttu-id="733e5-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="733e5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="733e5-122">-헤더</span><span class="sxs-lookup"><span data-stu-id="733e5-122">-Header</span></span>
<span data-ttu-id="733e5-123">백end에서 허용하는 헤더 매개 변수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="733e5-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="733e5-124">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="733e5-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="733e5-125">-쿼리</span><span class="sxs-lookup"><span data-stu-id="733e5-125">-Query</span></span>
<span data-ttu-id="733e5-126">백end에서 허용하는 쿼리 매개 변수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="733e5-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="733e5-127">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="733e5-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="733e5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="733e5-128">CommonParameters</span></span>
<span data-ttu-id="733e5-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="733e5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="733e5-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="733e5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="733e5-131">입력</span><span class="sxs-lookup"><span data-stu-id="733e5-131">INPUTS</span></span>

### <span data-ttu-id="733e5-132">없음</span><span class="sxs-lookup"><span data-stu-id="733e5-132">None</span></span>

## <span data-ttu-id="733e5-133">출력</span><span class="sxs-lookup"><span data-stu-id="733e5-133">OUTPUTS</span></span>

### <span data-ttu-id="733e5-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.psApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="733e5-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="733e5-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="733e5-135">NOTES</span></span>

## <span data-ttu-id="733e5-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="733e5-136">RELATED LINKS</span></span>

[<span data-ttu-id="733e5-137">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="733e5-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="733e5-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="733e5-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="733e5-139">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="733e5-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="733e5-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="733e5-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="733e5-141">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="733e5-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
