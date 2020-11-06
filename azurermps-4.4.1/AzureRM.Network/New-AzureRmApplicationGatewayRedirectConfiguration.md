---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 7f3834e13ce6fb6c3e9a661fead09ffcfab78933
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534896"
---
# <span data-ttu-id="6eb38-101">New-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6eb38-101">New-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="6eb38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6eb38-102">SYNOPSIS</span></span>
<span data-ttu-id="6eb38-103">응용 프로그램 게이트웨이에 대 한 리디렉션 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6eb38-103">Creates a redirect configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6eb38-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6eb38-104">SYNTAX</span></span>

### <span data-ttu-id="6eb38-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6eb38-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6eb38-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6eb38-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6eb38-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="6eb38-107">SetByURL</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6eb38-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6eb38-108">DESCRIPTION</span></span>
<span data-ttu-id="6eb38-109">**AzureRmApplicationGatewayRedirectConfiguration Cmdlet은** 응용 프로그램 게이트웨이에 대 한 리디렉션 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6eb38-109">**The New-AzureRmApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="6eb38-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6eb38-110">EXAMPLES</span></span>

### <span data-ttu-id="6eb38-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6eb38-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="6eb38-112">이 명령은 Redirect01 이라는 리디렉션 구성을 만들고 그 결과를 $RedirectConfig 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb38-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="6eb38-113">변수</span><span class="sxs-lookup"><span data-stu-id="6eb38-113">PARAMETERS</span></span>

### <span data-ttu-id="6eb38-114">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="6eb38-114">-IncludePath</span></span>
<span data-ttu-id="6eb38-115">리디렉션된 url의 포함 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="6eb38-115">Include path in the redirected url.</span></span>
<span data-ttu-id="6eb38-116">기본값은 true입니다.</span><span class="sxs-lookup"><span data-stu-id="6eb38-116">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eb38-117">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="6eb38-117">-IncludeQueryString</span></span>
<span data-ttu-id="6eb38-118">리디렉션된 url에 쿼리 문자열을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb38-118">Include query string in the redirected url.</span></span>
<span data-ttu-id="6eb38-119">기본값은 true입니다.</span><span class="sxs-lookup"><span data-stu-id="6eb38-119">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eb38-120">-이름</span><span class="sxs-lookup"><span data-stu-id="6eb38-120">-Name</span></span>
<span data-ttu-id="6eb38-121">리디렉션 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6eb38-121">The name of the Redirect Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eb38-122">RedirectType</span><span class="sxs-lookup"><span data-stu-id="6eb38-122">-RedirectType</span></span>
<span data-ttu-id="6eb38-123">리디렉션 유형</span><span class="sxs-lookup"><span data-stu-id="6eb38-123">The type of redirect</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eb38-124">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="6eb38-124">-TargetListener</span></span>
<span data-ttu-id="6eb38-125">HTTPListener 요청을 다음으로 리디렉션합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb38-125">HTTPListener to redirect the request to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eb38-126">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="6eb38-126">-TargetListenerID</span></span>
<span data-ttu-id="6eb38-127">요청을 리디렉션할 수신기의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6eb38-127">ID of  listener to redirect the request to</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eb38-128">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="6eb38-128">-TargetUrl</span></span>
<span data-ttu-id="6eb38-129">대상 URL 리디렉션</span><span class="sxs-lookup"><span data-stu-id="6eb38-129">Target URL fo redirection</span></span>

```yaml
Type: System.String
Parameter Sets: SetByURL
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eb38-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eb38-130">-DefaultProfile</span></span>
<span data-ttu-id="6eb38-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6eb38-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6eb38-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eb38-132">CommonParameters</span></span>
<span data-ttu-id="6eb38-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb38-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eb38-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6eb38-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eb38-135">입력</span><span class="sxs-lookup"><span data-stu-id="6eb38-135">INPUTS</span></span>

### <span data-ttu-id="6eb38-136">않아야</span><span class="sxs-lookup"><span data-stu-id="6eb38-136">None</span></span>

## <span data-ttu-id="6eb38-137">출력</span><span class="sxs-lookup"><span data-stu-id="6eb38-137">OUTPUTS</span></span>

### <span data-ttu-id="6eb38-138">Microsoft. 네트워크. Psapplication게이트웨이 Redirectconfiguration</span><span class="sxs-lookup"><span data-stu-id="6eb38-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="6eb38-139">상속자</span><span class="sxs-lookup"><span data-stu-id="6eb38-139">NOTES</span></span>

## <span data-ttu-id="6eb38-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6eb38-140">RELATED LINKS</span></span>

