---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: ea18df702913cd2ec7404a3fccb110f85e12ee47
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210368"
---
# <span data-ttu-id="38329-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="38329-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="38329-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38329-102">SYNOPSIS</span></span>
<span data-ttu-id="38329-103">PsApiManagementSslSetting의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="38329-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="38329-104">구문</span><span class="sxs-lookup"><span data-stu-id="38329-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38329-105">설명</span><span class="sxs-lookup"><span data-stu-id="38329-105">DESCRIPTION</span></span>
<span data-ttu-id="38329-106">PsApiManagementSslSetting의 인스턴스를 만드는 도우미 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="38329-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="38329-107">이 명령은 New-AzApiManagement 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="38329-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="38329-108">예제</span><span class="sxs-lookup"><span data-stu-id="38329-108">EXAMPLES</span></span>

### <span data-ttu-id="38329-109">예제 1: 백 엔드 및 프런트 엔드 모두에서 TLS 1.0을 사용하도록 설정하는 SSL 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="38329-109">Example 1: Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="38329-110">PsApiManagementSslSetting의 새 인스턴스를 만들어 ApiManagement 게이트웨이의 프런트 엔드(클라이언트와 APIM 간) 및 백 엔드(APIM과 백 엔드 간)에서 TLSv 1.0을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="38329-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="38329-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38329-111">PARAMETERS</span></span>

### <span data-ttu-id="38329-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="38329-112">-BackendProtocol</span></span>
<span data-ttu-id="38329-113">백end 보안 프로토콜 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="38329-113">Backend Security protocol settings.</span></span> <span data-ttu-id="38329-114">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="38329-114">This parameter is optional.</span></span>
<span data-ttu-id="38329-115">유효한 프로토콜 설정은 `Tls11` Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0입니다.</span><span class="sxs-lookup"><span data-stu-id="38329-115">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>

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

### <span data-ttu-id="38329-116">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="38329-116">-CipherSuite</span></span>
<span data-ttu-id="38329-117">Ssl 암호 모음 설정은 지정된 순서로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="38329-117">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="38329-118">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="38329-118">This parameter is optional.</span></span>
<span data-ttu-id="38329-119">유효한 `TripleDes168` 설정은 - Tripe Des 168 사용/사용 안 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="38329-119">The valid Settings are `TripleDes168` - Enable / Disable Tripe Des 168</span></span>

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

### <span data-ttu-id="38329-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38329-120">-DefaultProfile</span></span>
<span data-ttu-id="38329-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="38329-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38329-122">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="38329-122">-FrontendProtocol</span></span>
<span data-ttu-id="38329-123">프런트 엔드 보안 프로토콜 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="38329-123">Frontend Security protocols settings.</span></span> <span data-ttu-id="38329-124">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="38329-124">This parameter is optional.</span></span>
<span data-ttu-id="38329-125">유효한 프로토콜 설정은 `Tls11` Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0입니다.</span><span class="sxs-lookup"><span data-stu-id="38329-125">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>


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

### <span data-ttu-id="38329-126">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="38329-126">-ServerProtocol</span></span>
<span data-ttu-id="38329-127">Http2와 같은 서버 프로토콜 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="38329-127">Server protocol settings like Http2.</span></span> <span data-ttu-id="38329-128">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="38329-128">This parameter is optional.</span></span>
<span data-ttu-id="38329-129">유효한 설정은 `Http2` Http 2.0 사용입니다.</span><span class="sxs-lookup"><span data-stu-id="38329-129">The valid Settings are `Http2` - Enable Http 2.0</span></span>

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

### <span data-ttu-id="38329-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38329-130">CommonParameters</span></span>
<span data-ttu-id="38329-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="38329-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38329-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="38329-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38329-133">입력</span><span class="sxs-lookup"><span data-stu-id="38329-133">INPUTS</span></span>

### <span data-ttu-id="38329-134">없음</span><span class="sxs-lookup"><span data-stu-id="38329-134">None</span></span>

## <span data-ttu-id="38329-135">출력</span><span class="sxs-lookup"><span data-stu-id="38329-135">OUTPUTS</span></span>

### <span data-ttu-id="38329-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="38329-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="38329-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="38329-137">NOTES</span></span>

## <span data-ttu-id="38329-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="38329-138">RELATED LINKS</span></span>

[<span data-ttu-id="38329-139">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="38329-139">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

