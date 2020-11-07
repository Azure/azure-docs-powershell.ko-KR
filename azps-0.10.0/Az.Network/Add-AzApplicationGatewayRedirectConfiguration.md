---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 60b98db10aab4456ea8ca463f49ee3f7f58ffdd2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875690"
---
# <span data-ttu-id="a4157-101">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4157-101">Add-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="a4157-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4157-102">SYNOPSIS</span></span>
<span data-ttu-id="a4157-103">응용 프로그램 게이트웨이에 리디렉션 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4157-103">Adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="a4157-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a4157-104">SYNTAX</span></span>

### <span data-ttu-id="a4157-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a4157-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4157-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a4157-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4157-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="a4157-107">SetByURL</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4157-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a4157-108">DESCRIPTION</span></span>
<span data-ttu-id="a4157-109">**Add-AzApplicationGatewayRedirectConfiguration** Cmdlet은 응용 프로그램 게이트웨이에 리디렉션 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4157-109">The **Add-AzApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="a4157-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a4157-110">EXAMPLES</span></span>

### <span data-ttu-id="a4157-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a4157-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="a4157-112">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4157-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a4157-113">두 번째 명령은 응용 프로그램 게이트웨이에 리디렉션 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4157-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="a4157-114">변수</span><span class="sxs-lookup"><span data-stu-id="a4157-114">PARAMETERS</span></span>

### <span data-ttu-id="a4157-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a4157-115">-ApplicationGateway</span></span>
<span data-ttu-id="a4157-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a4157-116">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4157-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4157-117">-DefaultProfile</span></span>
<span data-ttu-id="a4157-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a4157-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4157-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="a4157-119">-IncludePath</span></span>
<span data-ttu-id="a4157-120">리디렉션된 url의 포함 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="a4157-120">Include path in the redirected url.</span></span>
<span data-ttu-id="a4157-121">기본값은 true입니다.</span><span class="sxs-lookup"><span data-stu-id="a4157-121">Default is true.</span></span>

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

### <span data-ttu-id="a4157-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="a4157-122">-IncludeQueryString</span></span>
<span data-ttu-id="a4157-123">리디렉션된 url에 쿼리 문자열을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4157-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="a4157-124">기본값은 true입니다.</span><span class="sxs-lookup"><span data-stu-id="a4157-124">Default is true.</span></span>

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

### <span data-ttu-id="a4157-125">-이름</span><span class="sxs-lookup"><span data-stu-id="a4157-125">-Name</span></span>
<span data-ttu-id="a4157-126">리디렉션 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a4157-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="a4157-127">RedirectType</span><span class="sxs-lookup"><span data-stu-id="a4157-127">-RedirectType</span></span>
<span data-ttu-id="a4157-128">리디렉션 유형</span><span class="sxs-lookup"><span data-stu-id="a4157-128">The type of redirect</span></span>

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

### <span data-ttu-id="a4157-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="a4157-129">-TargetListener</span></span>
<span data-ttu-id="a4157-130">HTTPListener 요청을 다음으로 리디렉션합니다.</span><span class="sxs-lookup"><span data-stu-id="a4157-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="a4157-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="a4157-131">-TargetListenerID</span></span>
<span data-ttu-id="a4157-132">요청을 리디렉션할 수신기의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a4157-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="a4157-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="a4157-133">-TargetUrl</span></span>
<span data-ttu-id="a4157-134">대상 URL 리디렉션</span><span class="sxs-lookup"><span data-stu-id="a4157-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="a4157-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4157-135">CommonParameters</span></span>
<span data-ttu-id="a4157-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4157-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4157-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4157-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4157-138">입력</span><span class="sxs-lookup"><span data-stu-id="a4157-138">INPUTS</span></span>

### <span data-ttu-id="a4157-139">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a4157-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a4157-140">출력</span><span class="sxs-lookup"><span data-stu-id="a4157-140">OUTPUTS</span></span>

### <span data-ttu-id="a4157-141">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a4157-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a4157-142">상속자</span><span class="sxs-lookup"><span data-stu-id="a4157-142">NOTES</span></span>

## <span data-ttu-id="a4157-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a4157-143">RELATED LINKS</span></span>

