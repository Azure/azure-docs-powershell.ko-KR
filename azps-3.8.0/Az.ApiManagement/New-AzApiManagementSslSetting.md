---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: 709e8483a5f21e3afc58add1046b5dae22bea7b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042209"
---
# <span data-ttu-id="c4914-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="c4914-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="c4914-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4914-102">SYNOPSIS</span></span>
<span data-ttu-id="c4914-103">PsApiManagementSslSetting의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c4914-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="c4914-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c4914-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4914-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c4914-105">DESCRIPTION</span></span>
<span data-ttu-id="c4914-106">PsApiManagementSslSetting의 인스턴스를 만드는 도우미 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="c4914-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="c4914-107">이 명령은 New-AzApiManagement 명령에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4914-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="c4914-108">예제의</span><span class="sxs-lookup"><span data-stu-id="c4914-108">EXAMPLES</span></span>

### <span data-ttu-id="c4914-109">예제 1: 백 엔드 및 프런트 엔드에서 모두 TLS 1.0을 사용 하도록 설정 하는 SSL 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="c4914-109">Example 1 : Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="c4914-110">PsApiManagementSslSetting의 새 인스턴스를 만들어 ApiManagement 게이트웨이에서 두 프런트 엔드 (클라이언트와 APIM) 및 백 엔드 (APIM 및 백 엔드 사이)에 TLSv 1.0를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4914-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="c4914-111">변수</span><span class="sxs-lookup"><span data-stu-id="c4914-111">PARAMETERS</span></span>

### <span data-ttu-id="c4914-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="c4914-112">-BackendProtocol</span></span>
<span data-ttu-id="c4914-113">백 엔드 보안 프로토콜 설정</span><span class="sxs-lookup"><span data-stu-id="c4914-113">Backend Security protocol settings.</span></span> <span data-ttu-id="c4914-114">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="c4914-114">This parameter is optional.</span></span>
<span data-ttu-id="c4914-115">유효한 프로토콜 설정은 `Tls11` -tls 1.1 `Tls10` -tls 1.0 `Ssl30` -SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="c4914-115">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>

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

### <span data-ttu-id="c4914-116">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="c4914-116">-CipherSuite</span></span>
<span data-ttu-id="c4914-117">지정 된 순서의 Ssl 암호 그룹 설정</span><span class="sxs-lookup"><span data-stu-id="c4914-117">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="c4914-118">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="c4914-118">This parameter is optional.</span></span>
<span data-ttu-id="c4914-119">유효한 설정은 `TripleDes168` Tripe Des 168에 대 한 사용 설정/해제</span><span class="sxs-lookup"><span data-stu-id="c4914-119">The valid Settings are `TripleDes168` - Enable / Disable Tripe Des 168</span></span>

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

### <span data-ttu-id="c4914-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4914-120">-DefaultProfile</span></span>
<span data-ttu-id="c4914-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c4914-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4914-122">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="c4914-122">-FrontendProtocol</span></span>
<span data-ttu-id="c4914-123">프런트 엔드 보안 프로토콜 설정</span><span class="sxs-lookup"><span data-stu-id="c4914-123">Frontend Security protocols settings.</span></span> <span data-ttu-id="c4914-124">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="c4914-124">This parameter is optional.</span></span>
<span data-ttu-id="c4914-125">유효한 프로토콜 설정은 `Tls11` -tls 1.1 `Tls10` -tls 1.0 `Ssl30` -SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="c4914-125">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>


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

### <span data-ttu-id="c4914-126">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="c4914-126">-ServerProtocol</span></span>
<span data-ttu-id="c4914-127">Http2 같은 서버 프로토콜 설정</span><span class="sxs-lookup"><span data-stu-id="c4914-127">Server protocol settings like Http2.</span></span> <span data-ttu-id="c4914-128">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="c4914-128">This parameter is optional.</span></span>
<span data-ttu-id="c4914-129">유효한 설정은 `Http2` -Enable Http 2.0입니다.</span><span class="sxs-lookup"><span data-stu-id="c4914-129">The valid Settings are `Http2` - Enable Http 2.0</span></span>

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

### <span data-ttu-id="c4914-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4914-130">CommonParameters</span></span>
<span data-ttu-id="c4914-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4914-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4914-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c4914-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4914-133">입력</span><span class="sxs-lookup"><span data-stu-id="c4914-133">INPUTS</span></span>

### <span data-ttu-id="c4914-134">않아야</span><span class="sxs-lookup"><span data-stu-id="c4914-134">None</span></span>

## <span data-ttu-id="c4914-135">출력</span><span class="sxs-lookup"><span data-stu-id="c4914-135">OUTPUTS</span></span>

### <span data-ttu-id="c4914-136">ApiManagement. PsApiManagementSslSettings/.</span><span class="sxs-lookup"><span data-stu-id="c4914-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="c4914-137">상속자</span><span class="sxs-lookup"><span data-stu-id="c4914-137">NOTES</span></span>

## <span data-ttu-id="c4914-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4914-138">RELATED LINKS</span></span>

[<span data-ttu-id="c4914-139">새로운 AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c4914-139">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

