---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: 2cb7455d5a902882fdd98dd5fea47ae5a28e1dc9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880366"
---
# <span data-ttu-id="15a12-101">New-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="15a12-101">New-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="15a12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15a12-102">SYNOPSIS</span></span>
<span data-ttu-id="15a12-103">응용 프로그램 게이트웨이에 대 한 리디렉션 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="15a12-103">Creates a redirect configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15a12-104">구문과</span><span class="sxs-lookup"><span data-stu-id="15a12-104">SYNTAX</span></span>

### <span data-ttu-id="15a12-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="15a12-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15a12-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="15a12-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15a12-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="15a12-107">SetByURL</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15a12-108">설명은</span><span class="sxs-lookup"><span data-stu-id="15a12-108">DESCRIPTION</span></span>
<span data-ttu-id="15a12-109">**AzureRmApplicationGatewayRedirectConfiguration Cmdlet은** 응용 프로그램 게이트웨이에 대 한 리디렉션 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="15a12-109">**The New-AzureRmApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="15a12-110">예제의</span><span class="sxs-lookup"><span data-stu-id="15a12-110">EXAMPLES</span></span>

### <span data-ttu-id="15a12-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="15a12-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="15a12-112">이 명령은 Redirect01 이라는 리디렉션 구성을 만들고 그 결과를 $RedirectConfig 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="15a12-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="15a12-113">변수</span><span class="sxs-lookup"><span data-stu-id="15a12-113">PARAMETERS</span></span>

### <span data-ttu-id="15a12-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a12-114">-DefaultProfile</span></span>
<span data-ttu-id="15a12-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="15a12-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15a12-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="15a12-116">-IncludePath</span></span>
<span data-ttu-id="15a12-117">리디렉션된 url의 포함 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="15a12-117">Include path in the redirected url.</span></span>
<span data-ttu-id="15a12-118">기본값은 true입니다.</span><span class="sxs-lookup"><span data-stu-id="15a12-118">Default is true.</span></span>

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

### <span data-ttu-id="15a12-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="15a12-119">-IncludeQueryString</span></span>
<span data-ttu-id="15a12-120">리디렉션된 url에 쿼리 문자열을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="15a12-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="15a12-121">기본값은 true입니다.</span><span class="sxs-lookup"><span data-stu-id="15a12-121">Default is true.</span></span>

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

### <span data-ttu-id="15a12-122">-이름</span><span class="sxs-lookup"><span data-stu-id="15a12-122">-Name</span></span>
<span data-ttu-id="15a12-123">리디렉션 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15a12-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="15a12-124">RedirectType</span><span class="sxs-lookup"><span data-stu-id="15a12-124">-RedirectType</span></span>
<span data-ttu-id="15a12-125">리디렉션 유형</span><span class="sxs-lookup"><span data-stu-id="15a12-125">The type of redirect</span></span>

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

### <span data-ttu-id="15a12-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="15a12-126">-TargetListener</span></span>
<span data-ttu-id="15a12-127">HTTPListener 요청을 다음으로 리디렉션합니다.</span><span class="sxs-lookup"><span data-stu-id="15a12-127">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="15a12-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="15a12-128">-TargetListenerID</span></span>
<span data-ttu-id="15a12-129">요청을 리디렉션할 수신기의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="15a12-129">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="15a12-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="15a12-130">-TargetUrl</span></span>
<span data-ttu-id="15a12-131">대상 URL 리디렉션</span><span class="sxs-lookup"><span data-stu-id="15a12-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="15a12-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a12-132">CommonParameters</span></span>
<span data-ttu-id="15a12-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="15a12-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a12-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15a12-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a12-135">입력</span><span class="sxs-lookup"><span data-stu-id="15a12-135">INPUTS</span></span>

### <span data-ttu-id="15a12-136">않아야</span><span class="sxs-lookup"><span data-stu-id="15a12-136">None</span></span>

## <span data-ttu-id="15a12-137">출력</span><span class="sxs-lookup"><span data-stu-id="15a12-137">OUTPUTS</span></span>

### <span data-ttu-id="15a12-138">Microsoft. 네트워크. Psapplication게이트웨이 Redirectconfiguration</span><span class="sxs-lookup"><span data-stu-id="15a12-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="15a12-139">상속자</span><span class="sxs-lookup"><span data-stu-id="15a12-139">NOTES</span></span>

## <span data-ttu-id="15a12-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="15a12-140">RELATED LINKS</span></span>

