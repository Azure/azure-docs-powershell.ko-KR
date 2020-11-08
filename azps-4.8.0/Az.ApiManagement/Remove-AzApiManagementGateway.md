---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
ms.openlocfilehash: 9b6eac7a0c0c994797de51c936840da515ef3f4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048550"
---
# <span data-ttu-id="1ad82-101">Remove-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="1ad82-101">Remove-AzApiManagementGateway</span></span>

## <span data-ttu-id="1ad82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ad82-102">SYNOPSIS</span></span>
<span data-ttu-id="1ad82-103">게이트웨이에서 API를 분리 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ad82-103">Detaches an API from a Gateway.</span></span>

## <span data-ttu-id="1ad82-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1ad82-104">SYNTAX</span></span>

### <span data-ttu-id="1ad82-105">ContextParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="1ad82-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ad82-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ad82-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ad82-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ad82-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGateway -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ad82-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1ad82-108">DESCRIPTION</span></span>
<span data-ttu-id="1ad82-109">**AzApiManagementGateway** Cmdlet은 게이트웨이에서 API를 분리 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ad82-109">The **Remove-AzApiManagementGateway** cmdlet detaches an API from a Gateway.</span></span>

## <span data-ttu-id="1ad82-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1ad82-110">EXAMPLES</span></span>

### <span data-ttu-id="1ad82-111">예제 1: 기존 게이트웨이 제거</span><span class="sxs-lookup"><span data-stu-id="1ad82-111">Example 1: Remove an existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGateway -Context $apimContext -GatewayId "g0001" -Force
```

<span data-ttu-id="1ad82-112">이 명령은 기존 게이트웨이를 제거 하 고 사용자에 게 확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1ad82-112">This command removes an existing gateway and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="1ad82-113">변수</span><span class="sxs-lookup"><span data-stu-id="1ad82-113">PARAMETERS</span></span>

### <span data-ttu-id="1ad82-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="1ad82-114">-Context</span></span>
<span data-ttu-id="1ad82-115">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="1ad82-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1ad82-116">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="1ad82-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ad82-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ad82-117">-DefaultProfile</span></span>
<span data-ttu-id="1ad82-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1ad82-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ad82-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="1ad82-119">-GatewayId</span></span>
<span data-ttu-id="1ad82-120">기존 게이트웨이의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="1ad82-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="1ad82-121">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="1ad82-121">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ad82-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ad82-122">-InputObject</span></span>
<span data-ttu-id="1ad82-123">PsApiManagementGateway의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="1ad82-123">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="1ad82-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="1ad82-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ad82-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ad82-125">-PassThru</span></span>
<span data-ttu-id="1ad82-126">지정 된 경우 대/소문자 구분 작업이 성공한 경우 true를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="1ad82-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="1ad82-127">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1ad82-127">This parameter is optional.</span></span>
<span data-ttu-id="1ad82-128">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="1ad82-128">Default value is false.</span></span>

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

### <span data-ttu-id="1ad82-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ad82-129">-ResourceId</span></span>
<span data-ttu-id="1ad82-130">게이트웨이의 팔 인 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="1ad82-130">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="1ad82-131">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="1ad82-131">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ad82-132">-확인</span><span class="sxs-lookup"><span data-stu-id="1ad82-132">-Confirm</span></span>
<span data-ttu-id="1ad82-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ad82-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ad82-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ad82-134">-WhatIf</span></span>
<span data-ttu-id="1ad82-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1ad82-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ad82-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1ad82-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ad82-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ad82-137">CommonParameters</span></span>
<span data-ttu-id="1ad82-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ad82-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ad82-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1ad82-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ad82-140">입력</span><span class="sxs-lookup"><span data-stu-id="1ad82-140">INPUTS</span></span>

### <span data-ttu-id="1ad82-141">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1ad82-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1ad82-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1ad82-142">System.String</span></span>

### <span data-ttu-id="1ad82-143">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1ad82-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1ad82-144">출력</span><span class="sxs-lookup"><span data-stu-id="1ad82-144">OUTPUTS</span></span>

### <span data-ttu-id="1ad82-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1ad82-145">System.Boolean</span></span>

## <span data-ttu-id="1ad82-146">상속자</span><span class="sxs-lookup"><span data-stu-id="1ad82-146">NOTES</span></span>

## <span data-ttu-id="1ad82-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ad82-147">RELATED LINKS</span></span>
