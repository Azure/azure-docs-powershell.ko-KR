---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: 7c4fb7c2147d7daf3307c2895893198ebe805ff0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698023"
---
# <span data-ttu-id="83f96-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="83f96-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="83f96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83f96-102">SYNOPSIS</span></span>
<span data-ttu-id="83f96-103">PsApiManagementSslSetting의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="83f96-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="83f96-104">구문과</span><span class="sxs-lookup"><span data-stu-id="83f96-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="83f96-105">설명은</span><span class="sxs-lookup"><span data-stu-id="83f96-105">DESCRIPTION</span></span>
<span data-ttu-id="83f96-106">PsApiManagementSslSetting의 인스턴스를 만드는 도우미 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="83f96-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="83f96-107">이 명령은 New-AzApiManagement 명령에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="83f96-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="83f96-108">예제의</span><span class="sxs-lookup"><span data-stu-id="83f96-108">EXAMPLES</span></span>

### <span data-ttu-id="83f96-109">예제 1: 백 엔드 및 프런트 엔드에서 모두 TLS 1.0을 사용 하도록 설정 하는 SSL 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="83f96-109">Example 1 : Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="83f96-110">PsApiManagementSslSetting의 새 인스턴스를 만들어 ApiManagement 게이트웨이에서 두 프런트 엔드 (클라이언트와 APIM) 및 백 엔드 (APIM 및 백 엔드 사이)에 TLSv 1.0를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83f96-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="83f96-111">변수</span><span class="sxs-lookup"><span data-stu-id="83f96-111">PARAMETERS</span></span>

### <span data-ttu-id="83f96-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="83f96-112">-BackendProtocol</span></span>
<span data-ttu-id="83f96-113">백 엔드 보안 프로토콜 설정</span><span class="sxs-lookup"><span data-stu-id="83f96-113">Backend Security protocol settings.</span></span> <span data-ttu-id="83f96-114">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="83f96-114">This parameter is optional.</span></span>

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

### <span data-ttu-id="83f96-115">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="83f96-115">-CipherSuite</span></span>
<span data-ttu-id="83f96-116">지정 된 순서의 Ssl 암호 그룹 설정</span><span class="sxs-lookup"><span data-stu-id="83f96-116">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="83f96-117">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="83f96-117">This parameter is optional.</span></span>

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

### <span data-ttu-id="83f96-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83f96-118">-DefaultProfile</span></span>
<span data-ttu-id="83f96-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="83f96-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83f96-120">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="83f96-120">-FrontendProtocol</span></span>
<span data-ttu-id="83f96-121">프런트 엔드 보안 프로토콜 설정</span><span class="sxs-lookup"><span data-stu-id="83f96-121">Frontend Security protocols settings.</span></span> <span data-ttu-id="83f96-122">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="83f96-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="83f96-123">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="83f96-123">-ServerProtocol</span></span>
<span data-ttu-id="83f96-124">Http2 같은 서버 프로토콜 설정</span><span class="sxs-lookup"><span data-stu-id="83f96-124">Server protocol settings like Http2.</span></span> <span data-ttu-id="83f96-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="83f96-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="83f96-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83f96-126">CommonParameters</span></span>
<span data-ttu-id="83f96-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="83f96-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83f96-128">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="83f96-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83f96-129">입력</span><span class="sxs-lookup"><span data-stu-id="83f96-129">INPUTS</span></span>

### <span data-ttu-id="83f96-130">않아야</span><span class="sxs-lookup"><span data-stu-id="83f96-130">None</span></span>

## <span data-ttu-id="83f96-131">출력</span><span class="sxs-lookup"><span data-stu-id="83f96-131">OUTPUTS</span></span>

### <span data-ttu-id="83f96-132">ApiManagement. PsApiManagementSslSettings/.</span><span class="sxs-lookup"><span data-stu-id="83f96-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="83f96-133">상속자</span><span class="sxs-lookup"><span data-stu-id="83f96-133">NOTES</span></span>

## <span data-ttu-id="83f96-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83f96-134">RELATED LINKS</span></span>

[<span data-ttu-id="83f96-135">새로운 AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="83f96-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

