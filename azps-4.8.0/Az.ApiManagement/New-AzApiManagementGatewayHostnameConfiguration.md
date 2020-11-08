---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: 6aadf94ff379df322907be66c73052196de803c5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204124"
---
# <span data-ttu-id="5a0ca-101">New-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a0ca-101">New-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="5a0ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a0ca-102">SYNOPSIS</span></span>
<span data-ttu-id="5a0ca-103">기존 게이트웨이에 대 한 호스트 이름 configuratin를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5a0ca-103">Creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="5a0ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5a0ca-104">SYNTAX</span></span>

```
New-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-GatewayHostnameConfigurationId <String>] -Hostname <String> -CertificateResourceId <String>
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5a0ca-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5a0ca-105">DESCRIPTION</span></span>
<span data-ttu-id="5a0ca-106">**AzApiManagementGatewayHostnameConfiguration** cmdlet은 기존 게이트웨이에 대 한 hostname configuratin를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5a0ca-106">The **New-AzApiManagementGatewayHostnameConfiguration** cmdlet creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="5a0ca-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5a0ca-107">EXAMPLES</span></span>

### <span data-ttu-id="5a0ca-108">예제 1: 기존 게이트웨이에 대 한 호스트 이름 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="5a0ca-108">Example 1: Create a hostname configuration for the existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$cert = Get-AzApiManagementCertificate -Context $apimContext -CertificateId "333"
PS C:\>New-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g01" -GatewayHostnameConfigurationId "h01" -Hostname "www.contoso.com" -CertificateResourceId $cert.Id
```

<span data-ttu-id="5a0ca-109">이 명령은 "g01" 게이트웨이에 대 한 "h01" 호스트 이름 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5a0ca-109">This command creates a "h01" hostname configuration for a "g01" gateway.</span></span>

## <span data-ttu-id="5a0ca-110">변수</span><span class="sxs-lookup"><span data-stu-id="5a0ca-110">PARAMETERS</span></span>

### <span data-ttu-id="5a0ca-111">-CertificateResourceId</span><span class="sxs-lookup"><span data-stu-id="5a0ca-111">-CertificateResourceId</span></span>
<span data-ttu-id="5a0ca-112">기존 인증서 id에 대 한 리소스 식별자입니다. 이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="5a0ca-112">A resource identifier for the existing certificate id. This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a0ca-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="5a0ca-113">-Context</span></span>
<span data-ttu-id="5a0ca-114">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="5a0ca-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5a0ca-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="5a0ca-115">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a0ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a0ca-116">-DefaultProfile</span></span>
<span data-ttu-id="5a0ca-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5a0ca-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a0ca-118">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5a0ca-118">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="5a0ca-119">새 게이트웨이 호스트 이름 confiuration의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5a0ca-119">Identifier of new gateway hostname confiuration.</span></span>
<span data-ttu-id="5a0ca-120">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5a0ca-120">This parameter is optional.</span></span>
<span data-ttu-id="5a0ca-121">지정 하지 않으면가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a0ca-121">If not specified will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a0ca-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="5a0ca-122">-GatewayId</span></span>
<span data-ttu-id="5a0ca-123">기존 게이트웨이의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5a0ca-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="5a0ca-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="5a0ca-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a0ca-125">-Hostname</span><span class="sxs-lookup"><span data-stu-id="5a0ca-125">-Hostname</span></span>
<span data-ttu-id="5a0ca-126">이름의.</span><span class="sxs-lookup"><span data-stu-id="5a0ca-126">Hostname.</span></span>
<span data-ttu-id="5a0ca-127">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="5a0ca-127">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a0ca-128">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="5a0ca-128">-NegotiateClientCertificate</span></span>
<span data-ttu-id="5a0ca-129">NegotiateClientCertificate을 적용 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="5a0ca-129">Flag to enforce NegotiateClientCertificate.</span></span>
<span data-ttu-id="5a0ca-130">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5a0ca-130">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a0ca-131">-확인</span><span class="sxs-lookup"><span data-stu-id="5a0ca-131">-Confirm</span></span>
<span data-ttu-id="5a0ca-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a0ca-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a0ca-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a0ca-133">-WhatIf</span></span>
<span data-ttu-id="5a0ca-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5a0ca-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a0ca-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5a0ca-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a0ca-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a0ca-136">CommonParameters</span></span>
<span data-ttu-id="5a0ca-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a0ca-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a0ca-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5a0ca-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a0ca-139">입력</span><span class="sxs-lookup"><span data-stu-id="5a0ca-139">INPUTS</span></span>

### <span data-ttu-id="5a0ca-140">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5a0ca-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5a0ca-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5a0ca-141">System.String</span></span>

### <span data-ttu-id="5a0ca-142">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5a0ca-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5a0ca-143">출력</span><span class="sxs-lookup"><span data-stu-id="5a0ca-143">OUTPUTS</span></span>

### <span data-ttu-id="5a0ca-144">ApiManagement. ServiceManagement. \ PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a0ca-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="5a0ca-145">상속자</span><span class="sxs-lookup"><span data-stu-id="5a0ca-145">NOTES</span></span>

## <span data-ttu-id="5a0ca-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a0ca-146">RELATED LINKS</span></span>
