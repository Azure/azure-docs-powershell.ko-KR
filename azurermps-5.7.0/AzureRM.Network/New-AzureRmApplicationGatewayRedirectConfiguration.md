---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 0d2d9d9390f60c7d7eb74061a52b9b437acdf772
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528051"
---
# <span data-ttu-id="f0c84-101">New-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0c84-101">New-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="f0c84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0c84-102">SYNOPSIS</span></span>
<span data-ttu-id="f0c84-103">응용 프로그램 게이트웨이에 대 한 리디렉션 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f0c84-103">Creates a redirect configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0c84-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f0c84-104">SYNTAX</span></span>

### <span data-ttu-id="f0c84-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f0c84-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0c84-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f0c84-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0c84-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="f0c84-107">SetByURL</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0c84-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f0c84-108">DESCRIPTION</span></span>
<span data-ttu-id="f0c84-109">**AzureRmApplicationGatewayRedirectConfiguration Cmdlet은** 응용 프로그램 게이트웨이에 대 한 리디렉션 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f0c84-109">**The New-AzureRmApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="f0c84-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f0c84-110">EXAMPLES</span></span>

### <span data-ttu-id="f0c84-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f0c84-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="f0c84-112">이 명령은 Redirect01 이라는 리디렉션 구성을 만들고 그 결과를 $RedirectConfig 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0c84-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="f0c84-113">변수</span><span class="sxs-lookup"><span data-stu-id="f0c84-113">PARAMETERS</span></span>

### <span data-ttu-id="f0c84-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0c84-114">-DefaultProfile</span></span>
<span data-ttu-id="f0c84-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f0c84-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0c84-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="f0c84-116">-IncludePath</span></span>
<span data-ttu-id="f0c84-117">리디렉션된 url의 포함 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="f0c84-117">Include path in the redirected url.</span></span>
<span data-ttu-id="f0c84-118">기본값은 true입니다.</span><span class="sxs-lookup"><span data-stu-id="f0c84-118">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c84-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="f0c84-119">-IncludeQueryString</span></span>
<span data-ttu-id="f0c84-120">리디렉션된 url에 쿼리 문자열을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0c84-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="f0c84-121">기본값은 true입니다.</span><span class="sxs-lookup"><span data-stu-id="f0c84-121">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c84-122">-이름</span><span class="sxs-lookup"><span data-stu-id="f0c84-122">-Name</span></span>
<span data-ttu-id="f0c84-123">리디렉션 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f0c84-123">The name of the Redirect Configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c84-124">RedirectType</span><span class="sxs-lookup"><span data-stu-id="f0c84-124">-RedirectType</span></span>
<span data-ttu-id="f0c84-125">리디렉션 유형</span><span class="sxs-lookup"><span data-stu-id="f0c84-125">The type of redirect</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c84-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="f0c84-126">-TargetListener</span></span>
<span data-ttu-id="f0c84-127">HTTPListener 요청을 다음으로 리디렉션합니다.</span><span class="sxs-lookup"><span data-stu-id="f0c84-127">HTTPListener to redirect the request to</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c84-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="f0c84-128">-TargetListenerID</span></span>
<span data-ttu-id="f0c84-129">요청을 리디렉션할 수신기의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f0c84-129">ID of  listener to redirect the request to</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c84-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="f0c84-130">-TargetUrl</span></span>
<span data-ttu-id="f0c84-131">대상 URL 리디렉션</span><span class="sxs-lookup"><span data-stu-id="f0c84-131">Target URL fo redirection</span></span>

```yaml
Type: String
Parameter Sets: SetByURL
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c84-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0c84-132">CommonParameters</span></span>
<span data-ttu-id="f0c84-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0c84-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0c84-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0c84-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0c84-135">입력</span><span class="sxs-lookup"><span data-stu-id="f0c84-135">INPUTS</span></span>

### <span data-ttu-id="f0c84-136">않아야</span><span class="sxs-lookup"><span data-stu-id="f0c84-136">None</span></span>

## <span data-ttu-id="f0c84-137">출력</span><span class="sxs-lookup"><span data-stu-id="f0c84-137">OUTPUTS</span></span>

### <span data-ttu-id="f0c84-138">Microsoft. 네트워크. Psapplication게이트웨이 Redirectconfiguration</span><span class="sxs-lookup"><span data-stu-id="f0c84-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="f0c84-139">상속자</span><span class="sxs-lookup"><span data-stu-id="f0c84-139">NOTES</span></span>

## <span data-ttu-id="f0c84-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f0c84-140">RELATED LINKS</span></span>

