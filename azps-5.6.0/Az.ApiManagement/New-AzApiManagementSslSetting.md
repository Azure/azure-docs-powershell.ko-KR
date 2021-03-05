---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: c1bdb71dcfbc554d8d9ca1d7d09a80053a564402
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001995"
---
# <span data-ttu-id="14dd2-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="14dd2-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="14dd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14dd2-102">SYNOPSIS</span></span>
<span data-ttu-id="14dd2-103">PsApiManagementSslSetting의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="14dd2-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="14dd2-104">구문</span><span class="sxs-lookup"><span data-stu-id="14dd2-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="14dd2-105">설명</span><span class="sxs-lookup"><span data-stu-id="14dd2-105">DESCRIPTION</span></span>
<span data-ttu-id="14dd2-106">PsApiManagementSslSetting의 인스턴스를 만드는 도우미 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="14dd2-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="14dd2-107">이 명령은 명령과 함께 New-AzApiManagement 합니다.</span><span class="sxs-lookup"><span data-stu-id="14dd2-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="14dd2-108">예제</span><span class="sxs-lookup"><span data-stu-id="14dd2-108">EXAMPLES</span></span>

### <span data-ttu-id="14dd2-109">예제 1: 백 엔드와 프런트 엔드 모두에서 TLS 1.0을 사용하도록 설정하는 SSL 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="14dd2-109">Example 1: Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="14dd2-110">ApiManagement Gateway의 프런트 엔드(클라이언트와 APIM 사이)와 백 엔드(APIM과 백 엔드 사이)에서 TLSv 1.0을 사용하도록 설정하는 PsApiManagementSslSetting의 새 인스턴스를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="14dd2-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="14dd2-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="14dd2-111">PARAMETERS</span></span>

### <span data-ttu-id="14dd2-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="14dd2-112">-BackendProtocol</span></span>
<span data-ttu-id="14dd2-113">백end 보안 프로토콜 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="14dd2-113">Backend Security protocol settings.</span></span> <span data-ttu-id="14dd2-114">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="14dd2-114">This parameter is optional.</span></span>
<span data-ttu-id="14dd2-115">유효한 프로토콜 설정은 `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="14dd2-115">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>

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

### <span data-ttu-id="14dd2-116">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="14dd2-116">-CipherSuite</span></span>
<span data-ttu-id="14dd2-117">Ssl 암호 제품군 설정은 지정된 순서로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="14dd2-117">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="14dd2-118">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="14dd2-118">This parameter is optional.</span></span>
<span data-ttu-id="14dd2-119">유효한 `TripleDes168` 설정은 - Tripe Des 168 사용/비활성화</span><span class="sxs-lookup"><span data-stu-id="14dd2-119">The valid Settings are `TripleDes168` - Enable / Disable Tripe Des 168</span></span>

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

### <span data-ttu-id="14dd2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14dd2-120">-DefaultProfile</span></span>
<span data-ttu-id="14dd2-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14dd2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14dd2-122">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="14dd2-122">-FrontendProtocol</span></span>
<span data-ttu-id="14dd2-123">Frontend Security 프로토콜 설정.</span><span class="sxs-lookup"><span data-stu-id="14dd2-123">Frontend Security protocols settings.</span></span> <span data-ttu-id="14dd2-124">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="14dd2-124">This parameter is optional.</span></span>
<span data-ttu-id="14dd2-125">유효한 프로토콜 설정은 `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="14dd2-125">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>


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

### <span data-ttu-id="14dd2-126">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="14dd2-126">-ServerProtocol</span></span>
<span data-ttu-id="14dd2-127">Http2와 같은 서버 프로토콜 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="14dd2-127">Server protocol settings like Http2.</span></span> <span data-ttu-id="14dd2-128">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="14dd2-128">This parameter is optional.</span></span>
<span data-ttu-id="14dd2-129">유효한 `Http2` 설정은 - Http 2.0 사용</span><span class="sxs-lookup"><span data-stu-id="14dd2-129">The valid Settings are `Http2` - Enable Http 2.0</span></span>

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

### <span data-ttu-id="14dd2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14dd2-130">CommonParameters</span></span>
<span data-ttu-id="14dd2-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="14dd2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14dd2-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14dd2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14dd2-133">입력</span><span class="sxs-lookup"><span data-stu-id="14dd2-133">INPUTS</span></span>

### <span data-ttu-id="14dd2-134">없음</span><span class="sxs-lookup"><span data-stu-id="14dd2-134">None</span></span>

## <span data-ttu-id="14dd2-135">출력</span><span class="sxs-lookup"><span data-stu-id="14dd2-135">OUTPUTS</span></span>

### <span data-ttu-id="14dd2-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="14dd2-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="14dd2-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="14dd2-137">NOTES</span></span>

## <span data-ttu-id="14dd2-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14dd2-138">RELATED LINKS</span></span>

[<span data-ttu-id="14dd2-139">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="14dd2-139">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

