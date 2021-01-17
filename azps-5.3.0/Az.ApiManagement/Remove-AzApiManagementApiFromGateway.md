---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
ms.openlocfilehash: 506287812f684a778fdb96e750aac34049912b58
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382264"
---
# <span data-ttu-id="b27d7-101">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="b27d7-101">Remove-AzApiManagementApiFromGateway</span></span>

## <span data-ttu-id="b27d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b27d7-102">SYNOPSIS</span></span>
<span data-ttu-id="b27d7-103">게이트웨이에 API를 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="b27d7-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="b27d7-104">구문</span><span class="sxs-lookup"><span data-stu-id="b27d7-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b27d7-105">설명</span><span class="sxs-lookup"><span data-stu-id="b27d7-105">DESCRIPTION</span></span>
<span data-ttu-id="b27d7-106">**Remove-AzApiManagementApiFromGateway** cmdlet은 API를 게이트웨이에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="b27d7-106">The **Remove-AzApiManagementApiFromGateway** cmdlet attaches an API to a gateway.</span></span>

## <span data-ttu-id="b27d7-107">예제</span><span class="sxs-lookup"><span data-stu-id="b27d7-107">EXAMPLES</span></span>

### <span data-ttu-id="b27d7-108">예제 1: 게이트웨이에서 API 제거</span><span class="sxs-lookup"><span data-stu-id="b27d7-108">Example 1: Remove an API from a gateway</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="b27d7-109">이 명령은 게이트웨이에서 지정된 API를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b27d7-109">This command removes the specified API from a gateway.</span></span>

## <span data-ttu-id="b27d7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b27d7-110">PARAMETERS</span></span>

### <span data-ttu-id="b27d7-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b27d7-111">-ApiId</span></span>
<span data-ttu-id="b27d7-112">게이트웨이에서 제거할 기존 API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b27d7-112">Identifier of existing APIs to remove from the Gateway.</span></span>
<span data-ttu-id="b27d7-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="b27d7-113">This parameter is required.</span></span>

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

### <span data-ttu-id="b27d7-114">-Context</span><span class="sxs-lookup"><span data-stu-id="b27d7-114">-Context</span></span>
<span data-ttu-id="b27d7-115">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="b27d7-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b27d7-116">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="b27d7-116">This parameter is required.</span></span>

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

### <span data-ttu-id="b27d7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b27d7-117">-DefaultProfile</span></span>
<span data-ttu-id="b27d7-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b27d7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b27d7-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="b27d7-119">-GatewayId</span></span>
<span data-ttu-id="b27d7-120">API를 제거할 기존 게이트웨이의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b27d7-120">Identifier of existing Gateway to remove API from.</span></span>
<span data-ttu-id="b27d7-121">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="b27d7-121">This parameter is required.</span></span>

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

### <span data-ttu-id="b27d7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b27d7-122">-PassThru</span></span>
<span data-ttu-id="b27d7-123">지정된 경우 작업이 성공하는 경우 true를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="b27d7-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="b27d7-124">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="b27d7-124">This parameter is optional.</span></span>
<span data-ttu-id="b27d7-125">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="b27d7-125">Default value is false.</span></span>

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

### <span data-ttu-id="b27d7-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b27d7-126">-Confirm</span></span>
<span data-ttu-id="b27d7-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b27d7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b27d7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b27d7-128">-WhatIf</span></span>
<span data-ttu-id="b27d7-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b27d7-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b27d7-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b27d7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b27d7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b27d7-131">CommonParameters</span></span>
<span data-ttu-id="b27d7-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b27d7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b27d7-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b27d7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b27d7-134">입력</span><span class="sxs-lookup"><span data-stu-id="b27d7-134">INPUTS</span></span>

### <span data-ttu-id="b27d7-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b27d7-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b27d7-136">System.String</span><span class="sxs-lookup"><span data-stu-id="b27d7-136">System.String</span></span>

### <span data-ttu-id="b27d7-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b27d7-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b27d7-138">출력</span><span class="sxs-lookup"><span data-stu-id="b27d7-138">OUTPUTS</span></span>

### <span data-ttu-id="b27d7-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b27d7-139">System.Boolean</span></span>

## <span data-ttu-id="b27d7-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b27d7-140">NOTES</span></span>

## <span data-ttu-id="b27d7-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b27d7-141">RELATED LINKS</span></span>
