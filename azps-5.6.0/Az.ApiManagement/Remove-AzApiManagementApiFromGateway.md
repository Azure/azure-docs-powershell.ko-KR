---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementapifromgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
ms.openlocfilehash: 2b50ddb0186e1c7ca8bc0da237f3fca833cb7367
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959072"
---
# <span data-ttu-id="66637-101">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="66637-101">Remove-AzApiManagementApiFromGateway</span></span>

## <span data-ttu-id="66637-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66637-102">SYNOPSIS</span></span>
<span data-ttu-id="66637-103">게이트웨이에 API를 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="66637-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="66637-104">구문</span><span class="sxs-lookup"><span data-stu-id="66637-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66637-105">설명</span><span class="sxs-lookup"><span data-stu-id="66637-105">DESCRIPTION</span></span>
<span data-ttu-id="66637-106">**Remove-AzApiManagementApiFromGateway** cmdlet은 게이트웨이에 API를 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="66637-106">The **Remove-AzApiManagementApiFromGateway** cmdlet attaches an API to a gateway.</span></span>

## <span data-ttu-id="66637-107">예제</span><span class="sxs-lookup"><span data-stu-id="66637-107">EXAMPLES</span></span>

### <span data-ttu-id="66637-108">예제 1: 게이트웨이에서 API 제거</span><span class="sxs-lookup"><span data-stu-id="66637-108">Example 1: Remove an API from a gateway</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="66637-109">이 명령은 게이트웨이에서 지정된 API를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="66637-109">This command removes the specified API from a gateway.</span></span>

## <span data-ttu-id="66637-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="66637-110">PARAMETERS</span></span>

### <span data-ttu-id="66637-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="66637-111">-ApiId</span></span>
<span data-ttu-id="66637-112">게이트웨이에서 제거할 기존 API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="66637-112">Identifier of existing APIs to remove from the Gateway.</span></span>
<span data-ttu-id="66637-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="66637-113">This parameter is required.</span></span>

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

### <span data-ttu-id="66637-114">-Context</span><span class="sxs-lookup"><span data-stu-id="66637-114">-Context</span></span>
<span data-ttu-id="66637-115">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="66637-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="66637-116">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="66637-116">This parameter is required.</span></span>

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

### <span data-ttu-id="66637-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66637-117">-DefaultProfile</span></span>
<span data-ttu-id="66637-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="66637-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66637-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="66637-119">-GatewayId</span></span>
<span data-ttu-id="66637-120">API를 제거할 기존 게이트웨이의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="66637-120">Identifier of existing Gateway to remove API from.</span></span>
<span data-ttu-id="66637-121">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="66637-121">This parameter is required.</span></span>

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

### <span data-ttu-id="66637-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66637-122">-PassThru</span></span>
<span data-ttu-id="66637-123">지정한 경우 작업이 성공할 경우 true를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="66637-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="66637-124">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="66637-124">This parameter is optional.</span></span>
<span data-ttu-id="66637-125">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="66637-125">Default value is false.</span></span>

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

### <span data-ttu-id="66637-126">-확인</span><span class="sxs-lookup"><span data-stu-id="66637-126">-Confirm</span></span>
<span data-ttu-id="66637-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="66637-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66637-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66637-128">-WhatIf</span></span>
<span data-ttu-id="66637-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="66637-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="66637-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66637-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66637-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66637-131">CommonParameters</span></span>
<span data-ttu-id="66637-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="66637-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66637-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66637-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66637-134">입력</span><span class="sxs-lookup"><span data-stu-id="66637-134">INPUTS</span></span>

### <span data-ttu-id="66637-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="66637-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="66637-136">System.String</span><span class="sxs-lookup"><span data-stu-id="66637-136">System.String</span></span>

### <span data-ttu-id="66637-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="66637-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="66637-138">출력</span><span class="sxs-lookup"><span data-stu-id="66637-138">OUTPUTS</span></span>

### <span data-ttu-id="66637-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="66637-139">System.Boolean</span></span>

## <span data-ttu-id="66637-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="66637-140">NOTES</span></span>

## <span data-ttu-id="66637-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66637-141">RELATED LINKS</span></span>
