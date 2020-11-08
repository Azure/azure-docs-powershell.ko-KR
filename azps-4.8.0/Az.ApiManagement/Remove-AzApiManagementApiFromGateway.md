---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
ms.openlocfilehash: 506287812f684a778fdb96e750aac34049912b58
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213758"
---
# <span data-ttu-id="e6e7b-101">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="e6e7b-101">Remove-AzApiManagementApiFromGateway</span></span>

## <span data-ttu-id="e6e7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6e7b-102">SYNOPSIS</span></span>
<span data-ttu-id="e6e7b-103">게이트웨이에 API를 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="e6e7b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e6e7b-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6e7b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e6e7b-105">DESCRIPTION</span></span>
<span data-ttu-id="e6e7b-106">**AzApiManagementApiFromGateway** cmdlet은 게이트웨이에 API를 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-106">The **Remove-AzApiManagementApiFromGateway** cmdlet attaches an API to a gateway.</span></span>

## <span data-ttu-id="e6e7b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e6e7b-107">EXAMPLES</span></span>

### <span data-ttu-id="e6e7b-108">예제 1: 게이트웨이에서 API 제거</span><span class="sxs-lookup"><span data-stu-id="e6e7b-108">Example 1: Remove an API from a gateway</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="e6e7b-109">이 명령은 게이트웨이에서 지정 된 API를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-109">This command removes the specified API from a gateway.</span></span>

## <span data-ttu-id="e6e7b-110">변수</span><span class="sxs-lookup"><span data-stu-id="e6e7b-110">PARAMETERS</span></span>

### <span data-ttu-id="e6e7b-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e6e7b-111">-ApiId</span></span>
<span data-ttu-id="e6e7b-112">게이트웨이에서 제거할 기존 Api의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-112">Identifier of existing APIs to remove from the Gateway.</span></span>
<span data-ttu-id="e6e7b-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-113">This parameter is required.</span></span>

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

### <span data-ttu-id="e6e7b-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="e6e7b-114">-Context</span></span>
<span data-ttu-id="e6e7b-115">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e6e7b-116">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-116">This parameter is required.</span></span>

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

### <span data-ttu-id="e6e7b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6e7b-117">-DefaultProfile</span></span>
<span data-ttu-id="e6e7b-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6e7b-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="e6e7b-119">-GatewayId</span></span>
<span data-ttu-id="e6e7b-120">API를 제거할 기존 게이트웨이의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-120">Identifier of existing Gateway to remove API from.</span></span>
<span data-ttu-id="e6e7b-121">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-121">This parameter is required.</span></span>

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

### <span data-ttu-id="e6e7b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6e7b-122">-PassThru</span></span>
<span data-ttu-id="e6e7b-123">지정 된 경우 대/소문자 구분 작업이 성공한 경우 true를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="e6e7b-124">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-124">This parameter is optional.</span></span>
<span data-ttu-id="e6e7b-125">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-125">Default value is false.</span></span>

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

### <span data-ttu-id="e6e7b-126">-확인</span><span class="sxs-lookup"><span data-stu-id="e6e7b-126">-Confirm</span></span>
<span data-ttu-id="e6e7b-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6e7b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6e7b-128">-WhatIf</span></span>
<span data-ttu-id="e6e7b-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6e7b-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6e7b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6e7b-131">CommonParameters</span></span>
<span data-ttu-id="e6e7b-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6e7b-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6e7b-134">입력</span><span class="sxs-lookup"><span data-stu-id="e6e7b-134">INPUTS</span></span>

### <span data-ttu-id="e6e7b-135">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e6e7b-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e6e7b-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e6e7b-136">System.String</span></span>

### <span data-ttu-id="e6e7b-137">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e6e7b-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e6e7b-138">출력</span><span class="sxs-lookup"><span data-stu-id="e6e7b-138">OUTPUTS</span></span>

### <span data-ttu-id="e6e7b-139">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e6e7b-139">System.Boolean</span></span>

## <span data-ttu-id="e6e7b-140">상속자</span><span class="sxs-lookup"><span data-stu-id="e6e7b-140">NOTES</span></span>

## <span data-ttu-id="e6e7b-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6e7b-141">RELATED LINKS</span></span>
