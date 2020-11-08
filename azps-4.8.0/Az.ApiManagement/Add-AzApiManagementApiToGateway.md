---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitogateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
ms.openlocfilehash: 6bb40d46c80e609824b1c56d05091ade5716f7f8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056846"
---
# <span data-ttu-id="79713-101">Add-AzApiManagementApiToGateway</span><span class="sxs-lookup"><span data-stu-id="79713-101">Add-AzApiManagementApiToGateway</span></span>

## <span data-ttu-id="79713-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79713-102">SYNOPSIS</span></span>
<span data-ttu-id="79713-103">게이트웨이에 API를 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="79713-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="79713-104">구문과</span><span class="sxs-lookup"><span data-stu-id="79713-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-ProvisioningState <PsApiManagementGatewayApiProvisioningState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79713-105">설명은</span><span class="sxs-lookup"><span data-stu-id="79713-105">DESCRIPTION</span></span>
<span data-ttu-id="79713-106">**Add-AzApiManagementApiToGateway** Cmdlet은 게이트웨이에 Azure API Management api를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="79713-106">The **Add-AzApiManagementApiToGateway** cmdlet adds an Azure API Management API to a Gateway.</span></span>

## <span data-ttu-id="79713-107">예제의</span><span class="sxs-lookup"><span data-stu-id="79713-107">EXAMPLES</span></span>

### <span data-ttu-id="79713-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="79713-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001"
```

<span data-ttu-id="79713-109">이 명령은 지정 된 게이트웨이에 지정 된 API를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="79713-109">This command adds the specified API to the specified Gateway.</span></span>

## <span data-ttu-id="79713-110">변수</span><span class="sxs-lookup"><span data-stu-id="79713-110">PARAMETERS</span></span>

### <span data-ttu-id="79713-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="79713-111">-ApiId</span></span>
<span data-ttu-id="79713-112">기존 API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="79713-112">Identifier of existing API.</span></span>
<span data-ttu-id="79713-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="79713-113">This parameter is required.</span></span>

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

### <span data-ttu-id="79713-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="79713-114">-Context</span></span>
<span data-ttu-id="79713-115">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="79713-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="79713-116">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="79713-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79713-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79713-117">-DefaultProfile</span></span>
<span data-ttu-id="79713-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="79713-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79713-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="79713-119">-GatewayId</span></span>
<span data-ttu-id="79713-120">기존 게이트웨이의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="79713-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="79713-121">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="79713-121">This parameter is required.</span></span>

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

### <span data-ttu-id="79713-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79713-122">-PassThru</span></span>
<span data-ttu-id="79713-123">지정 된 경우 대/소문자 구분 작업이 성공한 경우 true를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="79713-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="79713-124">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="79713-124">This parameter is optional.</span></span>
<span data-ttu-id="79713-125">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="79713-125">Default value is false.</span></span>

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

### <span data-ttu-id="79713-126">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="79713-126">-ProvisioningState</span></span>
<span data-ttu-id="79713-127">프로 비전 상태 (생성 됨)입니다.</span><span class="sxs-lookup"><span data-stu-id="79713-127">Provisioning State (Created).</span></span>
<span data-ttu-id="79713-128">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="79713-128">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState]
Parameter Sets: (All)
Aliases:
Accepted values: Created

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79713-129">-확인</span><span class="sxs-lookup"><span data-stu-id="79713-129">-Confirm</span></span>
<span data-ttu-id="79713-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="79713-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79713-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79713-131">-WhatIf</span></span>
<span data-ttu-id="79713-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="79713-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79713-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79713-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79713-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79713-134">CommonParameters</span></span>
<span data-ttu-id="79713-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="79713-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79713-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="79713-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79713-137">입력</span><span class="sxs-lookup"><span data-stu-id="79713-137">INPUTS</span></span>

### <span data-ttu-id="79713-138">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="79713-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="79713-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="79713-139">System.String</span></span>

### <span data-ttu-id="79713-140">시스템 Null 허용 ' 1 [[ApiManagement]. ServiceManagement, PsApiManagementGatewayApiProvisioningState, Microsoft azure. PowerShell. ApiManagement, Version = ServiceManagement, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="79713-140">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="79713-141">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="79713-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="79713-142">출력</span><span class="sxs-lookup"><span data-stu-id="79713-142">OUTPUTS</span></span>

### <span data-ttu-id="79713-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="79713-143">System.Boolean</span></span>

## <span data-ttu-id="79713-144">상속자</span><span class="sxs-lookup"><span data-stu-id="79713-144">NOTES</span></span>

## <span data-ttu-id="79713-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79713-145">RELATED LINKS</span></span>

[<span data-ttu-id="79713-146">제거-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="79713-146">Remove-AzApiManagementApiFromGateway</span></span>](./Remove-AzApiManagementApiFromGateway.md)