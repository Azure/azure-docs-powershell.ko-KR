---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: 6aadf94ff379df322907be66c73052196de803c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182377"
---
# <span data-ttu-id="9b3b3-101">New-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b3b3-101">New-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="9b3b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b3b3-102">SYNOPSIS</span></span>
<span data-ttu-id="9b3b3-103">기존 게이트웨이에 대한 호스트 이름 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b3b3-103">Creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="9b3b3-104">구문</span><span class="sxs-lookup"><span data-stu-id="9b3b3-104">SYNTAX</span></span>

```
New-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-GatewayHostnameConfigurationId <String>] -Hostname <String> -CertificateResourceId <String>
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b3b3-105">설명</span><span class="sxs-lookup"><span data-stu-id="9b3b3-105">DESCRIPTION</span></span>
<span data-ttu-id="9b3b3-106">**New-AzApiManagementGatewayHostnameConfiguration** cmdlet은 기존 게이트웨이에 대한 호스트 이름 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b3b3-106">The **New-AzApiManagementGatewayHostnameConfiguration** cmdlet creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="9b3b3-107">예제</span><span class="sxs-lookup"><span data-stu-id="9b3b3-107">EXAMPLES</span></span>

### <span data-ttu-id="9b3b3-108">예제 1: 기존 게이트웨이에 대한 호스트 이름 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="9b3b3-108">Example 1: Create a hostname configuration for the existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$cert = Get-AzApiManagementCertificate -Context $apimContext -CertificateId "333"
PS C:\>New-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g01" -GatewayHostnameConfigurationId "h01" -Hostname "www.contoso.com" -CertificateResourceId $cert.Id
```

<span data-ttu-id="9b3b3-109">이 명령은 "g01" 게이트웨이에 대한 "h01" 호스트 이름 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b3b3-109">This command creates a "h01" hostname configuration for a "g01" gateway.</span></span>

## <span data-ttu-id="9b3b3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b3b3-110">PARAMETERS</span></span>

### <span data-ttu-id="9b3b3-111">-CertificateResourceId</span><span class="sxs-lookup"><span data-stu-id="9b3b3-111">-CertificateResourceId</span></span>
<span data-ttu-id="9b3b3-112">기존 인증서 ID에 대한 리소스 식별자입니다. 이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3b3-112">A resource identifier for the existing certificate id. This parameter is required.</span></span>

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

### <span data-ttu-id="9b3b3-113">-Context</span><span class="sxs-lookup"><span data-stu-id="9b3b3-113">-Context</span></span>
<span data-ttu-id="9b3b3-114">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3b3-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9b3b3-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3b3-115">This parameter is required.</span></span>

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

### <span data-ttu-id="9b3b3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b3b3-116">-DefaultProfile</span></span>
<span data-ttu-id="9b3b3-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3b3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b3b3-118">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9b3b3-118">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="9b3b3-119">새 게이트웨이 호스트 이름 연결의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3b3-119">Identifier of new gateway hostname confiuration.</span></span>
<span data-ttu-id="9b3b3-120">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3b3-120">This parameter is optional.</span></span>
<span data-ttu-id="9b3b3-121">지정하지 않으면 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b3b3-121">If not specified will be generated.</span></span>

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

### <span data-ttu-id="9b3b3-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="9b3b3-122">-GatewayId</span></span>
<span data-ttu-id="9b3b3-123">기존 게이트웨이의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3b3-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="9b3b3-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3b3-124">This parameter is required.</span></span>

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

### <span data-ttu-id="9b3b3-125">-Hostname</span><span class="sxs-lookup"><span data-stu-id="9b3b3-125">-Hostname</span></span>
<span data-ttu-id="9b3b3-126">호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3b3-126">Hostname.</span></span>
<span data-ttu-id="9b3b3-127">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3b3-127">This parameter is required.</span></span>

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

### <span data-ttu-id="9b3b3-128">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="9b3b3-128">-NegotiateClientCertificate</span></span>
<span data-ttu-id="9b3b3-129">NegotiateClientCertificate를 적용하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3b3-129">Flag to enforce NegotiateClientCertificate.</span></span>
<span data-ttu-id="9b3b3-130">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3b3-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="9b3b3-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b3b3-131">-Confirm</span></span>
<span data-ttu-id="9b3b3-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b3b3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b3b3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b3b3-133">-WhatIf</span></span>
<span data-ttu-id="9b3b3-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9b3b3-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b3b3-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9b3b3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b3b3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b3b3-136">CommonParameters</span></span>
<span data-ttu-id="9b3b3-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3b3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b3b3-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9b3b3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b3b3-139">입력</span><span class="sxs-lookup"><span data-stu-id="9b3b3-139">INPUTS</span></span>

### <span data-ttu-id="9b3b3-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9b3b3-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9b3b3-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9b3b3-141">System.String</span></span>

### <span data-ttu-id="9b3b3-142">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9b3b3-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9b3b3-143">출력</span><span class="sxs-lookup"><span data-stu-id="9b3b3-143">OUTPUTS</span></span>

### <span data-ttu-id="9b3b3-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b3b3-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="9b3b3-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9b3b3-145">NOTES</span></span>

## <span data-ttu-id="9b3b3-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b3b3-146">RELATED LINKS</span></span>
